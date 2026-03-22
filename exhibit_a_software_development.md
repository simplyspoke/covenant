# Exhibit A: Software Development Application

*Tabletop exercise. Validates the Roles and Operating Agreement against a real project context. First draft.*

---

## Context

This exhibit applies the framework to an Internal Developer Platform with AI-Assisted Provisioning and Policy Enforcement. Developers request infrastructure through a service catalog. An AI participant translates intent into infrastructure code. Human platform engineers retain authority over policy definition, guardrails, and final promotion into production environments.

This is an early-stage project. One human currently holds multiple roles. The system is designed to distribute those roles over time as the team and trust develop.

---

## How the Framework Maps

### How Work Enters the System

Developers submit requests as markdown documents. The format is intentionally flexible — requests may range from a brief functional need to a full architectural specification. This keeps the system adaptive to unforeseen needs and avoids reliance on a fixed capability catalog.

Requests describe function, feature, or need — not implementation. The developer stays in their domain. The system translates across the boundary.

### Layers and Roles in This Context

| Layer | Role | Current Participant | Notes |
|---|---|---|---|
| Intake | Intake | AI | Validates request as actionable, returns for clarification if needed |
| Translation | Translator | AI | Interprets intent, produces Terraform or CloudFormation plan |
| Implementation | Implementer | AI | Executes plan, submits PR — does not promote |
| Review | Reviewer | Human (Platform Engineer) | Validates intent alignment, reviews AI plan, confirms automated checks passed |
| Promotion | Steward | Human (Platform Engineer) | Final sign-off, promotes to production |

The Architect, Curator, Observer, and Communicator roles exist but are currently absorbed by the primary steward. These are transitional states, not permanent designs.

### Anchor Documents in This Context

- Infrastructure policy documents
- Security and compliance standards
- Terraform and CloudFormation conventions
- This operating agreement and the covenant

The AI participant treats these as priority reference points. Patterns that develop over time are acceptable within them. Patterns that violate them trigger a signal.

---

## Signal Standard in Practice

### AI Translator — Example Signals

**Proceed** — request is within known patterns, intent is clear, plan is produced within policy.

**Pause** — request references a service or pattern the translator has not encountered. Surfaces the specific gap to the intake role before producing a plan.

**Escalate** — request involves cross-system dependencies or architectural decisions outside the translator's authority. Hands off to the Architect role with context.

**Abstain** — request cannot be reliably interpreted within policy. Translator withdraws, signals clearly, and the human reviewer navigates next steps.

### Human Reviewer — Example Signals

**Proceed** — automated checks passed, intent aligns with implementation, no exceptions flagged.

**Pause** — automated checks passed but something in the implementation does not feel right. Reviewer stops before acceptance and surfaces the concern.

**Escalate** — change has broader architectural impact than the reviewer can assess alone. Escalates to steward or architect.

**Abstain** — reviewer does not have sufficient domain knowledge to review a specific change reliably. Signals and routes to a more appropriate participant.

---

## Review and Approval in This Context

Review is risk-proportional:

- **Known infrastructure patterns within policy** — automated security scans, policy checks, and linting pass; human reviewer confirms and accepts with lightweight oversight
- **Novel or ambiguous requests** — greater human involvement, explicit intent validation, possible return to translator for clarification
- **Destructive actions** — permission changes, resource deletion, production modifications — maximum review, explicit steward sign-off required

Automated deterministic systems handle policy compliance and security scanning. The human reviewer focuses on what automation cannot catch — intent alignment, contextual judgment, and exceptions.

---

## Accountability in This Context

Accountability is systemic. When a misconfiguration or security gap occurs, a root cause analysis is conducted to understand how the system allowed it — not to assign individual blame.

The primary steward leads the RCA with AI assistance in documentation and analysis. All relevant participants and stakeholders review the findings. Recommendations result in systemic changes — to policy, guardrails, anchor documents, or process.

The primary steward holds residual accountability for anything not specifically delegated.

---

## AI Readiness Assessment

| Role | Current Readiness | Notes |
|---|---|---|
| Steward | Low | Held by human; AI supports through documentation and advisory |
| Architect | Moderate | AI contributes to analysis and documentation; human judgment leads structural decisions |
| Curator | Moderate to High | AI well suited to maintaining and cross-referencing policy docs |
| Communicator | Moderate | AI handles structured translation; human judgment for stakeholder relationships |
| Intake | High | Pattern recognition and validation within current AI capability |
| Translator | Moderate to High | Strong AI capability; readiness decreases for novel or high-risk requests |
| Implementer | High | Well-defined, policy-aligned execution; AI abstains when outside reliable range |
| Reviewer | Moderate | AI assists with preliminary review; human holds final acceptance authority |
| Observer | High | Continuous monitoring and anomaly surfacing well suited to AI |

---

## Gaps and Open Questions

The following were identified during the tabletop exercise and remain unresolved:

- **Grounding quality** — the reliability of AI output depends on the quality of anchor documents. If policy documents are incomplete or ambiguous, AI readiness across all roles decreases. Maintaining anchor document quality is a prerequisite, not an assumption.
- **Novel pattern handling** — the system has growing confidence in known patterns. Novel requests carry higher risk until the system has built track record. The threshold for escalation versus abstention in novel cases needs further definition.
- **Multi-participant review** — as the team grows and review is shared across participants, coordination between reviewers needs a defined approach to avoid gaps or duplication.

---

## Related Documents

- Roles — role definitions and AI readiness profiles
- Operating Agreement — the framework this exhibit validates against
- The Covenant — the shared philosophy governing all participants
- Exhibit B: Homeschool Curriculum Application *(forthcoming)*

*First drafted: February 2026*
