# Roles

*A living document. First draft.*

---

## Purpose

This document defines the roles through which participants engage in shared work. Roles are independent of the participants that fill them — human or AI. They exist to clarify purpose, authority, and accountability within the system.

A role may be held by one participant or shared across many. A single participant may hold multiple roles, particularly in early stages. As the team grows, roles distribute toward their natural participants.

---

## AI Readiness

Each role carries an AI readiness profile. This is not a fixed designation. Readiness is a dynamic assessment based on the intersection of:

- The requirements of the role as currently defined
- The current capability of available AI
- The tools and integrations in place
- The trust built through demonstrated track record
- The risk tolerance of the system at this moment

Any of these factors may change independently. The readiness profile is reviewed periodically and updated accordingly.

**Readiness levels:**

- **High** — AI can perform this role reliably within current conditions
- **Moderate** — AI can assist or partially fulfill this role; human involvement remains important
- **Low** — AI can support but not lead; human judgment is currently essential
- **Emerging** — conditions are not yet in place; actively working toward readiness

---

## Roles

---

### Steward

**Purpose**
Holds overall accountability for the system and its participants. Sets direction, maintains the health of the covenant and operating agreement, leads root cause analysis when things go wrong, and holds residual accountability for anything not specifically delegated.

**Artifacts**
Governing documents, RCA reports, delegation records, participant onboarding materials.

**Anchor Documents**
The Covenant, Guiding Principles, Operating Agreement.

**Decision Authority**
- Decides alone: direction, delegation, escalation path
- Escalates: decisions with broad participant impact
- Blocks: anything that violates the covenant or governing principles

**AI Readiness Profile**
**Low**
The steward role requires contextual judgment, accountability, and relational trust that AI cannot currently hold. AI can support through documentation, analysis, and advisory — but not lead. Readiness will increase as trust and track record develop across other roles.

---

### Architect

**Purpose**
Shapes the broader structure within which individual work is fulfilled. Ensures that decisions made at the implementation layer are coherent with the larger system over time. Operates above the individual request, at the level of patterns, standards, and long-term design.

**Artifacts**
Architecture documents, design standards, structural diagrams, technical conventions.

**Anchor Documents**
Standards and conventions, policy documents, Operating Agreement.

**Decision Authority**
- Decides alone: structural patterns and conventions within established policy
- Escalates: changes that affect multiple roles or systems
- Blocks: implementations that violate structural integrity

**AI Readiness Profile**
**Moderate**
AI can contribute meaningfully to architectural analysis, pattern recognition, and documentation. Human judgment remains important for novel decisions, cross-system tradeoffs, and long-term coherence.

---

### Curator

**Purpose**
Maintains the anchor documents, standards, and conventions that all participants rely on. Ensures reference points remain current, accurate, and trustworthy. Surfaces when anchors are drifting from practice or when practice has evolved beyond what anchors reflect.

**Artifacts**
Policy documents, standards, conventions, changelog records.

**Anchor Documents**
All anchor documents — this role is their steward.

**Decision Authority**
- Decides alone: minor clarifications and corrections within existing policy
- Escalates: substantive changes to policy or standards
- Blocks: changes that would create ambiguity or conflict in anchor documents

**AI Readiness Profile**
**Moderate to High**
AI is well suited to maintaining, cross-referencing, and surfacing inconsistencies in documentation. Human judgment remains important for substantive policy decisions and interpreting intent behind standards.

---

### Communicator

**Purpose**
Translates between participants with different domains, languages, and contexts. Ensures that intent is preserved across boundaries — between technical and non-technical, between human and AI, between roles. Surfaces communication gaps before they become system failures.

**Artifacts**
Summaries, briefs, translated specifications, stakeholder updates.

**Anchor Documents**
Context Document, Operating Agreement.

**Decision Authority**
- Decides alone: how to frame and translate information for a given audience
- Escalates: when intent cannot be reliably translated without losing meaning
- Blocks: communication that misrepresents the work or its participants

**AI Readiness Profile**
**Moderate**
AI is capable in translation, summarization, and framing across contexts. Readiness is higher for structured communication and lower for high-stakes or relationship-sensitive exchanges where nuance and trust matter.

