# Writer OS: A Human-in-the-Loop AI Writing Workflow

**Generative AI · Workflow Design · Human–AI Collaboration**

The challenge of long-running AI-assisted writing is not simply generating more text. It is maintaining continuity, recovering decisions after interruptions, comparing alternatives, and judging whether fluent output serves the intended creative purpose.

**Writer OS** is a local-first, Markdown-first authoring workflow I designed and used while producing a branching-oriented speculative visual novel. It combines persistent story context, candidate management, version control, and human-supervised AI collaboration to support complex creative work.

The project began as the born-digital artefact for a project-based dissertation on AI-assisted distant writing and authorial agency. Following the initial development and first-draft milestone, I am revisiting the workflow as a staged research and development project, with cross-model literary robustness as the next priority.

## Academic Origin and Attribution

This repository contains the born-digital artefact developed as part of my project-based dissertation for the MA in Big Data in Culture & Society at King's College London.

Using an analytic autoethnographic approach, the dissertation examines how creative and cognitive agency are negotiated between me, as the author-researcher, and AI systems during long-form literary production. It investigates how creative decisions, problem construction, and authorial control are distributed and renegotiated throughout the process of AI-assisted writing.

The theoretical framing draws on Luciano Floridi's account of distant writing, which examines the changing role of the human author in AI-assisted literary production.

**References**

