# AI Fingerprint and Late-Tea-Scene Skill Extraction

Date: 2026-09-04

## Fixed Range

This pass only checks the following three traces that already exist. It does not automatically include new captures produced after the review begins:

- `traces/2026-09-03/01a06380-f600-7d00-bcc4-dba1b89fc133-c060f9087d61.jsonl`
- `traces/2026-09-04/01a06380-f600-7d00-bcc4-dba1b89fc133-c060f9087d61.jsonl`
- `traces/2026-09-04/01a06dc0-656f-7321-b1ba-ea77c255fb5d-81e680980973.jsonl`

Basis for selection: the first two belong to the same long session and contain the process in which the late-tea scene moved from minimal design, to an English draft, to the author's identification of AI fingerprint, and then into continuous structural rewriting. The third immediately follows the late-tea checkpoint and contains the first embodied appearance of Interface and the author's correction of premature character inference. It can function as counterevidence or extension around the adjacent problem, instead of deriving a rule only from one marked bad sentence.

The author later explicitly asked for Opening language-revision records to be added. The range is therefore expanded here once to include the following existing captures and checkpoint-bounded intervals; later traces that appear after this point are still not automatically included:

- `traces/recovered/01a02e7d-c329-7060-b5a4-d405b39a4100.recovered.jsonl`, only recovered sequences 341-520;
- `traces/2026-08-27/01a04356-e61f-7383-99d0-d950918c445c-1614cb66438f.jsonl`, sequences 1-314;
- `traces/2026-08-28/01a04356-e61f-7383-99d0-d950918c445c-1614cb66438f.jsonl`, sequences 315-629.

The added range was navigated from the existing `records/2026-08-29_draft-style-subtlety-and-pacing-skills.md`: the first segment covers the first English Draft of Opening and early line-by-line revisions; the latter two cover later revisions of walking together, friend conversation, maid café, narration / inner voice and language density. The old Record is used only for navigation. Judgement still returns to these traces; the low-value late segment sequences 470-504 already judged by that Record are not added again.

## Review Progress

- Completed: trace and existing Records enumeration; selection of the initial range based on user/assistant message-level hits; mechanical completeness checks of the three recent captures; review of late-tea design, first draft, two rounds of rewriting and adjacent Interface first-appearance review.
- Completed: according to the author's added request, reviewed Opening recovered sequences 341-520, 27 August sequences 1-314 and 28 August sequences 315-629, with limited calibration against the final Opening.
- Completed: sixth skill prototype, shared aesthetic profile, integrated review routing, retrospective use cases, structural validation and project-level installation.
- Pending: none. The first real drafting invocation is left for a later natural forward test, without opening an extra Agent context for this delivery.
- Checked and skipped: in the early range, sequences 1-229 concerning orbital science, space-law web materials and ordinary success receipts that have no direct relation to AI fingerprint; in the Opening range, large-scale transcript path lookup, historical name materials, web fact-checking and purely mechanical formatting-conversion results. All were first confirmed by message/tool index for their function, then marked low-value.
- Current evidence gap: checkpoint Git snapshots fixedly point to `Dissertation/project/`, not the actual working `Documents/distant-writing-project/`; therefore the snapshots cannot be used to judge clean/dirty evolution of the late-tea files. The first Opening session uses a recovered trace, so its recovery limits remain. The new skill has not yet had an independent forward test.

## Capture Verification

- The 3 September capture for the same session covers sequences 1-334, including two paired automatic Pre/Post checkpoints (182/185, 331/334); the 4 September continuation capture covers 335-526, including one paired manual checkpoint (524/526). Both have session ID `01a06380-f600-7d00-bcc4-dba1b89fc133`.
- The later 4 September session covers sequences 1-161, including one paired automatic checkpoint (158/161), with session ID `01a06dc0-656f-7321-b1ba-ea77c255fb5d`.
- All checkpoints have cwd `/Users/[username]/Documents/distant-writing-project`, model recorded as `gpt-5.6-sol`; there is no `capture_gap`, `capture_error`, `reset_reason`, or `partial_tail_bytes`.
- The three captures respectively contain 114/114, 82/82 and 47/47 `assistant_tool_call` / `tool_result` records; user, assistant commentary/final, hook and turn ID are distinguishable.
- The fixed `project/` Git snapshot command itself succeeded, but it does not cover the actual working repository. The following analysis therefore relies mainly on trace user/assistant messages and visible tool input/result; when textual state must be checked, `distant-writing-project` is inspected separately in read-only mode, without treating later current files as the version at the time.