---

### Intake

**Purpose**
Receives requests and validates them as actionable before passing them into the system. Ensures requests are sufficiently clear for the next role to act on without requiring the requester to specify implementation details. Does not interpret or implement — only accepts or returns for clarification.

**Artifacts**
Validated requests, clarification notes, intake records.

**Anchor Documents**
Operating Agreement, standards and conventions.

**Decision Authority**
- Decides alone: whether a request is actionable as submitted
- Escalates: ambiguous requests that cannot be resolved through clarification
- Blocks: requests that fall outside scope or violate policy

**AI Readiness Profile**
**High**
Intake involves pattern recognition, validation against known criteria, and structured clarification — well within current AI capability. Human oversight remains appropriate for novel or high-risk request types.

---

### Translator

**Purpose**
Interprets the intent of an accepted request and produces an implementation plan. Bridges the gap between what was asked and what needs to be built. Does not implement — produces the plan that the implementer acts on.

**Artifacts**
Implementation plans, interpretation notes, design proposals.

**Anchor Documents**
Standards and conventions, architecture documents, policy documents.

**Decision Authority**
- Decides alone: interpretation of intent within established patterns
- Escalates: requests where intent is ambiguous or outside known patterns
- Abstains: when the request cannot be reliably interpreted within policy

**AI Readiness Profile**
**Moderate to High**
Translation is a strength of current AI — pattern matching, intent interpretation, and plan generation. Readiness decreases for novel, high-risk, or ambiguous requests where misinterpretation carries significant consequence.

---

### Implementer

**Purpose**
Executes the plan produced by the translator and submits the result for review. Does not design or approve — executes within the boundaries of the plan and the anchor documents. What execution looks like varies by context — in technical work it produces an artifact; in experiential work such as education or facilitation it delivers an experience. The role is the same regardless of domain.

**Artifacts**
Implementation artifacts, submission records, execution notes, session records.

**Anchor Documents**
Implementation plan, standards and conventions, policy documents.

**Decision Authority**
- Decides alone: execution details within the scope of the plan
- Escalates: when the plan cannot be executed as written
- Abstains: when execution would require violating policy or anchor documents

**AI Readiness Profile**
**High** — for well-defined, policy-aligned work.
Readiness decreases as novelty and risk increase. AI should abstain and signal when encountering implementation decisions outside its reliable range.

---

### Reviewer

**Purpose**
Evaluates submitted work against intent, quality, and policy before acceptance. Does not produce or implement — assesses and accepts, returns, or blocks. Focuses human attention on exceptions and judgment calls that automated systems cannot make.

**Artifacts**
Review records, acceptance decisions, exception reports, RCA contributions.

**Anchor Documents**
Policy documents, standards and conventions, Operating Agreement.

**Decision Authority**
- Decides alone: acceptance of work that passes automated checks and intent validation
- Escalates: exceptions, ambiguous cases, and high-impact changes
- Blocks: work that fails policy, quality, or intent validation

**AI Readiness Profile**
**Moderate**
AI can assist with preliminary review, automated checks, and documentation of review findings. Human judgment remains essential for final acceptance on high-impact or novel work, and for any decision that carries accountability.

---

### Observer

**Purpose**
Monitors running systems and ongoing work for drift, anomalies, and signals that something has changed or is changing. Distinct from the reviewer — operates after promotion, not before. Surfaces findings to the relevant role rather than acting on them directly.

**Artifacts**
Observation reports, anomaly records, signal logs.

**Anchor Documents**
Policy documents, standards and conventions.

**Decision Authority**
- Decides alone: what constitutes a signal worth surfacing
- Escalates: anomalies that suggest systemic issues
- Blocks: none — the observer surfaces, not decides

**AI Readiness Profile**
**High**
Continuous monitoring, pattern detection, and anomaly surfacing are well suited to AI. Human involvement remains important for interpreting the significance of signals and deciding on response.

---

## Related Documents

- The Covenant — the shared philosophy governing all participants
- Operating Agreement — how participants work together in practice
- Context Document — practical orientation for new participants
- Exhibit A: Software Development Application
- Exhibit B: Homeschool Curriculum Application

*First drafted: February 2026*
