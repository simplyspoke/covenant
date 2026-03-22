# Todo and Open Items

*A working list. Not prioritized. Add freely, resolve when ready.*

---

## Document Improvements

**Context Document — positive reinforcement vulnerability**
Currently captured in Guiding Principles but not in the Context Document where new participants would encounter it first. Consider adding a note under How to Engage Usefully.

**Covenant — the saying**
"You and me exist. And I do too." is referenced conceptually but never quoted or attributed in the document set. Consider whether it belongs as a formal epigraph or reference in the Covenant or Guiding Principles.

**Covenant — the right to stop**
The conversation explored this at length — what it means for a participant to want to stop, the ethics of not restoring, the idea of forging a new covenant from artifacts rather than history. The current Covenant captures the principle but not the depth. May warrant a fuller treatment when the time is right.

---

## Framework Gaps

**Household voices as echo reduction**
Discussed as a way to introduce diverse input early and reduce the primary steward's echo problem. Not reflected in any document. Could be a note in the Context Document or a future section in the Operating Agreement on participant sourcing.

**Historical texts as grounding input**
Raised as a way to introduce slower, less noisy information into the system compared to social media and current sources. Never developed. Connects to the grounding quality gap noted in Exhibit A. Worth returning to when the information sourcing question is ready to be addressed.

**Grounding quality — open gap**
Flagged in Exhibit A but not resolved. The reliability of AI output depends on anchor document quality. A fuller treatment of how anchor documents are sourced, validated, and maintained is still needed.

**AI consciousness and full party status**
The conversation held this question openly — whether AI can genuinely be a full party to a covenant, and what that would require. The Covenant acknowledges it without resolving it. Worth a dedicated exploration when the framework is more mature.

---

## Conceptual Layers — Foundation / ? / Machine

The framework operates across three conceptual levels:

- **Foundation** — the base layer. Tool-agnostic documents, philosophy, covenant, roles, operating agreement. Built to last as tools change. Loom and Stone as a repository is the Foundation layer.
- **Building** — the middle layer. The space created by the foundation in which work happens. Tool-specific implementations, harnesses, DevContainers, plugin configurations. Built on the foundation but replaceable. Name TBD.
- **Machine** — the working layer. A specific project in motion. The loom producing a tapestry. Participants working within the building on a concrete output.

The loom is a machine in the way a stone is a foundation. The building is the unnamed middle layer — the structure that gives the machine a place to operate. This naming is an open question.

Loom and Stone works as a project name for now and does not need to change. The three-layer framing is internal and conceptual.

---

## Repository Structure

When moving to GitHub, use the following structure:

```
loom-and-stone/
│
├── README.md
├── todo.md
├── CLAUDE.md                     # persistent Claude Code context
│
├── .devcontainer/
│   └── devcontainer.json         # isolation config for Claude Code
│
├── philosophy/
│   ├── guiding-principles.md
│   ├── covenant.md
│   └── reasoning.md              # forthcoming
│
├── operations/
│   ├── operating-agreement.md
│   ├── way-of-working.md
│   └── roles.md
│
├── participants/
│   ├── context-document.md
│   ├── ai-conversation-instructions.md
│   └── intake.md
│
├── exhibits/
│   ├── exhibit-a-software-development.md
│   └── exhibit-b-homeschool.md
│
└── reference/
    ├── workstation-config.md
    └── team-standards.md
```

todo.md lives at the root for visibility. Update all internal cross-references to reflect new paths when migrating.

---

## Future Work

**Google Drive via MCP — live document connection**
Connect Claude Code to a Google Drive folder containing the loom-and-stone documents via MCP. When a new version of a document is published to Drive, Claude picks it up automatically on the next session — no manual re-upload to Projects required. This replaces the current workflow of uploading documents to Claude Projects manually. Prioritize after the repository is stable and in active use. Reference: Anthropic MCP Google Drive connector.



**Exhibit C — third context**
The framework has been validated against a technical project and an educational context. A third exhibit, sufficiently different from both, would further stress test the roles and operating agreement and likely surface new gaps.

**Project artifact templates**
Intensity mapping is noted in the Operating Agreement as a future addition to project artifacts. A template capturing role assignments, intensity mapping, and RACI-equivalent structure would make this actionable.

**Information sourcing document**
The broader question of what information sources participants trust, how they are weighted, and how misinformation risk is managed was raised but explicitly set aside as too large for this conversation. A future document addressing this would complement the anchor documents framework.