## Trace-First Findings

### It slid from completed design directly into "telling the design completely"

When 3 September sequences 242-320 formed the writable conditions for late tea, many local judgements were careful in themselves: Yuankai knows that once He Xuyuan understands the problem, he will be summoned; He Xuyuan had already participated in integrating evidence across sources; Yuankai must both let him understand and protect his right to refuse; late tea only makes him continue reading and does not make him accept ascent; the parents remain healthy, and the responsibility that comes from being an only son is still included in ordinary retirement life. Character tension is not lacking here.

The risk comes from the fact that the design language had already explained these relations very completely. After sequence 322 authorised drafting, the Agent fully read the opening, active development, story state and relevant Git evolution; sequence 381 also accurately summarised three narrowings: "care candidate -> healthy parents' retirement", "ordinary witness -> core of the evidence chain", and "mission failure -> action success but return failure". Source understanding was broadly correct, but the first draft at sequence 382 assigned almost every correct design decision to visible narration or dialogue.

The first draft's fingerprint appears on at least four levels:

- Syntactic level: consecutive three-part lists, nearly equal-length parallel statements, complete positive/negative contrasts, and repeated `not X / still Y / what changed was Z`. Each sentence is clear by itself, but their density near each other gives the whole text the same kind of rhetorical completion.
- Information level: legal authorisation, orbital facility, evidentiary continuity, return risk and family responsibility enter the prose according to the logical groupings of the design document; `## The Papers`, `## The Invitation`, and `## The Rest of the Tea` further cut the scene into argumentative chapters.
- Dialogue level: He Xuyuan frequently functions as a question interface, while Yuankai provides complete, correct and pre-organised explanation. There is too little process in which characters misread, answer only locally, materials reveal meaning before speakers do, or a question changes direction.
- Scene level: the black confidential case, the place specially kept for the protagonist, the friend's admission that he recommended him, the backup-personnel scheme and the risk table together reproduce the familiar device of "an old acquaintance representing a system comes to recall a special talent". Even if three-part lists were removed, this motif would still control the reader's understanding of the character relation.

It is notable that at sequence 384 the Agent had already promised to read through and "press down any paragraph that feels like a setting briefing", and at sequence 401 it judged that the technical, legal and risk material in about 3,100 words already served the pressure of choice. Only afterwards, at sequence 408, did the author point out that the whole text still contained many parallelisms, three-part lists, positive/negative juxtapositions, direct translation of Chinese discussion into fiction, Yuankai's lines being ninety percent explanation, He Xuyuan looking as if he had not read the material, and a clichéd item-by-item recruitment Q&A. This was not a lack of one reminder to "avoid infodump". It was the Agent mistaking **correct design and the presence of choice pressure** for **information having already acquired literary movement**.

### The first revision solved surface and medium, but not the motif

In sequences 409-470, the Agent read five existing skills, the shared aesthetic profile, the full late-tea text and the full opening. It explicitly redistributed information to materials, He Xuyuan's reading, incomplete inference, Yuankai's local answers and silence. The first rewrite deleted thesis-like subheadings, compressed about 3,100 words to about 2,400, and transformed abstract explanation into a near miss with unloading robots, permissions that did not connect across files, a blank authorisation field, a red-line moment and return estimates. He Xuyuan began to actively discover, instead of only asking on the reader's behalf.

These were substantial improvements, but the revision process also repeatedly used regex to find `not`, three-part lists, `Yes/No` and similar sentence patterns. Such searches can locate recurrent density; they cannot judge whether a repetition belongs to character voice, comic beat or deliberate form. More important, at sequence 472, before rereading the sentences, the author pointed from an overall feeling to the problem that the scene still resembled "an old officer coming to find a retired veteran". This proves that the first revision changed the information medium, but did not check the default dramatic template governing the whole scene.

### The second revision changed scene ownership

