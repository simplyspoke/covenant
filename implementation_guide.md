# Implementation Guide: Claude Code and Desktop App

*Mac setup. Getting running and connected to the repository. First draft.*

---

## Prerequisites

- macOS 13.0 (Ventura) or later
- An active Claude Pro, Max, Teams, or Enterprise subscription — the free tier does not include CLI access
- A GitHub account with the loom-and-stone repository created
- Git installed — verify with `git --version` in Terminal

---

## Option A: Claude Desktop App

The Desktop app is the lowest-friction entry point. No terminal required. Good for conversation, document work, and quick questions.

### Install

1. Visit [claude.ai/download](https://claude.ai/download) and download the macOS version
2. Open the downloaded file and drag Claude to Applications
3. Open Claude from Finder > Applications
4. Sign in with your Anthropic account

### Connect to the Repository

The Desktop app does not connect directly to GitHub. Use Claude Projects instead:

1. In Claude, create a new Project — name it `loom-and-stone`
2. Upload the core documents as project context:
   - README.md
   - covenant.md
   - context-document.md
   - operating-agreement.md
   - roles.md
3. Each new conversation within the project inherits this context automatically
4. Update the uploaded documents periodically as the repository evolves

### Recommended Settings

- Set a keyboard shortcut in Preferences for quick access from anywhere
- Keep the project documents current — when documents change in the repository, re-upload to the project

---

## Option B: Claude Code CLI

Claude Code lives in your terminal and operates within your project directory. It can read your files directly, making it the most connected option for working within the repository.

### Install

Open Terminal and run the native installer:

```bash
curl -fsSL https://claude.ai/install.sh | bash
```

Do not use `sudo`. Do not use the npm method — it is deprecated.

Verify the installation:

```bash
claude --version
```

Run diagnostics to confirm everything is healthy:

```bash
claude --doctor
```

### Authenticate

On first run, Claude Code will open your browser to authenticate:

```bash
claude
```

Log in with your Anthropic account and approve access. Your credentials are stored in your Mac keychain — you will not need to log in again.

### Connect to the Repository

Navigate to your local clone of the repository before starting Claude Code:

```bash
cd ~/path/to/loom-and-stone
claude
```

Claude Code reads the files in your current directory. Starting it from within the repository means it has access to all documents as context without additional configuration.

To keep context focused, start Claude Code from the relevant subdirectory when working on a specific area:

```bash
cd ~/path/to/loom-and-stone/participants
claude
```

### Useful Commands

| Command | Purpose |
|---|---|
| `claude` | Start a new session in the current directory |
| `claude --continue` | Continue the previous session |
| `claude --resume` | Open a past session |
| `claude --doctor` | Run diagnostics |
| `/exit` | Exit Claude Code |
| `/model` | Change the model |
| `?` | Help |

---

## Keeping Both in Sync

- **Repository** is the source of truth — all document changes commit and push here
- **Claude Projects** (Desktop) — re-upload changed documents after significant updates
- **Claude Code CLI** — always reads live from the filesystem, no sync needed

A simple workflow:

1. Edit documents in your IDE or Obsidian
2. Commit and push to GitHub
3. If using the Desktop app, re-upload updated documents to the Project
4. Claude Code CLI picks up changes automatically on next session

---

## Option C: DevPod + DevContainer (Recommended for Isolation)

DevPod is an open source DevContainer client that runs the same container environment locally or on a cloud provider without lock-in. Claude Code runs inside the container with access only to the repository — no access to your host keychain, SSH keys, or admin credentials.

### Why This Approach

- Claude Code operates in its own isolated session, not yours
- Credentials and tokens on your host machine are not accessible inside the container
- The same configuration runs locally via Docker or on a cloud provider
- DevPod has a desktop GUI alongside CLI, matching your preferred working style
- The `.devcontainer` configuration lives in the repository — portable and version controlled

### Prerequisites

- [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop/) installed and running
- [DevPod](https://devpod.sh) installed — download the Mac desktop app or install via Homebrew:

```bash
brew install --cask devpod
```

### Starter .devcontainer Configuration

Add the following to your repository at `.devcontainer/devcontainer.json`:

```json
{
  "name": "loom-and-stone",
  "image": "mcr.microsoft.com/devcontainers/base:ubuntu",
  "features": {
    "ghcr.io/devcontainers/features/git:1": {},
    "ghcr.io/devcontainers/features/node:1": {
      "version": "18"
    },
    "ghcr.io/devcontainers/features/python:1": {
      "version": "3.11"
    }
  },
  "postCreateCommand": "curl -fsSL https://claude.ai/install.sh | bash",
  "mounts": [],
  "remoteEnv": {
    "ANTHROPIC_API_KEY": "${localEnv:ANTHROPIC_API_KEY}"
  },
  "customizations": {
    "vscode": {
      "extensions": [
        "anthropic.claude-code"
      ]
    }
  }
}
```

This configuration:
- Uses a clean Ubuntu base image with no host credentials
- Installs Claude Code on container creation
- Passes only the Anthropic API key from your host environment — nothing else
- Installs the Claude Code VSCode extension if you open the container in VSCode

### Running Locally with DevPod

1. Open DevPod desktop app
2. Add a new workspace — point it to your local repository path or GitHub repository URL
3. Select Docker as the provider
4. DevPod builds the container and opens the workspace
5. Start Claude Code inside the container:

```bash
claude
```

Claude Code now operates within the container. It can read and modify repository files but cannot access your host machine beyond what is explicitly mounted.

### Running on a Cloud Provider

DevPod supports multiple cloud providers with the same configuration — no changes to the `.devcontainer` setup required.

1. In DevPod, add a cloud provider — AWS, GCP, DigitalOcean, and others are supported
2. Create a new workspace pointing to your GitHub repository
3. Select your cloud provider instead of Docker
4. DevPod provisions the environment and connects you via SSH automatically

This is useful when you want Claude Code running independently of your local machine, or when the work involves infrastructure that should not run locally.

### Credential Handling

Only pass credentials the container genuinely needs. For the repository and document work:

```bash
# Set in your host shell before starting DevPod
export ANTHROPIC_API_KEY=your_key_here
```

Never mount your host `~/.ssh` or `~/.aws` directories into the container unless a specific task requires it — and treat that as an exception requiring review, not a default.

---

## Open Items and Next Steps

- **MCP integration** — Model Context Protocol would allow Claude Code to connect directly to GitHub as a live data source, eliminating the need to re-upload documents to Projects. Worth exploring when ready to move toward active AI participant implementation. See todo for details.
- **CLAUDE.md** — Claude Code looks for a `CLAUDE.md` file in the project root for persistent instructions. Consider creating one that points to the covenant, context document, and operating agreement as the starting context for any session. This is the closest current equivalent to a persistent system prompt for the CLI.
- **DevContainer refinement** — the starter config is intentionally minimal. As the work evolves and specific tools or languages are added, extend the `.devcontainer/devcontainer.json` to match. Treat it like any other anchor document — version controlled, reviewed, changed through process.

---

## Related Documents

- README — project overview and document index
- Context Document — participant orientation
- Todo — open items including MCP exploration

*First drafted: February 2026*
