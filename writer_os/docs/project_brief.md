# Project Brief

## Purpose

Writer OS is a local-first, agent-independent, Markdown-first working environment for creating a branching visual novel with AI assistance. It externalises selected creative work and persistent story context without forcing the human author to maintain a database-like schema.

The system should help the author:

- develop plot blocks and prose through iterative discussion and generation;
- design player-facing presentation, staging, choices, hidden events, and convergence;
- maintain shared and worldline-local continuity;
- retain useful alternatives without polluting active context;
- resume work without rereading the entire project;
- delegate summaries, navigation, comparison, and clerical consistency work to agents;
- preserve enough visible process evidence for separate dissertation analysis.

## Design Position

The author may move between narrative designer, direct writer, editor, aesthetic judge, curator, and staging designer. Writer OS must support those shifts rather than impose a linear distant-writing pipeline.

Plot blocks and nodes are different possible cuts. Plot blocks describe what a stretch of narrative develops; nodes and other presentation units describe how material is exposed to the player. Branches describe interactive path relations, while worldlines describe narrative worlds with persistent state.

The work may contain worldlines whose later histories differ at the scale of separate long-form `if` stories, not merely conventional romance routes or affection-threshold variations. Some lines may share little useful local writing context. This is why current-line context and deliberate cross-line comparison remain separate: a large narrative structure does not require every writing task to load every branch.

Authoritative creative material, inactive candidates, and agent-derived views have different responsibilities. Saving content, adopting it, loading it, implementing it, and assigning it to a worldline are separate decisions.

## Current Scope

- Markdown-only first version.
- Pre-authored and pre-edited reader-facing text; LLM assistance occurs only in the author's backstage creative workflow.
- One lightweight current-work entry.
- Creative work organised by development, presentation, story state, and drafts.
- Inactive candidate sets organised by creative question.
- Agent-maintained, human-readable summaries and navigation views created only when useful.
- Git-backed local workflow.

The current dissertation story is being selectively populated here. Existing material remains partial; directories and indexes should still be created only when real content needs them.

## Non-Goals

- No Python automation, YAML, JSON, front matter, or fixed metadata schema.
- No requirement that the author maintain registries or fill forms before writing.
- No automatic promotion from generated material to story truth.
- No complete transcript or research-analysis store inside Writer OS.
- No automatic Round Table ingestion.
- No front end or asset-production pipeline.
- No runtime LLM narration or direct player-to-LLM conversation.
- No Ren'Py export, labels, menus, variables, or bridge implementation.
- No claim that Writer OS is an agent, an independent repository, or the project-wide canonical source.