At sequence 472, the author did not give a list of new settings. He gave a provisional relation closer to the required nuance: He Xuyuan integrates information for different parties from outside the system, and the problem gradually becomes an attractor; Yuankai, inside the system, consults him about whether he should enter a vortex while knowing that he will be changed. Sequence 481 added that Yuankai might care more about He Xuyuan himself than mainly about the problem or mission.

From this, the Agent identified the deeper residue in the first rewrite: ownership of the scene's information and action still lay with Yuankai / the system. The revisions in sequences 479-516 removed the black case, recommendation, exclusive reserved place, candidate-risk table and `plan without Xuyuan`; the evidence map on the table was He Xuyuan's own working environment from the start, and Yuankai only brought a temporary access key. The blank no longer meant that the system had reserved a place for a genius, but that the problem on site kept pointing back to judgement that could not be fully handed over. Yuankai no longer persuaded on behalf of the mission. He only said that he did not want the evidence map to make the decision for He Xuyuan, and used the return-risk page he had reread again and again to answer whether this line should be crossed.

Removing the fingerprint here was not a matter of reducing textual neatness. It changed the default causality: from "the system discovers and recalls a special person" to "work that the system cannot monopolise has already formed inside the character's home, and an external problem gradually draws him in". The author's correction was not merely negative deletion; it supplied a more distinctive scenic gravity and relational centre.

### The adjacent Interface first appearance exposed the same kind of epistemic shortcut

In sequence 40 of the following session, the Agent had already actively used subtext and dialogue skills and tried to minimise Interface's explanation, but it still made He Xuyuan immediately ask after opening the door whether she was behind the orbital policy shift, and then let him produce `In another history.` The author pointed out at sequence 49 that visually she is first just an ordinary, even almost high-school-aged, beautiful girl; the extraordinary attention in her pupils can only possibly be felt after looking for a while, and at the moment the door opens there is no perceptual evidence leading to the orbital backstage or multiple worldlines.

The correction in sequence 58 acknowledged that this was not a single-sentence problem. He Xuyuan had said the "worldline structure only the author knows" on Interface's behalf. This comes from the same source as the first late-tea draft: the Agent back-projected dialogue from the debate endpoint it wanted to reach quickly, letting the character skip the path that should have been formed by observation, misunderstanding, suspicion and gradual evidence. Even if the sentences are short and the explanation minimal, a character who sounds as if he has read the outline will still produce a marked AI-shaped feeling.

### Opening provides counterevidence: form itself is not the prohibition

The author's request to learn from Opening does not mean copying the surface of its short sentences. The current Opening also uses repetition, parallelism, positive/negative contrast and brief Q&A: left-right movement during the collision, three bad mornings, repeated `Yes` in the maid café, and Hyde Park's parallel weighing of London / returning to China all contain regularity. They do not necessarily produce the same fingerprint because each regularity has a local task: making collision rhythm, varied repetition, dry comedy between characters, or letting He Xuyuan actually form a difficult decision. Objects, bodies, mistakes, silence, social actions and unfinished relationships continue to share the burden of information.

Therefore, AI fingerprint in this project cannot be defined as the appearance of a particular word, dash, three-part list or `not X but Y`. A more accurate working definition is: **excess default neatness, explanatory closure and a pre-answered feeling appear simultaneously at several scales, making characters, scene and wording seem to faithfully demonstrate an already completed design.** Judgement depends on frequency, neighbouring density, whether function changes, who is entitled to know, and whether a more specific scenic gravity exists.

## Additional Calibration from the Opening Language-Revision Process

The author explicitly asked for the Opening language-revision traces to be added, because the final Opening had undergone more rounds of precise review, and its language quality should make it more suitable than the first late-tea draft as current calibration. The added range supports this judgement, but also shows that what should be learned is **the mode of judgement used in revision**, not the surface sentence length of the final Opening copied into later sections.

### The same form can first be questioned, then preserved because of local function

The first traffic-section draft once used `He found her in the movement. She found him.` The author first asked whether this symmetrical turn relative to the preceding text was intentional; the Agent explained that it had meant to mark the third short cut "opening" into a sustained scene, but that the second `found` also implied that Lulu actively searched. It was finally changed to `He found her in the crowd. She saw him too.` (27 August sequences 143-158). What was revised was not that "symmetrical sentences are illegal", but that the symmetry had additionally assigned the wrong character action.

