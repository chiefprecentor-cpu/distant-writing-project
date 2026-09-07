# AGENTS

These instructions apply to the whole `distant-writing-project/` repository. A more specific `AGENTS.md` in a descendant directory adds to or overrides these instructions for that subtree.

## Repository Boundaries

- Treat the repository root as the working and integration boundary. Before editing a subtree, read its nearest `AGENTS.md` and relevant navigation file.
- `writer_os/` is the file-based authoring and persistent-context environment. Its `AGENTS.md` and `README.md` define the rules for that subtree.
- Do not extend Writer OS-specific restrictions, including Markdown-only work and its prohibition on automation, schemas, or Ren'Py implementation, to unrelated subtrees.
- Keep Ren'Py or other runtime implementation outside `writer_os/`. If an implementation subtree is introduced by an explicit task, use its native formats and give it local instructions when needed.
- `.codex/` contains repository-local Codex configuration. Do not change hooks, commands, external paths, or capture behaviour unless the task explicitly concerns that configuration.
- Agency-audit tooling and records referenced by hooks are external to this repository. Do not import them into Writer OS, treat them as story sources, or modify them during ordinary repository work.

## Writer OS Context Loading

- Whenever a task concerns `writer_os/`, read `writer_os/AGENTS.md` before analysing or editing files, even when Codex was started from the repository root.
- After context compaction or other context loss, if the active task still concerns `writer_os/`, reread `writer_os/AGENTS.md` before continuing and follow its current-work loading instructions.
- Read `writer_os/README.md` when orientation to the Writer OS structure is needed.
- Read `writer_os/docs/project_brief.md` when assessing or changing Writer OS purpose, scope, non-goals, or architecture.
- Read `writer_os/docs/operating_principles.md` when work concerns authority, uncertainty, human-AI responsibilities, candidates, derived views, evidence, or cross-layer design.
- Do not load these supporting documents for an ordinary local writing task unless the decision depends on them.

## Working Rules

- Make the smallest change that completes the requested task. Preserve existing structure and style; do not add speculative features, abstractions, directories, indexes, or schemas.
- Distinguish discussion, candidate material, confirmed creative decisions, implementation, and research evidence. Do not silently promote or copy material across those boundaries.
- Human confirmation, not file location or agent inference, determines creative authority. If status is unclear, label material as a candidate, question, or TBD rather than inventing facts.
- Do not silently overwrite or normalise human-authored final text, protected revisions, research records, or project configuration.
- Load and edit only the context relevant to the task. Private material outside the repository requires explicit relevance and permission.
- For cross-subtree work, identify the source of truth and intended destination before copying or translating material. Prefer links or an explicit handoff over competing primary copies.
- Treat Writer OS summaries as navigation aids, not executable game truth. Any future implementation bridge must use the relevant drafts, confirmed presentation decisions, and confirmed story state.

## Completion

- Run checks appropriate to the files changed, when available.
- Report what changed, any checks performed, remaining uncertainty, and any cross-boundary or semantic consequence introduced by the work.
