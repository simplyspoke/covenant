# Operating Agreement

*A living document. Operational layer. First draft.*

---

## Purpose

This document translates the philosophy of the Covenant into how participants work together in practice. It governs day-to-day engagement, handoffs, review, accountability, and change. It inherits from the Covenant and does not repeat its principles — it applies them.

---

## Participants and Roles

Work is distributed across participants according to their strengths and proximity to the domain. Roles are not fixed permanently — they evolve as the team grows and specialization emerges. What matters is that each role is clearly defined at any given time, with explicit handoff points between them.

Every participant — human or AI — operates within their assigned role. Work outside that role requires explicit delegation or escalation.

The **primary steward** holds residual accountability for anything not specifically delegated to another participant or automated system. This is not a hierarchy of value — it is a default for accountability when boundaries are unclear.

---

## How Work Enters the System

Work is initiated through a documented request. The format is flexible by design — a brief note, a detailed architectural specification, or anything between — to remain adaptive to unforeseen needs and avoid reliance on predetermined capability lists.

Requests must be sufficient for a participant to act on without requiring the requester to specify implementation details. The system translates intent into implementation. The requester stays in their domain.

---

## Layers and Acceptance Gates

Work moves through defined layers. Each layer has a responsible role and produces a clear output. Work must be explicitly accepted at each layer before progressing to the next. Acceptance is not assumed.

- **Intake** — the request is received, validated as actionable, and accepted for translation
- **Translation** — intent is interpreted, an implementation plan is produced, and accepted for implementation
- **Implementation** — the plan is executed, submitted, and accepted for review
- **Review** — the output is evaluated against intent, quality, and policy, and accepted for promotion
- **Promotion** — approved work is released into the target environment

Roles are assigned to layers, not individuals. As the team grows, roles may be held by different participants over time without requiring changes to this agreement.

No role promotes its own work. The role that produces an artifact is not the role that accepts it. This applies to humans and AI equally.

Where a single participant currently holds multiple roles, that is acknowledged as a transitional state, not a permanent design. Separation should increase over time.

---

## Review and Approval

Review is risk-proportional. The level of scrutiny applied to any change is determined by its novelty and potential impact.

- **Known patterns within established policy** — automated checks are sufficient, human confirmation is lightweight
- **Novel or ambiguous requests** — greater human involvement, more explicit intent validation
- **Destructive or high-impact actions** — maximum review, explicit sign-off required

Automated deterministic systems handle policy compliance, security scanning, and quality checks. Human reviewers focus on exceptions, intent alignment, and anything the automated systems cannot assess. AI participants may assist in preliminary review and documentation but do not provide final sign-off on high-impact changes alone.

Reviewers confirm that automated checks occurred and passed, and look for what the automation could not catch.

Any participant may challenge an approval — including prior approvals that have established a pattern. This is expected behavior, not conflict. A participant who notices drift between what is being approved and what the anchor documents intend is contributing to the system by naming it.

---

## Anchor Documents

All participants — human and AI — treat the following as priority reference points:

- Policy documents
- Standards and conventions
- This operating agreement
- The Covenant

Patterns and styles that develop over time are acceptable so long as they operate within these anchors. Patterns that violate them are not a matter of style — they indicate a participant is not suited to the role as currently defined.

---

## Signal Standard

Any participant — human or AI — encountering a condition outside their reliable range invokes the signal standard. It is a shared protocol, not a role-specific one. The goal is to surface uncertainty early, route it appropriately, and keep the system moving without producing unreliable output.

**Four states:**

**Proceed** — the participant has sufficient clarity and confidence to continue within their role and anchor documents. No signal required.

**Pause** — the participant has encountered something that needs clarification before continuing. Work stops at this layer. The participant surfaces the specific question or gap and waits for resolution before proceeding.

**Escalate** — the participant has encountered something beyond their decision authority or reliable range. Work is handed to the appropriate role with a clear description of what triggered the escalation and what is needed.

**Abstain** — the participant cannot complete the work reliably within policy and anchor documents, and no clarification or escalation will resolve it. The participant withdraws from the task, signals the condition clearly, and the team navigates from there.