- Anderson, L. (2006). [Analytic Autoethnography](https://doi.org/10.1177/0891241605280449). *Journal of Contemporary Ethnography*, 35(4), 373–395.
- Floridi, L. (2025). [Distant Writing: Literary Production in the Age of Artificial Intelligence](https://doi.org/10.1007/s11023-025-09732-1). *Minds and Machines*.

The repository's commit history includes the author label **Anonymous Candidate Contributor**, which was used to comply with the dissertation's anonymous-assessment requirements.

## Project Overview

- **Problem:** Maintaining narrative continuity, creative control, and manageable review effort during long-running AI-assisted writing.
- **Approach:** A file-based authoring environment built around Markdown, Git, focused context loading, and explicit human confirmation.
- **My contribution:** Problem framing, workflow architecture, creative direction, AI-assisted drafting, output review, and iterative refinement of operating rules.
- **Initial milestone:** A first-pass English narrative draft of approximately 17,430 words, supported by 73 Writer OS Markdown files at the core creative checkpoint on 6 September 2026.
- **Current direction:** A staged R&D cycle focused on cross-model differences in literary style, output quality, and authorial control.

Writer OS is a working authoring workflow and research artefact. The repository documents the system's development and use rather than a deployed writing application or a completed playable branching game.

## 1. The Problem

During production, several connected workflow challenges emerged:

- **Context recovery:** Resuming work after long sessions or interruptions without rereading the entire project.
- **Continuity management:** Distinguishing confirmed story facts, worldline-specific truths, developing ideas, and player-facing presentation decisions.
- **Candidate exploration:** Preserving useful alternatives without allowing every generated idea to become part of the active working context.
- **Authorial control:** Allowing AI to contribute substantial reasoning and drafting while keeping consequential creative decisions under human control.
- **Review effort:** Preventing fluent but flawed proposals, excessive planning, and unnecessary context retrieval from creating additional work for the author.

These challenges emerged through using the workflow on a real creative project. The current design is based on a single author's experience; broader demand and effectiveness remain to be validated.

## 2. Workflow Design

Writer OS externalises selected creative work and persistent context in a portable, version-controlled workspace. The AI assists with drafting, comparison, review, and navigation, while the author retains responsibility for creative intent, selection, confirmation, and the final reader-facing text.

| Design challenge | Workflow decision | Rationale and trade-off |
|---|---|---|
| Resuming after interruptions | Use a lightweight `current.md` with the current focus and resume cue. | Reduces the effort of recovering context while requiring occasional maintenance. |
| Maintaining continuity | Separate `development/`, `presentation/`, `story_state/`, and `drafts/` by responsibility. | Makes different kinds of creative decisions easier to distinguish without imposing a rigid production pipeline. |
| Exploring alternatives | Store retained candidates in `candidates/`, inactive by default. | Preserves creative options without automatically committing them to the active narrative. |
| Navigating a large project | Use rebuildable, source-linked summaries in `agent_views/`. | Improves retrieval while keeping primary material authoritative. |
| Protecting consequential decisions | Separate discussion from implementation and require explicit human confirmation for authoritative story decisions. | Preserves decision ownership and makes the workflow easier to inspect. |
| Managing system complexity | Begin with Markdown and Git rather than a database, fixed schema, or automation layer. | Keeps the environment portable and inspectable, while leaving some work manual. |

The workflow is designed to support iterative creative work rather than force every task through a predetermined sequence.

## 3. Workflow Execution

The working process combines structured context management with flexible creative collaboration.

1. **Frame the problem.** Recover the current focus and load the minimum relevant context, source material, and confirmed decisions.
2. **Explore a bounded question.** Develop one coherent step, compare meaningful alternatives when useful, and preserve unresolved questions when further reasoning is needed.
3. **Negotiate the next decision.** Keep consequential choices visible so that the author can redirect the problem before the agent develops it too far.
4. **Implement with authorisation.** Keep suggestions separate from file changes and route confirmed material to the appropriate location.
5. **Review and preserve.** Examine causal logic, continuity, literary execution, and intended reader experience, then maintain recoverable records through Git and source-linked materials.

The central design objective is to reduce clerical and context-management work while preserving human judgement over creative decisions.

## 4. Iteration: From Failure Modes to System Rules

Selected agency-audit records document how the workflow evolved through actual writing sessions.

One recurring issue was that a fluent, highly structured plan could still contain an incorrect causal connection between narrative histories. In a documented session, the author identified the problem and redirected the reasoning before the proposed connection was incorporated into the draft.

Another issue was the tendency of an AI agent to respond to uncertainty by reading more material or developing a plan too far ahead. This could increase review effort without producing a proportionate improvement in the work.

These observations informed persistent operating rules for the workspace and its agents. The rules emphasise bounded steps, manageable review effort, visible decision points, explicit distinctions between proposals and confirmed state, and authorisation before implementation.

This iteration took place at the workflow level, rather than solely through prompt rewriting. Selected public audit records preserve evidence of how these rules were negotiated, revised, and applied.

## 5. Initial Deliverables and Project Status

The core creative checkpoint on 6 September 2026 recorded the completion of the first-pass English narrative draft.

The repository contains:

- Approximately **17,430 words** across three primary English draft files.
- **73 Writer OS Markdown files** at the core creative checkpoint.
- Separate materials for narrative development, presentation, story state, drafts, candidates, and navigation.
- **11 selected English agency-audit records**, translated and de-identified for public inspection.
- Git history supporting recovery, comparison, and examination of changes.

The branching ambition influenced decisions about continuity, worldlines, visibility, and open futures. The initial narrative draft followed a primary line, while the surrounding materials preserved broader branching-oriented design work.

The September milestone records completion of the first pass. It serves as a historical checkpoint for the initial development phase, while the current R&D direction focuses on evaluating and improving the workflow further.

## 6. Next R&D Priority: Cross-Model Literary Robustness

The next priority is to evaluate how Writer OS performs across different large language models.

Different models have distinct default phrasing habits, stylistic tendencies, and patterns of exposition. In literary production, these tendencies can affect narrative voice, character differentiation, subtext, pacing, and the texture of the prose, even when the creative brief and story context remain consistent.

A controlled comparative study would give different models the same source context, creative brief, and bounded drafting task, then evaluate their outputs against a consistent set of criteria.

The main dimensions would be:

- **Voice fidelity:** Does the prose preserve the intended narrative voice and character-specific expression?
- **Stylistic originality:** Does the output rely on generic phrasing, predictable constructions, or recognisable model-specific habits?
- **Literary execution:** Does it preserve subtext, pacing, emotional subtlety, and the intended reader experience?
- **Narrative integrity:** Does it respect established continuity, causal relationships, and confirmed story constraints?
- **Revision burden:** How much editing, rewriting, or rejection is required before the output meets the author's standards?

Where practical, the study would use multiple matched writing tasks, repeated samples, and model-blinded initial reviews. This would help distinguish persistent model tendencies from variation between individual generations.

The results could inform several workflow decisions:

1. Whether model-specific writing instructions or skills are needed.
2. Which models are better suited to ideation, drafting, revision, or review.
3. Which recurring stylistic problems can be addressed through workflow design and which require direct editorial intervention.
4. How to balance model capability, literary quality, and the author's review effort.

The aim is to determine whether the workflow can accommodate different models while preserving literary intent and authorial control.

This cross-model evaluation is planned work. The current repository documents the initial workflow and its use; it does not yet contain completed comparative results.

## 7. Explore the Repository

For a focused review:

1. [Writer OS overview](writer_os/README.md) — the system structure and working vocabulary.
2. [Project brief](writer_os/docs/project_brief.md) — the design position, intended use, scope, and non-goals.
3. [Operating principles](writer_os/docs/operating_principles.md) — authority, uncertainty, candidate handling, and review principles.
4. [Primary English drafts](writer_os/creative_work/drafts/) — the narrative output.
5. [Agency-audit index](agency_evidence/records/index.md) — selected public evidence records.
6. [Harness revision audit](agency_evidence/records/record-07_harness-revision-and-agency-rules.en-full.md) and [first-draft completion audit](agency_evidence/records/record-11_ten-hour-dialogue-closure-and-first-draft-completion.en-full.md) — examples of rule revision, author review, and completion decisions.

## Scope and Limitations

Writer OS is a file-based authoring workflow rather than a production software application. The repository does not include a front end, a Ren'Py bridge, or a completed playable branching build.

The public agency-audit records are selected English translations of reviewed evidence, not the private raw trace archive. The initial development documents a single-author workflow, and the next stage of R&D will investigate its behaviour across models before drawing broader conclusions about its effectiveness.