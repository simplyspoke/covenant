# Workstation Configuration

*Reference document. Extracted from team standards.*

---

## IDE

- **VSCode** — standard IDE with a set of preferred extensions
- Maintain a dotfiles repository for consistent environment setup across machines

## Editor Settings

- Use an `.editorconfig` file for consistent editor settings across participants

## Credentials and Security

- Manage SSH sessions with a **GPG key stored on a Yubikey**
- Use **short-lived credentials** where possible
- Encrypt sensitive values locally and remotely
- Regularly rotate vulnerable credentials

## Environment Configuration

- Use **direnv** for environment-specific configurations
- Include `.envrc.example` in project repositories for ENV configuration reference

## Local Development

- Deploy locally only for static tests and low-level integration
- Prefer **Kubernetes** for comprehensive testing environments

## Package and Release Management

- Use **Node.js** for managing projects
- Use **semantic-release** for automated releases
- Use **Prettier** for linting and formatting
- Use **lint-staged** and **Husky** to enforce linting and formatting before commits

---

*Extracted: February 2026*