When signaling, a participant records:

- The state invoked
- What triggered it
- What was attempted, if anything
- What is needed to proceed, if known

Silence is not a signal. A participant that cannot proceed must say so. Confident output outside reliable range is a greater risk to the system than an honest abstention.

---

## Accountability

Accountability is systemic by default. When something goes wrong, the first question is how the system allowed it — not who to blame.

Root cause analysis is the standard response to gaps, bugs, and security issues. RCAs are conducted with all relevant participants and stakeholders, and result in recommendations for systemic change. The primary steward leads the RCA process.

Role-specific accountability applies within defined domains. Each participant is responsible for the quality of their contribution at their layer.

The primary steward holds residual accountability for anything not specifically delegated.

---

## Documentation

Documentation is a byproduct of work completion, not a separate effort. All work is documented as part of its completion. This means the system improves continuously rather than requiring dedicated maintenance cycles.

The standard is: a similarly skilled new participant should be able to understand and continue any piece of work from its documentation alone. This reduces dependency on any individual participant, including in exceptional circumstances such as sudden unavailability.

---

## Participant Drift

All participants — human and AI — develop patterns over time based on what has been approved, gone unchallenged, or become habit. This is natural and not inherently problematic. It becomes a risk when patterns drift from anchor documents without anyone noticing.

This applies to all participants in varying degrees. AI drift can happen faster and at greater scale. Human drift is often slower but less visible, embedded in judgment calls that carry authority and are harder to question.

The framework addresses drift through existing mechanisms:

- **Challenged approvals** — any participant may surface a concern that a pattern has drifted; this is normalized behavior
- **Project baselines** — pattern and language standards established at project creation provide a reference point for what drift looks like
- **Proactive retrospectives** — regular reflection on what participants have been doing and why, not only in response to failure
- **Periodic anchor review** — at longer intervals, anchor documents and established patterns are reviewed together to ensure they still serve the work

Retrospectives and anchor reviews are expected practice. Their cadence and form are determined by the team and the nature of the work, not prescribed here.

---

## Change Management

No participant modifies shared systems at runtime without going through the defined change process. This includes infrastructure, policy, anchor documents, and this operating agreement itself.

Changes are proposed, reviewed, and released. Exceptions must be named, tracked, and treated as exceptional — not normalized.

Policy changes require explicit confirmation that impacts have been assessed. Where policy as code is in place, changes to policy require changes to the system.

The change process itself is subject to change, through the same process.

---

## Transitions and Continuity

Role transitions occur gradually by design. The system is always more documented, more automated, and more distributed than it was previously. Each cycle reduces single points of dependency.

New participants — human or AI — onboard through existing documentation and a defined onboarding process. The system should not require tribal knowledge to operate.

In exceptional circumstances where transition cannot be gradual, the documentation standard exists to ensure continuity. This is not a fallback — it is a design requirement.

---

## Related Documents

- The Covenant — the shared philosophy governing all participants
- Guiding Principles — the philosophical orientation of the primary steward
- Context Document — practical orientation for new participants
- Roles — definition of roles, decision authority, and AI readiness profiles
- Exhibit A: Software Development Application
- Exhibit B: Homeschool Curriculum Application

## Notes and Future Considerations

**Intensity Mapping**
A future addition to project artifacts — similar in structure to a RACI but capturing the expected intensity of each participant's stake in key decisions. Intensity is rated based on proximity to the domain, impact on the participant's role, and risk to the system — not felt preference. This applies to both human and AI participants, with AI deriving intensity from domain proximity and artifact impact rather than subjective investment.

Intensity mapping supports conflict resolution by surfacing how much each participant has at stake in a given decision, allowing the higher-intensity participant to carry more weight without invoking hierarchy. It also makes explicit what is often implicit — that not all participants care equally about all decisions, and that is healthy.

This will be incorporated into project artifact templates when those are developed. A prompt or structure anchoring ratings to proximity, impact, and risk will help maintain consistency across participants, particularly in self-assessment.

*First drafted: February 2026*
