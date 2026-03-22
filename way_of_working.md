# Way of Working

*A living document. First draft.*

---

## Purpose

This document captures the texture of how work actually happens within Loom and Stone — the rhythms, habits, and practices that make the framework livable day to day. It is not policy. It is practice. Where governance documents set the rules, this document describes the practice.

---

## Rhythms

**Daily**
A brief check-in at the start of the working day. Not a status report — a orientation. What is in motion, what needs attention, what is blocked. Kept short. Asynchronous where possible.

**Weekly**
A planning session to set direction for the week. Review what was completed, what carries forward, and what is new. This is the primary moment for adjusting priorities and surfacing anything that needs more than a day to resolve.

**As needed**
Outside of the daily and weekly rhythms, communication happens within windows — mid-to-late morning or evening after dinner where possible. Interruptions outside those windows should be reserved for things that genuinely cannot wait.

---

## Task and Work Tracking

Work is tracked in Asana. Tasks move through a board structure — Backlog, Selected for Work, In Progress, Done. All participants are responsible for keeping their tasks current.

- Transition to In Progress when work begins
- Add comments for clarity on status or to support handoffs
- Move to Done upon acceptance and merge

In Progress covers all active work including work awaiting review. A comment on the task signals when something is ready for review rather than a separate board column.

For tasks that are not yet ready to be formal Asana items, Google Keep and working documents serve as a lightweight capture layer. Anything that matters eventually moves to Asana or a project document.

---

## Git and Version Control

**Branching**
- Default branch: `main`
- Branch naming: `feature/task-id`
- Simple projects use GitHub Flow. Complex projects use GitFlow.

**Commits**
- Follow the Conventional Commits standard — [conventionalcommits.org](https://www.conventionalcommits.org/en/v1.0.0/)
- Use Commitizen for standardized commit messages
- Commit regularly — daily at minimum, hourly where practical
- Push often. Do not accumulate unpushed work.

**Pull Requests**
- Open PRs early for visibility and feedback — not only when work is complete
- At least one participant familiar with the scope must review before merge
- No participant merges their own work without sign-off
- Automated tooling handles linting, formatting, and policy enforcement — reviewers focus on intent, design, and exceptions

---

## Definition of Done

Work is done when:

- The implementation matches the intent of the request
- Automated checks pass — linting, formatting, security scanning, tests
- At least one other participant has reviewed and accepted
- Documentation has been updated or created as part of the work
- The task is transitioned to Done in Asana

Done is not done if documentation is deferred. Documentation is part of the work, not a follow-on task.

---

## Documentation

Documentation lives across three layers depending on audience and use:

- **GitHub** — technical documentation, READMEs, changelogs, and standards. Source of truth for project-level docs.
- **Obsidian** — working notes, drafts, and personal knowledge management. Not a shared source of truth but a useful drafting layer.
- **Google Docs** — accessible shared documents for participants who prefer a GUI. Used for collaboration where Markdown is a barrier.

Every project includes:
- A README with basic project information
- A `makefile` for common commands
- An `.envrc.example` for environment configuration
- A `CHANGELOG.md` maintained as part of the release process
- Code comments explaining the purpose of each significant block

The standard is: a similarly skilled new participant should be able to understand and continue any piece of work from its documentation alone.

---

## Code Quality

Automated tooling enforces the baseline. Participants do not need to manually police formatting or style — the tools do it.

- Prettier for formatting
- `.editorconfig` for editor consistency
- Language-specific guidelines referenced from [awesome-guidelines](https://github.com/Kristories/awesome-guidelines)

Code review focuses on what automation cannot catch — intent, design decisions, edge cases, and anything novel or high-risk.

---

## Testing

- Begin with manual testing descriptions before automating
- No fixed coverage target — evaluate based on project goals and risk
- Prioritize strong unit tests, effective integration tests, and selective end-to-end tests
- CI/CD handles automated testing, scanning, building, and deployment

---

## Security

- Short-lived credentials where possible
- Encrypt sensitive values locally and remotely
- Rotate vulnerable credentials regularly
- Leverage GitHub dependency scanning and language-specific package managers
- Least privilege, encryption at rest, limited ports and sources as defaults
- Regular security audits as a goal, not an afterthought

---

## Monitoring and Observability

- Inventory key system metrics for centralized monitoring
- Log levels restricted to info, warning, and error in production
- Debug logs enabled selectively for development or issue resolution
- Separate workloads for easier issue detection
- Distributed tracing for complex applications

---

## Knowledge Sharing

- Regular pairing and open communication are preferred over siloed work
- Working in isolation is draining and increases risk — pull in another participant when stuck or uncertain
- Meeting notes with third parties or in contract discussions are committed to a centralized log
- Retrospectives happen regularly — cadence determined by the team and the nature of the work

---

---

## Technical Standards Reference

For detailed technical standards — language-specific guidelines, commit conventions, security baselines, and similar — refer to the team standards document. This document captures working practice. That document captures technical specification.

---

## Related Documents

- Operating Agreement — governance layer
- Roles — participant roles and decision authority
- Workstation Configuration — local environment setup reference
- Team Standards — technical baseline and specifications

*First drafted: February 2026*
