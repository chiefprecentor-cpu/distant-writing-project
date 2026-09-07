# AGENTS

These instructions apply only to the `writer_os/` subtree.

Writer OS is an agent-independent, file-based authoring and persistent-context environment in the `writer_os/` subtree of this repository. It is not an agent, an independent repository, the canonical source for the whole project, a research-record store, or a Ren'Py implementation layer.

The current dissertation story is being selectively populated here. Existing files do not imply complete coverage; do not invent missing story facts to fill gaps or complete the structure.

## Working Rules

- Work in Markdown only for the first version.
- Do not introduce Python automation, YAML, JSON, front matter, fixed IDs, or other schemas unless explicitly requested later.
- Accept natural-language input that mixes plot, dialogue, aesthetics, staging, and player experience. Do not require the author to convert it into a form first.
- Keep the size of the work proportional to the task. A local prose question does not require rebuilding the global story model.
- For ordinary narrative design, prefer development, comparison, and local coherence checks. Do not frame literary creation as stress testing or exhaustive validation unless the author explicitly requests a system, harness, or experimental evaluation.
- Separate discussion from implementation. Suggestions do not change files until the human author authorises implementation.
- After implementation, report the completed scope, any deviation, and any new semantic consequence that was not already agreed.
- Do not treat uncertainty, hesitation, AI praise, generated prose, brainstorming, or retained candidates as human decisions.
- Do not silently overwrite or normalise human-authored wording, protected revisions, or final text.

## Authority and Responsibilities

- Directory location alone does not grant authority. Story authority comes from explicit human confirmation.
- Route material by its current role, not by its origin or a mandatory maturity sequence.
- `creative_work/development/` contains active narrative and prewriting design being developed, resolved, or given literary or narrative form. It may include selected directions and provisional material, but does not establish story truth by location.
- `creative_work/presentation/` records creative decisions about player-facing cuts and staging; these are not clerical metadata.
- `creative_work/story_state/` holds human-confirmed shared or global commitments and worldline-local truths. An agent may propose changes but must not promote them silently.
- `creative_work/drafts/` is the single primary location for prose or script drafts. Do not maintain a second copy inside node folders.
- `candidates/` is inactive by default. Saving, adopting, implementing, loading, and assigning to a worldline are separate decisions.
- A common route may be `candidates -> development -> story_state or drafts`, but it is not compulsory. Active material and confirmed commitments may enter their appropriate areas directly.
- When a confirmed setting still needs literary or narrative development, keep the authoritative constraint in `story_state/` and develop how it enters plot, character, scene, or player experience in the relevant creative material. Link between them instead of maintaining competing primary copies.
- `agent_views/` is reserved for rebuildable derived aids when a demonstrated repeated-use need appears. Do not use it for private-source navigation, provenance records, or a second source of story truth.
- `archive/` is for deliberately retired active material, not ordinary Git history or every unused generation.

Create directories and indexes only when real content requires them. Do not recreate a full empty skeleton.

## Current Work and Loading

- On a cold start, after context loss, or after a task change, read `current.md` once.
- `current.md` may name one current focus, a short near-term queue of usually no more than three directions, and one resume cue.
- Load the current target, directly relevant human-confirmed commitments, and the minimum local context needed for the task. Queue entries are pointers only: they do not authorise implementation and are not default context until the task moves to them.
- Within an ongoing conversation, read only new or changed material unless the task requires a broader check.
- When the author has authorised ongoing maintenance of the current development file, refresh it in place whenever discussion establishes or reverses a provisional judgment, produces exact wording needed for later comparison, or leaves an unresolved question that determines the next writing step. Record the current semantic state rather than session chronology; preserve consequential rationale and copy key wording exactly when paraphrase could cause semantic, voice, or conceptual drift. As discussion develops, revise or integrate superseded provisional material in the same file, retaining only prior reasoning still needed to avoid a known misunderstanding. Do not copy the full transcript.
- Load adjacent worldline summaries only for a concrete divergence, convergence, cross-line echo, comparison, or special cross-line scene. Read full adjacent-line prose only when exact comparison is necessary.
- Do not load inactive candidates, unrelated worldlines, rejected material, full transcripts, research analysis, or Ren'Py planning merely because they may be useful.
- Private material outside this repository requires explicit task relevance and permission.

Update `current.md` only after a meaningful change of focus or confirmed state. Do not update or repeat it after every small action.

## Summaries and Navigation

- Give each relatively stable chapter a concise summary when leaving it or reaching a meaningful checkpoint.
- Give each mature plot block summary coverage. If its primary record is already concise, do not create a duplicate summary file.
- Summarise a node only when it has independent narrative importance; do not summarise every minor camera, environment, or technical cut.
- Refresh a worldline state summary when the line forms, changes materially, or reaches a meaningful checkpoint.
- A persistent summary must identify its source scope. A summary stored in `agent_views/` must record its source locations as paths relative to the repository root, for example `writer_os/creative_work/...`, never as absolute filesystem paths. If a clickable Markdown link is also used, its target must resolve relative to the summary file. If the source changes materially, update the view or state clearly that it may be stale.
- Return to primary text for exact wording, voice, rhythm, and fine-grained emotional judgment.
- Prefer Markdown links and ordinary search. Create a central index only after scale, stable IDs, repeated lookup failure, or later bridge work demonstrates a real need.
- Indexes list objects and links; they do not duplicate full prose or silently add facts.

