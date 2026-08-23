# Writer OS

Writer OS is a local-first, agent-independent, Markdown-first working environment for an AI-assisted branching visual novel. It occupies the `writer_os/` subtree of this repository and supports authoring, persistent story state, candidate isolation, and focused context loading.

The current target is a pre-authored and pre-edited visual novel. LLMs may assist the author during prewriting, drafting, comparison, and review, but the player does not converse with a live LLM and the game does not generate its narrative text at runtime.

Writer OS is not an agent, an independent repository, the canonical source for the whole project, a research-record store, or a Ren'Py implementation layer.

The current dissertation story is being selectively populated here. Existing files provide working context, not complete coverage of every source, worldline, or unresolved design question.

## Start Here

1. Read `AGENTS.md` for the rules that apply to this subtree.
2. Read `current.md` once when starting cold, resuming after context loss, or changing tasks.
3. Follow the current-focus link to the actual working material. Treat any near-term queue as pointers, not as material to load automatically.
4. Load only the story commitments and context needed for the current task.

`current.md` is a lightweight pointer, not a second project status document. It may hold one current focus, a short near-term queue of usually no more than three directions, and one resume cue. A queue entry does not authorise work or enter default context. `current.md` should not duplicate repository-level handoff or status files, or external research records.

## Working Vocabulary

The following terms describe different boundaries within the same creative activity. They are not stages in a pipeline, required file types, or a fixed schema.

| Term | Primary boundary | Primary question |
| --- | --- | --- |
| working brief | the author's current turn of expression and attention | What intention is the author giving the agent in this turn? |
| plot block | narrative development | What is this stretch of the story developing? |
| node | player-facing presentation and staging | How and when does the player experience the material? |

### Working brief

A working brief is one human-authored input turn for the current work. It may be long or short, edited later, or followed by supplementary briefs. It may mix plot sequence, dialogue, emotional or event effects, aesthetic direction, staging, player experience, and sentence-level requirements.

A brief often ends because the author has expressed what is available in that turn, not because a narrative unit has reached its boundary. Later briefs may extend, correct, or redirect the same work. The brief remains author input and provenance; neither its contents nor an agent's interpretation of them becomes story truth without human confirmation. A working brief is not automatically a separate persistent file: ordinary input may remain in the transcript unless the author asks to retain or implement material from it. When retained or selected material is transferred into persistent creative work, preserve the source and any author-specified wording, effects, or constraints that matter.

### Plot block

A plot block is a flexibly sized narrative-development unit. One or more characters act across one or more logically connected scenes so that the story completes a perceptible causal, intellectual, emotional, or thematic development.

Its unity comes from what the stretch is developing, not necessarily from one location, one cast, or one scene. Time or place changes, completion of an action, a relationship change, an intended emotional or event effect, and the author's working rhythm may all suggest a boundary, but none is a mechanical test. A key event may occur in the middle while the rest of the block interprets, intensifies, transforms, or carries forward its effect.

### Node

A node is a deliberately treated player-facing presentation unit. It supports creative decisions about how and when material is exposed or staged, including cast, time, place, camera, environment, visibility, pacing, choices, and possible asset needs.

Node design is not clerical metadata or necessarily a later analytical step. It may arise before, during, or after plot-block development, and presentation decisions may reshape narrative order, pacing, revelation, or emotional effect. Not every camera, environment, scene, or choice change requires a node. A node is not automatically a branch, a worldline, or a future Ren'Py label.

### Relationship among the three

Their relationships are many-to-many and iterative. Several working briefs may develop or revise one plot block; one brief may span several plot blocks or directly discuss nodes and staging. One plot block may be presented through several nodes, while one node may contain material from several smaller plot developments when a continuous player-facing presentation makes that useful. Do not force material through a `brief -> plot block -> node` conversion sequence. A future Ren'Py bridge may map these decisions into different execution units without assuming one-to-one correspondence.

## Working Structure

The following directories are created only when real material first needs them. Do not pre-populate them with empty templates or placeholder indexes.

```text
writer_os/
├── README.md
├── AGENTS.md
├── current.md
├── creative_work/
│   ├── development/
│   ├── presentation/
│   ├── story_state/
│   └── drafts/
├── candidates/
├── agent_views/
├── archive/
└── docs/
```

### `creative_work/`

- `development/`: active plot blocks and narrative or prewriting design currently being developed, resolved, or given literary or narrative form. A selected prewriting outcome belongs here when it has been activated for continued creative work; placement does not make it story truth.
- `presentation/`: player-facing cuts and staging, including nodes, chapter or cast changes, time and place changes, camera or environment changes, visibility, choices, and future asset needs.
- `story_state/`: human-confirmed shared or global continuity commitments, worldline-local truths, branching and convergence decisions, and durable style or voice commitments.
- `drafts/`: the single primary location for prose and script drafts.

Material in `creative_work/` may still be developing. Directory location alone does not make a statement authoritative; authority comes from explicit human confirmation.

These areas describe parallel responsibilities, not a required promotion pipeline. A retained option may commonly move from candidate exploration into active development and later contribute to story state or drafts, but active material may enter `development/` directly and a confirmed commitment may enter `story_state/` directly. “Prewriting outcome” describes where material came from, not a single maturity level.

When a confirmed setting has not yet been literary or narratively realised, keep the confirmed fact or constraint in `story_state/`; use `development/` for the active work of turning it into plot, character, conflict, scene, or player experience. Link the two rather than maintaining competing authoritative copies.

### `candidates/`

Use this area for deliberately retained candidate sets organised around a creative question. Retained candidates are inactive by default. Saving material does not mean adopting it, loading it, implementing it, or assigning it to a worldline. A candidate can be loaded explicitly for comparison without first being moved or copied; if continued work produces an active synthesis, link it to the candidate source.

### `agent_views/`

This reserved directory is currently empty. Create a derived, rebuildable aid here only after repeated use demonstrates a concrete need. It must remain self-contained, point only to material that is already safe to include in Writer OS, and must not become a private-source navigation layer, provenance store, or second source of story truth.

### `archive/`

Create this area only when material that was once active is deliberately retired but still needs to remain visible as a historical artefact. Use Git for ordinary version history.

## Context Boundaries

For ordinary writing, prefer the current work, relevant shared commitments, and the current worldline. Load adjacent worldlines only for a concrete comparison, divergence, convergence, cross-line echo, or other task that requires them.

Inactive candidates, rejected material, full transcripts, research analysis, imported prior work, and future Ren'Py planning are not default writing context.

Raw transcripts and result-producing agent actions may be dissertation evidence, but that evidence remains outside Writer OS. Content enters the active story only after explicit human selection.

## Deferred Work

- No Python automation, YAML, JSON, front matter, or fixed metadata schema.
- No front end.
- No Ren'Py bridge or export mapping.
- No project-wide research-record structure.

These may be reconsidered only after real writing exposes a concrete need.