Similarly, writing both intersections as `changed against them` made the city seem to actively obstruct the characters and made structural design too visible; the second instance was changed into an ordinary stopping. Conversely, the highly neat short contrast `The result was not unusual. The order was.` was provisionally accepted by the author because it accurately limited semantic intensity: what was unusual was the order in which judgement occurred, not Lulu passing some rare mate-selection threshold (sequences 244-256). These two adjacent cases show that shape is only an entry point for checking. The final question is what agency, intensity or relational fact it has written into the scene.

### Over-compression and over-expansion can both look like prefabricated argument

The early design of the friend conversation used `A blind corner. A wrong room. A string of service disruptions. Two people with similar timetables.` to neatly review events. The author pointed out that real conversation rarely solemnly repeats a known list in this way, and also felt that the quick exchange of short sentences erased He Xuyuan's desire to express himself. He asked for the dialogue to slow down, with fewer turn switches, so that the character could form aestheticisation and self-rebuttal around a chain of low-probability events in a longer utterance (sequences 191-220). AI-shaped feeling can therefore come from long explanation, and also from compressing complex experience into overly elegant noun fragments.

The first version of He Xuyuan's long speech also contained `a signal failure, a crowd-control decision and my inability to wake up on Thursdays`. The author specifically pointed out that the third item in the list was too written, as if ordinary oversleeping had been nominalised only to complete the list (sequence 244); this directly continues the judgement at late-tea sequence 408 about repeated three-part lists. But the author did not therefore ask the whole section to become short dialogue. The revision preserved the long argument and only reconstructed local causality, reference and word meaning. Finally, at the author's request, `absence of a common cause...formless` was changed to the more first-readable `‘not arranged by fate’ does not mean ‘formless’` (sequences 258-274).

This establishes a two-way threshold: a complete explanation fails if it sounds like a pre-prepared authorial summary; deleting the thinking that a character actually needs to own into elegant compression, for the sake of "subtlety" or "naturalness", also fails.

### Naturalness comes from conversational action and implied fact, not from replacing words with more colloquial ones

The author thought `Was that the talk you came for?` sounded like checking an itinerary. Asking `What did you think of the talk?` first, then letting Lulu herself say that she went to the wrong room, better fit the immediate conversational motive (recovered sequences 443-444). He also pointed out that a dangling `her` followed by `Who is she?` accidentally implied that He Xuyuan often reported different women to his friend, and that `found the conclusion there` wrote ordinary attraction as an overly strong conclusion. The revision handled antecedent, tense, relational implication and intensity at the same time, instead of merely choosing a more colloquial word.

In the Mallowbell draft, the author preserved the slightly nerdy `You omitted several relevant properties.`, because it may be precisely He Xuyuan translating discomfort into missing parameters. He also preserved the second paragraph of the rice fantasy, because letting only a close reader infer the kitchen, the night and Lulu sitting by the table would lose a necessary relational shift. By contrast, `Neither friend commented.` was deleted, because the friends' failure to tease had already been accomplished by action (28 August sequences 555-560). This further confirms that removing fingerprint cannot have "more colloquial, less, more implicit" as one unified direction.

### The calibration value and boundary of the final Opening

The current Opening can function as stronger calibration because it has gone through several rounds of specific author review on conversational motive, semantic intensity, viewpoint permission, function of repetition, characters' desire to express, first-read visibility and format channels. Its borrowable features include:

- information is shared by action, traffic, crowd, objects, scene sound, misunderstanding and character language;
- quietness is not equivalent to one syntax or continuous sparse dialogue; language density can change between sections;
- repetition needs to change condition or relation; it does not require every surface form to be replaced;
- He Xuyuan can speak at length, technically and awkwardly, but a long speech should make thinking happen rather than recite a development summary to the player;
- relational transitions that must be graspable on first reading can be explained; meanings already completed by action do not need to be summarised again.

The boundary is also clear: Opening is a section that has currently received relatively sufficient review; it is not the sole voice of the whole work. The existing aesthetic profile still acknowledges insufficient samples for later worldlines, sustained tragedy, horror, action sections and other characters' speech. In this project, the new skill may use corresponding Opening fragments for functional comparison by problem, but should not by default read the whole draft, imitate its short-sentence ratio, or automatically judge an item wrong because it differs from Opening.

## Provisional Analytical Propositions