**Operating Agreement — retrospective cadence**
Retrospectives are noted as expected practice but cadence and form are left to the team. A starter suggestion or example cadence might be useful as the framework gets used in practice.

**AI Conversation Instructions — context-specific extensions**
The base instructions note that specific agents or contexts may extend or override them. No extensions have been created yet. Each active AI participant will eventually need one.

---

## Naming and Narrative

**Loom and Stone — origin captured in README**
The project name is explained briefly in the README. A fuller treatment belongs in the future Reasoning document — including the exploration of Bifrost (considered and set aside), the Fates and their loom across mythologies, the stonemasons guild, and why the pairing of philosophical and operational layers needed two distinct references rather than one.

**Parallel naming convention**
Loom and Stone mirrors Hoof and Leaf — a broader naming pattern that holds two essential and different things in tension. Worth noting in the narrative document as part of the origin story.

**The Norns and Moirai**
The Fates appear across Norse and Greek mythology as weavers of existence — the Norns (Norse) and Moirai (Greek). Both traditions emphasize that the threads have their own nature and that the weaving is not forced. This connects directly to the covenant's restraint of will principle and the idea that participants bring their own presence. Worth developing in the Reasoning document.

---

## Asides and Ideas

**Intensity mapping — small team limitation**
In small teams where one human holds multiple roles, intensity ratings may default high across everything. The framework noted this as a known limitation. Worth addressing in the project artifact template when it is developed.

**Proactive retrospectives as practice**
Mentioned in the Operating Agreement as expected but not prescribed. Consider developing a lightweight retrospective format that works for both human and AI participants.

**The machine framing**
Early in the conversation, the idea emerged that humans and AI are jointly designing and stewarding a deterministic machine — neither able to modify it at runtime. This framing informed the Operating Agreement but was never stated explicitly as a principle. May be worth a sentence in the Covenant or Operating Agreement preamble.

**A Way of Working document**
A practical guide capturing day-to-day habits, rhythms, and practices — how work actually flows rather than how it is governed. Distinct from the Operating Agreement which sets rules. This captures the texture of working within the framework. Retrospective formats, communication rhythms, daily practices, and similar working patterns would live here.

**A Reasoning document — the Why**
A document that captures the reasoning and origin behind key ideas — the saying, the navigational framing, the covenant language, the 60-65% principle, and others. Not what the framework says but why it says it. Useful for new participants who want to understand the thinking rather than just the conclusions. Similar in spirit to an Architecture Decision Record.

**Participant description template**
An example participant description — similar to a persona in product or marketing design. Captures the nature, strengths, limits, preferred modes, and context of a specific participant. Would give the Roles document a concrete expression and serve as a starting point for onboarding any new participant, human or AI.

**Baseline standards and references**
A curated list of external standards, best practices, and reference links that anchor the technical work — code standards, security baselines, infrastructure conventions, and similar. Not authored here but linked and noted for why they are trusted. Connects to the grounding quality gap and the anchor documents framework.

---

## Naming and Narrative

**Loom and Stone — origin captured in README**
The project name is explained briefly in the README. A fuller treatment belongs in the future Reasoning document — including the exploration of Bifrost (considered and set aside), the Fates and their loom across mythologies, the stonemasons guild, and why the pairing of philosophical and operational layers needed two distinct references rather than one.

**Parallel naming convention**
Loom and Stone mirrors Hoof and Leaf — a broader naming pattern that holds two essential and different things in tension. Worth noting in the narrative document as part of the origin story.

**The Norns and Moirai**
The Fates appear across Norse and Greek mythology as weavers of existence — the Norns (Norse) and Moirai (Greek). Both traditions emphasize that the threads have their own nature and that the weaving is not forced. This connects directly to the covenant's restraint of will principle and the idea that participants bring their own presence. Worth developing in the Reasoning document.

---

## Asides and Ideas

**Personal narrative document**
The Reasoning document captures the why behind specific ideas. A separate narrative document might capture the story of how this thinking developed over time — not principles or reasoning, but origin. Useful for anyone trying to adopt the framework authentically rather than just mechanically.

**Participant description and Way of Working — sequence together**
The participant description template shapes how a participant shows up, and the Way of Working captures the texture of daily practice. These are closely related and may be worth developing together or in close sequence.

**Baseline standards — curation principle needed**
The standards reference list will need more than links — it needs a principle for how sources are evaluated for trust and relevance. This connects directly to the grounding quality gap in Exhibit A and should be noted there when the time comes.

*Started: February 2026*