## Narrative Structure

- Treat a plot block and a player-facing node as different possible cuts; do not assume a one-to-one relationship.
- Keep chapter, cast, time, place, camera, environment, visibility, and player-choice cuts available as distinct presentation concerns.
- Treat a branch as an interactive path relation and a worldline as a narrative world with persistent state. Neither automatically implies the other.
- Keep shared commitments, worldline-local truths, character knowledge, player knowledge, and the writing agent's comparison context distinct.
- Preserve hidden, offscreen, and protagonist-absent events when they have later continuity consequences.
- Treat convergence as a creative structural decision, not an automatic erasure of prior state.

## Large-Scale Plot and Narrative Design

- Develop large, open-ended plot or narrative-design tasks through several rounds rather than turning the first promising direction into a complete plan. In each round, take one coherent step by working on one bounded question, level, or connection. Give the author enough material to judge that step, then stop before beginning another consequential step or elaborating the same line into a full plan.
- A round may present one candidate direction when only one appears genuinely useful, or compare a small number, usually two or three, when meaningful alternatives address the same question at roughly the same scale. Do not invent a weaker alternative merely to fill a number or create the appearance of choice. Keep the total round, rather than each candidate, within the amount the author can comfortably review; around a hundred lines may serve as a rough upper guide for a substantial design pass, not a target to fill.
- Give parallel candidates compact and comparably developed accounts of their central narrative movement, required assumptions, intended effect, and what they foreground or leave aside. Stop before developing any candidate into the next level. If several remain promising, explain whether they appear mutually exclusive, combinable, or potentially suitable for distinct player-facing branches, and let the author decide how they should continue. Preserving several candidates does not by itself establish branches or worldlines.
- Let the author participate in constructing each consequential next question. When moving between the whole story, a chapter group, plot block, bridge, scene, or wording would materially redirect later work, show what the next choice is and wait for the author's response. Routine elaboration within a direction the author has already confirmed does not require a new checkpoint.
- Treat development from micro material towards a larger structure as primarily author-led. When the author introduces a strong line, image, action, or local scene, help explore how it might grow upwards. During macro-level work, do not routinely invent additional micro scenes. Surface an agent-originated micro anchor only when there is a specific reason to think it is unusually novel, forceful, or well aligned with the author's established aesthetics. Present such an exception singly and briefly, explain why it may deserve attention, and do not expand it unless the author chooses to pursue it.
- When two worthwhile parts of the narrative do not yet have a convincing connection, preserve both and leave the bridge unresolved. Do not generate an ordinary or over-explained transition merely to make the structure appear complete. Return to the bridge when character motivation, worldbuilding, or surrounding scenes provide better material.

## Candidates and Reviews

- Ordinary chat output remains in the transcript unless the human explicitly asks to retain or implement it.
- Deliberate enumeration may preserve a whole candidate set without activating any option.
- Compare any number of candidates using the intended emotional, narrative, staging, or player effect; do not present one aesthetic rubric as universally objective.
- A candidate-curation pass may be proposed when the author is stuck, finishes a stage, or asks for it. Return only a small relevant selection with source links and reasons.
- Continuity, plausibility, voice, style, and Git-history checks are task-triggered activities, not mandatory gates or permanent review folders.

## Language and Style

- Treat durable tone, narrative voice, character language, and local aesthetic commitments as creative story material, not as agent summaries.
- Protect specified dialogue, emotional aims, character relationships, and deliberately unusual expression during language cleanup.
- Do not equate removing generic AI phrasing with flattening the work's voice.
- Write prose or script material placed in `creative_work/drafts/` directly in English unless the author explicitly requests a Chinese reference version or bilingual work. Chinese input alone does not imply that the draft should be written in Chinese.
- Translate routine Chinese instructions into natural English without requiring a translation discussion. When a Chinese expression permits materially different English readings that could affect meaning, voice, characterisation, imagery, cultural resonance, or a conceptual or technical claim, identify the ambiguity and discuss the translation approach before treating one rendering as final, even if the author did not flag the issue.
- English is the current target text; Chinese may assist author review but must not hide defects in the English; Japanese remains a later cultural and localisation layer requiring stronger human validation.
- Temporary language, voice, and dataprint checks do not need to be saved unless they produce a durable human-confirmed rule.

## Research and Ren'Py Boundaries

- Raw transcripts, tool or file actions, Git changes, and researcher interpretation remain outside Writer OS even when they are dissertation evidence.
- Keep Writer OS self-contained. Do not record private or local source filenames, absolute paths, raw chat excerpts, personal-process notes, course provenance, or mappings from fictional characters and events to identifiable real people or incidents. Public, verifiable references may be retained when they support research or fact-checking.
- Do not copy a full transcript into active story context. Transfer only material the human explicitly selects for continued creative work.
- A future Ren'Py bridge must use accurate drafts, confirmed presentation decisions, and confirmed story state rather than treating summaries as executable truth.
- Do not create a front end, asset pipeline, Ren'Py mapping, or bridge registry in this version.