### Proposition 1: The main mechanism is design-completeness leakage

The clearer the existing design, the more easily the Agent mistakes "decisions that must not be forgotten" for "information that should enter the text". This is a combination of framing and delayed oversight: the author delegates most English surface generation to the Agent; the Agent faithfully maintains the source, but leaks the source's complete logic into dialogue and narration; the author only reclaims part of information allocation and scene construction after reading the primary Draft.

The counterevidence is that the Agent did not mechanically copy all settings: the first draft already omitted some cosmological background, and also organised the scene through tea, documents and silence. An alternative explanation is that this legal/technical conversation itself is especially likely to produce explanatory language, rather than this being a general model feature. The current proposition only applies to the reviewed late-tea scene and adjacent Interface skeleton, and should not be used to diagnose all AI texts.

### Proposition 2: Sentence-pattern cleanup cannot replace scene-motif checking

The first revision proves that reducing three-part lists, Q&A paraphrase and complete explanation can significantly improve the text. The author then still accurately felt the "retired veteran recalled by an old officer" template, showing that fingerprint can be sustained by higher-level character roles, props and plot prefabrication. Effective revision should first judge scene ownership, character knowledge path and information medium, then decide syntactic change; regex or counts are only suitable as clues for finding clusters.

The counterevidence is that a familiar motif does not naturally fail; deliberate genre patterning can also be powerful. The problem is not the existence of a nameable trope, but whether it replaces this work's more specific relational logic without being chosen.

### Proposition 3: The author prefers traceable information movement, not universal subtlety

The author did not require all information to be hidden. He required some information to enter subtext, some to be delayed as clues, and some never to be said in the whole work; at the same time, He Xuyuan may still speak technically, at length or with unusual precision. The key is that the reader can follow how information is acquired through objects, observation, misreading, questions, pauses and later echoes, rather than receiving an English transcription of the conclusion of a discussion all at once.

This also explains why the short dialogue in the adjacent Interface scene still failed: it was restrained, but it lacked traceable cognitive causality. Current evidence is insufficient to generalise this preference to action, horror, sustained tragedy or other character voices; it should be treated as an updatable aesthetic tendency, not as the constitution of the work.

### Proposition 4: The value of the final model passage comes from revision history, not static similarity

The higher language quality of Opening is not a property that can be extracted as average sentence length or a fixed "quiet style". The revision history shows that the author sometimes dismantled symmetry and sometimes preserved it; sometimes deleted explanation and sometimes supplied it; sometimes compressed jokes and sometimes restored long expression. Its stability comes from each form having been asked: "who is doing what here, what must the reader grasp, and what extra implication does this sentence add?"

Therefore, using Opening as calibration should be comparative reading: compare how information moves, how characters acquire judgement, whether repetition changes function, and whether explanation has been earned by the scene. It cannot only ask the model to "learn the language style". Another explanation is that the final Opening's quality comes mainly from more everyday subject matter and lower technical burden, while late tea is inherently harder. That difference does exist, so the skill must also allow later scenes to carry higher conceptual density instead of forcing them into early-romance prose.

## Requirements for the New Skill

The existing `workshop-dialogue-and-comedy`, `explore-subtext-and-distance`, `shape-vn-rhythm-and-montage` and `review-vn-draft` can respectively handle dialogue action, timing of explanation, rhythm and integrated reading, but none of them explicitly owns cross-scale AI-shaped diagnosis among "sentence regularity - information flow - character knowledge - scene template". A new skill has a real function here; it is not merely a renamed duplicate:

- treat AI fingerprint as reading effect and pattern clustering, without claiming to determine real authorial source from style and without serving detector evasion;
- for a long scope, first read the full text and the author-designated approved calibration passage, without requiring the user to pre-mark every problem;
- distinguish functional repetition/symmetry from undifferentiated recurrence, and do not create bans on three-part lists, negative sentences or precise dialogue;
- check whether design conclusions have entered the text without scene transformation, and which information should instead be carried by action, object, error, delay, silence or remaining unsaid forever;
- track the perceptual and epistemic path for each key judgement, preventing characters from having outline knowledge;
- before polishing sentences, check whether a default recruitment, interrogation, confession, mentor explanation or other familiar scaffold has taken scene ownership away;
- in revision, change high-leverage structure and information allocation first, then local sentence shape, and report the meanings delayed, deleted or changed as a result;
- allow Opening to function as current project calibration, but learn its information division and local functions, not its short-sentence ratio or surface rhythm.

