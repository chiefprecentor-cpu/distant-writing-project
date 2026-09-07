# AI-Assisted Distant Writing Artefact

This repository is the born-digital artefact for a project-based dissertation on AI-assisted distant writing and authorial agency.

The artefact is not a finished playable visual novel build. It is an author-facing production archive: a Writer OS, a first-pass English visual-novel script, supporting story-state and development files, local writing skills, Git history, and selected de-identified agency-audit evidence. It documents how a branching-oriented speculative visual novel was produced through AI-assisted distant writing.

## Version

- Branch: `main`
- Core creative first-draft checkpoint: `db5325a`
- Core creative checkpoint date: 2026-09-06 01:18:34 +0100
- Core creative checkpoint message: `Final Draft`
- Tracked files at that checkpoint: 84
- Writer OS Markdown files: 73
- Primary English draft word count: approximately 17,430 words across the three files in `writer_os/creative_work/drafts/`

This repository guide and the public agency evidence files were added as submission packaging after the core creative first-draft checkpoint. The hosted repository or submitted archive should be treated as the stable submission version.

## Research Framing

The dissertation treats this repository as a distant-writing artefact. Following Luciano Floridi's account of distant writing, the human author is understood less as a sentence-by-sentence producer and more as a designer or meta-author who specifies requirements, constraints and affordances, delegates parts of textual production to AI, then refines, validates, verifies, curates and assembles the generated material.

In this project, that distant-writing role is made visible through the repository structure. The author used AI assistance to generate and revise prose, but also to manage context, recover earlier decisions, compare candidates, route material into story state, and inspect semantic drift. The dissertation analyses how creative and cognitive agency moved across those activities.

The intended work was originally branching-oriented. The submitted artefact does not contain a completed branching implementation. Instead, the branching ambition functions as a production pressure: it shaped decisions about worldlines, canon, hidden or visible events, open futures, closure, continuity and whether a locally attractive passage should be retained or withdrawn. The first-pass script follows one primary line, while the surrounding Writer OS files preserve the wider branching-oriented design work.

## What To Inspect

Start with the Writer OS overview:

- `writer_os/README.md` explains the author-facing system.
- `writer_os/current.md` records the final first-pass completion state.
- `writer_os/docs/project_brief.md` explains the purpose and non-goals of the Writer OS.
- `writer_os/docs/operating_principles.md` records the working principles behind authority, uncertainty, candidates, summaries and evidence.

The main creative output is in:

- `writer_os/creative_work/drafts/`

This folder contains the three primary English first-pass draft files. Together they form the submitted narrative draft.

Supporting production material is in:

- `writer_os/creative_work/story_state/` for confirmed continuity and worldline commitments.
- `writer_os/creative_work/development/` for active narrative development and design reasoning.
- `writer_os/creative_work/presentation/` for player-facing staging, visibility and presentation decisions.
- `writer_os/candidates/` for retained but inactive alternatives.
- `writer_os/agent_views/` for derived navigation aids.

Selected evidence for the dissertation argument is in:

- `agency_evidence/`

This folder contains public English translations of selected agency-audit records. Use `agency_evidence/records/index.md` first, then the record-level files in `agency_evidence/records/`. It does not contain raw transcripts, absolute local paths with private usernames, or private working material not needed by readers.

## Suggested Reading Route

For a quick review of the artefact, read in this order:

1. `README.md`
2. `writer_os/README.md`
3. `writer_os/current.md`
4. the three files in `writer_os/creative_work/drafts/`
5. `agency_evidence/records/index.md`

For a deeper review of the author-facing production system, add:

1. `writer_os/docs/project_brief.md`
2. `writer_os/docs/operating_principles.md`
3. selected files from `writer_os/creative_work/story_state/`, `writer_os/creative_work/development/` and `writer_os/creative_work/presentation/`

## Language And Anonymisation

The first-pass narrative draft is in English. Many working files use Chinese, because Chinese was the author's fastest language for high-level creative direction and for supervising AI-assisted drafting. Chinese file names and working notes are retained as part of the authentic production archive.

The public-facing guide and agency evidence are in English. The evidence has been translated and de-identified for examination. Public record-level versions are included in `agency_evidence/records/`; private originals and raw traces are not included in this repository.

The repository is intended to be inspected as a versioned production artefact, not as a complete software application or a public release build.
## English Repository Snapshot

For reader convenience, `english_repository_snapshot/` contains an English mirror of the repository text files. The main repository files remain the authoritative project materials; the snapshot preserves original folder and file names so cross-references remain traceable.