Added Opening range completion status: message layers and directly related patches in recovered sequences 341-520 have been reviewed; language judgements, related patches and final Opening comparisons in 27 August sequences 1-314 and 28 August sequences 315-629 have been reviewed. Large-scale transcript search, web fact-checking, historical name materials and purely mechanical formatting-conversion results were skipped after confirmation, because they have low analytical value for this AI fingerprint definition. The recovered file preserves the recovery manifest and the historical `transcript_identity_changed` gap at sequence 209; the 341-520 range used here belongs to a later reconstructed lifecycle, so conclusions retain the boundary of recovery evidence.

## Skill Implementation Result

New prototype:

`agency_audit/skill_prototypes/rework-ai-shaped-fiction/SKILL.md`

The name chosen is `rework-ai-shaped-fiction`, rather than detector or humanizer language. The description will participate in automatic routing when the user mentions `AI fingerprint`, `AI flavour`, generated-feeling regularity, dialogue-as-essay or over-designed polish, while explicitly expanding the possible problem to sentence shape, information flow, character knowledge and familiar scene templates. It states clearly that it only performs literary revision, does not judge author source, and is not used to evade detection.

`SKILL.md` remains 50 lines and 893 words, with no extra scripts or references. Its core order is not a fixed workflow but a causal priority: first read the user-specified scope and necessary calibration; identify the scale that truly produces the effect; revise scene ownership, information allocation and character cognitive path before sentence shape. It explicitly allows review of local excerpts, but forbids claiming that the whole draft has been cleared of the relevant issue after reading only an excerpt.

The shared aesthetic profile adds four updatable calibrations: planning material is not a prose-delivery checklist; unusual intuition still needs a perceptible epistemic path; AI-shaped feeling is cross-scale accumulation, not a single tell; final Opening is the current stronger project calibration, but not the only one. The project-installed version already had one later-formed judgement, "do not turn viewpoint ownership into moral sanitisation". It was first synchronised back into the prototype before migration, and was not overwritten by the old file.

The selective specialist list in `review-vn-draft` adds this skill. Integrated review does not load it by default; it is read only when AI fingerprint, as a cross-sentence, information-flow, character-knowledge or scene-scaffold problem, would actually change judgement.

Retrospective use cases are written into `agency_audit/skill_prototypes/SMOKE_TESTS.md`: the full first late-tea draft, the first rewrite still containing the recruitment template, final Opening as a counter-prohibition case, and the short Interface first appearance that still has outline knowledge. They prove that the test design is not using only the bad sentence already circled by the author, and does not mistakenly delete functional regular forms in the final Opening. This is trace-backed retrospective mapping, not an independent model evaluation.

Installed to:

`/Users/[username]/Documents/distant-writing-project/.agents/skills/rework-ai-shaped-fiction/`

and synchronised with the shared profile and `review-vn-draft` routing inside the project. The target project at this point has modifications to two tracked skill files and one new skill directory; no add or commit was executed.

The official `quick_validate.py` still reports `ModuleNotFoundError` because system Python lacks `PyYAML`, the same as last time; this is not recorded as validation success. An equivalent check of the items monitored by that validator was performed with system Ruby YAML, and all six skills passed frontmatter, directory name, description length and all local relative links; prototype and installed version were byte-identical across the three synchronised files, and `git diff --check` passed in both repositories.

## Correction After the Author's Clarification: The Unresolved Sentence in Opening and AGENTS Rules (2026-09-04)

The author clarified that `The result was not unusual. The order was.` had not received definite approval. The current feeling was only "acceptable", and a conjunction might also be added. The wording above, "this highly neat short contrast was accepted by the author", is too strong. Under the Record's append-only provenance rule, the original paragraph is not rewritten. The current state is corrected as follows: this sentence is a **local candidate that is acceptable but still open**. The no-conjunction version is more broken and more like the character compressing the difference into an aphorism; `The result was not unusual, but the order was.` is more continuous and may better fit on-site explanation, but may also become an overly standard rhetorical contrast. At this stage, the choice is not made for the author.

It can still serve as an anti-prohibition test, but the test target changes: the skill must neither automatically delete symmetry when it sees it, nor declare its function positively confirmed simply because the sentence remains in final Opening. The prototype and test description have been supplemented with "surviving line is not equivalent to positively confirmed".

The target repository has only two applicable rule files: root `AGENTS.md` and `writer_os/AGENTS.md`. Item-by-item checking found no conflict:

- `writer_os/AGENTS.md` requires protecting specified dialogue, emotional aims, character relations and deliberately unusual expression, and explicitly states that removing generic AI phrasing is not equivalent to flattening voice. The new skill likewise lists purposeful strangeness, technical or uneven voice, and effective repetition as things to protect.
- AGENTS requires precise wording, voice, rhythm and fine-grained emotional judgement to return to the primary text. The new skill requires reading the author-specified full scope, and only selectively reads corresponding Opening fragments when useful; it cannot replace reading with summaries or sentence-pattern counts.
- AGENTS requires minimal relevant context. The new skill does not default to loading the full Opening; it selects corresponding sections only when calibration would substantively change judgement. A user-requested whole-draft cleanup reads the whole draft; a local problem reads only the local area. These do not conflict.
- AGENTS states that review does not automatically authorise file modification, and human final text must not be silently overwritten or normalised. The skill only implements under authorised revision, and requires reporting semantic or relational consequences.
- AGENTS makes style / voice check task-triggered rather than a permanent gate. The skill's description only routes it when the user raises AI fingerprint / AI flavour or when the text genuinely presents cross-scale generated-feeling; it does not turn every writing task into mandatory purification.
- AGENTS allows bridges to remain unresolved and opposes making ordinary, over-explained connections for completeness. This is consistent with the skill's caution around explanatory closure and scene scaffold.

Their hierarchy is: AGENTS supplies the permission, source and style-protection boundaries for the whole Writer OS; `rework-ai-shaped-fiction` only supplies more specific diagnosis and revision thinking after the relevant task is triggered. There is no need to reduce AGENTS, and the skill content should not be duplicated back into it.

This calibration changed the new `SKILL.md` from the 50 lines and 893 words recorded above into 52 lines and 940 words; the original numbers only describe the version before the author's clarification. After supplementation, prototype and installed version were again compared byte-for-byte and found identical; equivalent validation of YAML, name and links for six items passed, and `git diff --check` passed in both repositories. One Ruby command during the process exited because the directory argument to validate was missing; it was replaced by two successful runs with complete arguments and is not counted as evidence of passing.

## Seven-Item Bundle: Proactive Drafting Skill and Three Narrow Updates (2026-09-04)

The author confirmed the previous bundle review: first establish `draft-vn-scene-from-design`, and update the old skills already identified. Although `stage-vn-presentation` is a real issue, it should not be created now. The author also gave a local production decision for late tea: to save time, there is no plan to make extra background states or CG for screen lights turning on and off, small actions, or similar changes.

This local decision was not written into the shared aesthetic profile, and did not become a rule that the whole work should use fewer CGs / screen changes. The new drafting skill only extracts the generalisable part: respect the production scope / asset budget that the author gives for the current scene; stable composition can carry change through text, sound, time and player understanding; do not automatically add micro-action CG, background variants or continuous sprite churn just to prove that a visual novel is "visual". When another scene truly depends on visual change and the budget allows it, such changes remain available.

### `draft-vn-scene-from-design`

New prototype and installation:

- `agency_audit/skill_prototypes/draft-vn-scene-from-design/SKILL.md`
- `/Users/[username]/Documents/distant-writing-project/.agents/skills/draft-vn-scene-from-design/SKILL.md`

It fills the gap of first drafting rather than after-the-fact review: when moving from development, story state, outline or agreed scene design into / continuation of English VN Draft, it preserves source constraints without making the planning structure directly perform itself as prose. Its core judgements include: the authorised entry and stopping point for this scene; the difference between confirmed / active / candidate / TBD; the current knowledge of characters and player; through which channel information is obtained; which designs should be delayed or never said; whether a familiar dramatic scaffold is assigning roles to characters instead; and the explicit production budget.

This skill is a lightweight coordinator. It selectively reads `interpret-co-writing-signals`, `explore-subtext-and-distance`, `workshop-dialogue-and-comedy`, `shape-vn-rhythm-and-montage` or `rework-ai-shaped-fiction` only when a related issue actually changes first drafting; it does not default to loading all siblings. Its boundary with the latter is: the former prevents design-completeness leakage when moving from design into Draft; the latter diagnoses and reconstructs text that has already produced AI-shaped feeling.

The production file has 58 lines and 884 words, with no additional references, scripts or UI metadata. The description limits its trigger range to moving from prewriting / design into, or continuing, VN draft. It should not attract ordinary design discussion or local review of existing text.

### Three Narrow Updates to Existing Skills

- `interpret-co-writing-signals/references/signal-reading.md`: adds that a line remaining in a stronger draft, not being opposed, being judged `acceptable`, or receiving a neutral evaluation is not equivalent to positive confirmation; when provisional acceptability appears, preserve the current version and active alternatives for comparison, and do not write it into the long-term aesthetic profile.
- `explore-subtext-and-distance`: description adds triggers around character inference / unsupported knowledge; the body asks through what perceptual or information path an explanation is established for a character, while explicitly stating that the path does not need to be written as a full reasoning chain. A detail, bodily hesitation, wrong initial model or later correction may be enough.
- `workshop-dialogue-and-comedy`: description and body separate dialogue-local problems from AI fingerprint across narration / knowledge / scene scaffold; adds the check "does the question come from the speaker's own knowledge, desire or uncertainty, or is it only bringing out the next explanation for the reader?"

`shape-vn-rhythm-and-montage`, `review-vn-draft` and the newly built `rework-ai-shaped-fiction` are not changed again in this round. `stage-vn-presentation` and a long-form philosophical-debate specialist continue to wait for actual text and repeated failure; they are not pre-built merely because a possible use can already be imagined.

### Validation and Status

Retrospective use cases were added to `skill_prototypes/SMOKE_TESTS.md`, covering the high-density late-tea source, long character speech in Opening, Interface knowledge timing, late-tea local production budget and candidate-status boundary; no new independent Agent context was started, so this is not called a forward test.

The official `quick_validate.py` still fails at import because system Python lacks `PyYAML`. Equivalent checks with system Ruby passed for the frontmatter, directory name, description length, unfinished scaffold and local links of seven skills; prototype / installed versions of the new and three updated files are byte-identical, and `git diff --check` passed in both repositories.

No Writer OS Draft, development, presentation or `current.md` files were modified, and no `stage-vn-presentation` directory was created. Skill changes in the target project remained un-added and uncommitted.

## Calibration of Specialist-Loading Threshold for the Drafting Skill (2026-09-04)

The author wanted `draft-vn-scene-from-design` to read sibling skills more generously when related craft dimensions are connected, rather than taking token-saving as the first goal; he also accepted the boundary that not all siblings should be loaded by default.

On that basis, the subsection title was changed from `Consult craft guidance selectively` to `Consult craft guidance as needed`, and the earlier higher threshold of "read only when it will materially change this draft" was loosened: if specialist guidance has a clear relation to the current drafting problem, it may be read; it does not first have to be proven indispensable, and it need not be known in advance that it will change the resulting draft. When dialogue action, inference path, rhythm and AI-shaped regularity all operate at once, several relevant lenses can be combined. When two neighbouring skills are both relevant, read both and coordinate them rather than forcing an early single choice.

The rule "do not automatically load all siblings" is still retained, but token scarcity is not the reason. The official Skills documentation says Codex first sees skill names and descriptions, and only reads the full `SKILL.md` after selecting one; this progressive disclosure manages the current context. Official model guidance also warns that multiple unclear or competing skill instructions more strongly affect model behaviour. Pro gives a wider usage allowance, while official materials also state that actual consumption still varies with context, task complexity, reasoning and tools; it does not make irrelevant guidance useful context. The current rule is therefore: load generously inside a live scene problem; stop when the added guidance would only repeat existing judgement; and always return to the specific scene.

The modification was synchronised to the project-installed version in `distant-writing-project`; the two `SKILL.md` files are byte-identical. Ruby equivalent checks passed for frontmatter, directory name, description and local relative links, and `git diff --check` passed in both repositories. The official `quick_validate.py` still fails at import because system Python lacks `PyYAML`; it is not counted as a passing validation.
