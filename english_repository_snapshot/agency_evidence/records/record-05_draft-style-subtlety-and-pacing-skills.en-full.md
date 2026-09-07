# Draft Language Style, Subtle Tone and Rhythm Judgement: Skills Design Audit

Date: 2026-08-29

## Scope

This audit fixes its review to two continuous writing sessions from 2026-08-23 to 2026-08-28. At the time the review began, these were the materials in `agency_audit/traces/` that best matched the author's description of approximately five days involving Draft language style, subtle tone and rhythm. Newly generated traces after this point are not automatically included.

- `traces/recovered/01a02e7d-c329-7060-b5a4-d405b39a4100.recovered.jsonl`, recovered sequences 1-520, covering 2026-08-23 to 2026-08-26;
- `traces/2026-08-27/01a02e7d-c329-7060-b5a4-d405b39a4100-f20d97a3fef0.jsonl`, original sequences 470-504, covering the final segment of the same session on 2026-08-27;
- `traces/2026-08-27/01a04356-e61f-7383-99d0-d950918c445c-1614cb66438f.jsonl`, sequences 1-314;
- `traces/2026-08-28/01a04356-e61f-7383-99d0-d950918c445c-1614cb66438f.jsonl`, sequences 315-629.

The original captures for the same `01a02...` session under `traces/2026-08-23/`, `2026-08-25/` and `2026-08-26/` were specified and merged by the manifest of the recovered trace above. To avoid counting the old parser's missing messages and the reconstructed lifecycle twice, this semantic analysis uses the recovered trace. The original files serve only as recovery provenance and are not used as a parallel source for the main account.

## Capture Integrity and Evidence Boundary

- The lifecycle actor labels in the four selected files are complete; non-hook lifecycle records have no missing `turn_id`.
- In each file, the numbers of `assistant_tool_call` and `tool_result` records and their visible `call_id`s correspond one-to-one: 171, 9, 87 and 108 pairs respectively.
- Every PreCompact/PostCompact checkpoint has `/Users/[username]/Documents/distant-writing-project` as `cwd`; the `project/` Git snapshot is available, the branch is always `main`, and HEAD advances with writing commits. The commands for status, unstaged diff and staged diff in each checkpoint succeeded.
- The recovered trace contains one `capture_gap` from 2026-08-25: `transcript_identity_changed` caused the cursor to reset at that time and indicated that the original capture might contain duplicates. After offline recovery, the lifecycle was reparsed once from the raw rollout in physical order. The manifest shows that after the original final checkpoint there were only 255 bytes and no additional lifecycle. The recovered trace is therefore usable for this judgement, but it remains a reconstruction after the fact and should not be presented as native hook-time capture.
- The recovery manifest shows that the Desktop Markdown was used only to check the presence of messages: 32 of 35 user prompts matched, and 3 did not. Semantic judgement is based primarily on the recovered raw-rollout lifecycle, not on the Desktop Markdown as a whitelist for deleting or retaining messages.
- Here, only explicit judgements, choices, questions and corrections in the author's `user_prompt`s are attributed to the author. Agent suggestions, files read by tools and final written files are treated as response or result evidence; they do not automatically count as authorial judgement. Temporal proximity also does not automatically establish causality.
- The primary Draft that the trace explicitly operated on, `../distant-writing-project/writer_os/creative_work/drafts/开幕_流水冷开场_相撞与讲座.md`, was cross-checked in read-only mode. Its mtime was 2026-08-28 18:58:52 BST, close to the last PostCompact in the selected scope, 2026-08-28 17:59:26Z. It is used only to confirm reported formatting and sentence outcomes, not to replace user prompts or infer new decisions outside the trace.

## Review Progress

- Completed: source selection; checks of checkpoint, trigger, `cwd`, capture gap, actor, turn, tool pairs and Git snapshot.
- Completed: a sequential first pass through every user prompt in the four files, used to locate high-value sections.
- Completed: recovered sequences 116-520, with focus on the Opening, traffic montage, walking together and the first English Draft. Mechanical searches, repeated file reads and success receipts were skipped after checking event type and adjacent semantics; tool output itself was not treated as authorial judgement.
- Completed: original sequences 470-504, the late segment of the same session on 2026-08-27. Skipped: low analytical value. These three turns mainly dealt with a temporary write-down strategy before compaction and did not add concrete language aesthetics relevant to the present question. Their principle that provisional judgements require continued revision and should not be promoted into conclusions merely because they were written down is retained as a provenance boundary for the skill.
- Completed: new-session sequences 1-314, with focus on the Draft of walking together, the friend conversation and the author's sentence-level revisions. The actual written result was separately read against the current primary Draft.
- Completed: new-session sequences 315-629, with focus on the maid café Draft, narration / inner voice, language density, formatting and naming. If there were closing messages after sequence 629 not captured by that checkpoint, they are outside the fixed scope of this audit.
- Checked and provisionally judged low-value: recovered sequences 1-115 mainly involve repository-level AGENTS, docs, summary and compact-rule setup. Apart from possible effects on skill boundaries, such as "the Draft should default to being written directly in English" and "precise wording should return to the primary text", they do not enter this literary-language synthesis.
- Resolved as far as the current evidence allows: the author's term `Subtle` was not a fixed English label repeatedly used in the trace. It is operationally understood below as the question of how much readers should infer, when narration may name meaning on behalf of characters, and which ambiguities should be preserved. This audit does not claim that the author had given the term a unified definition.

## Judgement

### One: Rhythm Is Not the Amount of Dialogue or Total Word Count, but the Density Curve of Several Channels

1. The author accepted the overall quietness of the Opening and further pointed out that the collision and lecture were also quiet: characters spoke little, and most meaning was carried by narration, action, slides, traffic announcements and cuts (recovered sequences 347 / 352 / 365). At the same time, the author worried that if the traffic montage continued in the same quiet mode, the first chapter would lack internal variation; the friend conversation and the maid café were expected to provide contrast through different language density and comic texture (new-session sequence 18). The durable rule is therefore not "always keep dialogue low", but "do not solve rhythmic variation only by adding dialogue".
2. The author explicitly accepted progression through repetition: several traffic failures could be short cuts, one walk together could be extended, and a very short recurrence in which the train was normal but the two were again in the same carriage could then close the sequence (recovered sequences 147 / 190 / 196). The movement of encounter is not repeated information, but "seeing -> speaking -> walking together and exchanging names -> actively approaching". Repetition must change a condition, relational action or timescale.
3. The author corrected the prior assumption that every encounter had to include speech (recovered sequence 196), and did not want narration to define the meaning of early silence on behalf of the characters: at that moment, He Xuyuan did not necessarily "feel something" through the silence (new-session sequence 92). Action, crossing the road, being separated by a crowd, an announcement that does not come, and a pause that nobody fills can all be complete beats.
4. For the friend conversation, the author rejected using many fast short lines to create liveliness, because that would erase He Xuyuan's desire to explain. A more suitable option was to reduce turn switching and let him give medium-long statements interrupted by action pauses (new-session sequences 191 / 197 / 220). The author later stated explicitly that dialogue in a visual novel can be long and that "length is secondary" (sequence 462). Short sentences, short scenes and fixed word counts therefore cannot be treated as the project style.
5. In the four-person maid café scene, the author was worried in the opposite direction: if the two friends did not have enough language, the work had to be clearly aware that it was using third-person narration to represent or skip conversation, which would create a montage feeling (sequences 436 / 462). This means that omission is itself a perceptible formal choice. It cannot pretend to have no rhythmic consequences.

### Two: What Is Called Subtle Is Mainly About the Timing of Explanation and the Reader's Burden of Inference

1. The author repeatedly rejected language that was elegant at sentence level but completed a character's understanding too early. `He had checked the room twice. She had walked into the wrong one and stayed.` was judged unnatural in the walking section because it summarised the difference between the two characters too neatly (recovered sequence 446). `It still makes doing nothing feel unreasonable.` was also deferred until after the maid café, because the relationship at that moment had not yet created pressure to act (new-session sequence 177). These are not line-level elegance problems, but problems of semantic timing.
2. The author was alert to local action being upgraded into stable personality evidence. For the set of "she entered the wrong lecture but stayed; the subway broke down and they walked together; when it did not break down she still approached", the author thought it would be foolish to infer from this that Lulu would "choose contingency". What was more supportable was that He Xuyuan beautified low-probability repetition into fate urging him to act (recovered sequence 495). In other words, the work can present a character's projection, but should not quietly write that projection as certified by narration.
3. Subtlety does not mean mechanically deleting explanation. The second paragraph of the rice imagining explicitly gives "kitchen, night, Lulu sitting beside the table" and the fact that they do not yet have an arrangement to meet again. The author decided to keep it, because keeping only the first paragraph would leave a key relational transition to readers with strong close-reading ability (new-session sequence 555). Likewise, the author asked for the abstract logic of `absence of a common cause...formless` to be given another more direct cue for ordinary players (sequence 268).
4. When the action itself already performs the meaning, the author supported not announcing the reaction again: `Neither friend commented.` was eventually deleted. The absence of teasing is more natural than a sentence saying "nobody teased" (sequence 555 and adjacent revisions). What is needed is therefore an inference budget: when a meaning must be caught by an ordinary reader and changes plot understanding, it may need another layer of support; when the meaning is already clearly presented by action, position, pause or structure, it should not be summarised again.
5. The author allows a slight second reading. `what sort of place it was / Knowledge had not prepared him...` works both as "conceptual knowledge is not bodily experience" and as a light accommodation of the terminal AI's way of seeing. The author did not require the second reading to be made explicit (sequence 555). Intentional ambiguity and accidental obscurity therefore need to be separated.

### Three: Natural Dialogue Is Not a Button for "More Colloquial", but Is Produced by Context, Semantic Intensity and Character Syntax

1. The author judged `Was that the talk you came for?` slightly stiff because it sounded like checking an itinerary. Asking first about the lecture and then letting Lulu naturally say that she had entered the wrong room sounded more like real turn-taking (recovered sequence 443). This is a conversational-motive check, not only a lexical substitution.
2. The author continually checked whether wording was too written, too complete or too semantically intense: for example, questioning whether the three-part `my inability to wake up` sounded like ordinary speech; questioning whether `I looked at her and found the conclusion there` made an ordinary judgement too strong; and pointing out that `You used more infrastructure` was hard to understand (new-session sequence 244). At the same time, the author retained the character's right to say complex things. The issue is that complex speech should sound like this character thinking in the moment, not like a dissertation summary prepared by the author in advance.
3. The author did not accept a realistic conversation that repeated a four-item summary already known to the reader simply for the reader's sake (sequence 197), but did accept He Xuyuan narrating the full chain of events in order and gradually beautifying the structure as he spoke. Whether information is repetitive depends on whether it presents the character organising experience in the moment, not on whether the sentence is "efficient".
4. The author was sensitive to implied character facts after dialogue: an unanchored `her` followed by `Who is she?` could make readers think He Xuyuan regularly reported different girls to his friends; too strong a word such as `conclusion` would invent a very high threshold for romantic judgement (sequence 244). Line review therefore has to check pragmatic implication, not only literal meaning.
5. Character voices may remain uneven. He Xuyuan can be nerdy; friends need to be able to respond to niche discussion without becoming the author's all-purpose exposition devices. Their teasing should remain basically non-malicious and use compressed short turns to contrast with He Xuyuan's long unfolding explanations (sequences 143 / 156 / 191 / 220). Although `You omitted several relevant properties.` is nerdy, the author thought it did not necessarily need to be naturalised, because it might be exactly He Xuyuan's way of translating discomfort into missing parameters (sequence 555).

### Four: Comedy Should Be Able to Work Without Knowledge of the Reference, and Should Not Be So Dense That It Rewrites the Whole Scene's Texture

1. The author explicitly thought the old summary's "dense comic feeling" was bad (recovered sequence 495). When traffic failure, walking even after paying money, and four people being forced to cast a spell together already produce comic situations, characters do not need to say the punchline in full.
2. The author would still actively ask for "more jokes", but this was not unconditional piling-up. The *MyGO!!!!!* matcha parfait, the three-character explanation of `bishoujo`, and `Yuan Kai comes to raise a candidate` all had to be readable as independent action, character oddity or ordinary dialogue for players who did not know the source; readers who did know the source could get another layer (sequences 285 / 316 / 529 / 588).
3. The author tended to preserve functional foreignness or cross-cultural texture. The three Chinese-character dimensions of `bishoujo` were themselves a meaning device, and "people who do not understand can not understand" (recovered sequence 159). By contrast, ritual phrases could sometimes be directly translated into readable English without repeated original wording plus brackets (new-session sequence 316). This is a local judgement and cannot be generalised into "never add glosses".

### Five: Draft Channel Boundaries Need to Be Clear, but Ontological Ambiguity in the Narration Sometimes Has to Remain

1. The author first questioned whether presentation guidance such as the steady blur of traffic should enter narration, then immediately revised the judgement to "presentation can remain in the Draft" (new-session sequences 120 / 133). The final concern was not which file it appeared in, but whether players would mistake production / visual instructions for narrative voice.
2. The author then proposed light formatting requirements: spoken text, player-visible narration, inner speech and visual / sound instructions need to be distinguishable, but the author did not want excessive formatting (sequence 555). The whole Draft finally used four types: `Speaker`, ordinary player-visible narration, `Visual/Audio/Scene/Cut`, and a small amount of direct thought.
3. More importantly, the author pointed out that some ordinary narration might actually be disguised observation by a terminal AI or a reader perspective. If all inner speech and narration were forcibly labelled, the narrative mechanism would be explained too early (sequence 579, with conversion confirmed at sequence 588). The correct constraint is therefore not "explicitly tag every thought", but: add action or perception anchors only when a thought might otherwise be mistaken for that of another character; preserve an ordinary surface where the mixing of narrative layers is intentional.
4. Channel formatting also carries information timing: before a character reports a name, the speaker label should not reveal `Xuyuan / Lulu` to the player early. This is not pure layout, but control over player knowledge.

### Six: Judgement in Chat Must Be Read According to State; Not Every Question or Quotation Can Become a Style Rule

1. The author often used phrases such as "would it be", "is it", and "I feel" to raise diagnostic questions, and then accepted, withdrew or locally revised them. For example, presentation was questioned first and then allowed to remain in the Draft; the friend conversation was first called a "short conversation", and later the size assumption was cancelled and it was allowed to become longer than the walk. If a skill only captures keywords, it will create conflicting rules.
2. Several prompts contain long quotations from web ChatGPT. Only the parts that the author explicitly described as acceptable, endorsed or confirmed can be treated as ratification. The quotation itself remains external AI framing, not authorial judgement.
3. The author allowed development files to continue preserving provisional judgements and then be rewritten later, and opposed adding rigid rules merely in anticipation of compact (late segment of the same 2026-08-27 session, sequences 470-504). A single write-down, Agent suggestion or sentence such as "this can be discussed" therefore cannot be promoted automatically into a durable style rule.

## Provisional Analytical Propositions

1. **The author's stylistic agency mainly appears through delayed supervision and negative selection.** The Agent often first provided complete, neat and explainable language; the author then pointed out that it was "too early", "too strong", "too much like checking an itinerary", "too written", or implied wrong character facts. Counterevidence is that the author also extensively authorised the Agent to design cut syntax, draft English and accept wording. This is therefore not one-way correction, but a collaborative division of labour in which the Agent generates candidates and the author controls semantic timing and applicability boundaries. Another explanation is that this is ordinary editing. What is distinctive in this material is that judgement is distributed across multiple rounds of AI co-writing and compact recovery, and future skills must recover its state rather than merely copy final sentences.
2. **The project meaning of `subtle` is closer to "distribution of explanatory authority" than to "saying less".** The author both deleted summaries that completed characters' understanding too early and kept key transitions that ordinary readers might otherwise miss; he also allowed the terminal AI to disguise itself as narration. Counterevidence is that several judgements only concern the current Opening and may not apply to all worldlines or characters. Another explanation is that these are merely clarity revisions. Yet the question of who may explain, at what moment, and whether explanation turns projection into certified fact recurs across scenes, which supports its extraction as a reusable review mechanism.
3. **Rhythmic agency moves away from dialogue as the centre and towards multi-channel visual-novel composition.** The author initially acknowledged his own prior assumption that every encounter had to include speech, and later stably used sound, action, pause, cut, scene density and turn length together to regulate rhythm. Counterevidence is that the author still worried about insufficient language density, which means visual and sound channels cannot be used as an unconditional reason to delete dialogue. The more precise proposition is: dialogue is one rhythm channel among several, and every addition or deletion should clarify which channel takes over the function.
4. **Removing "AI flavour" cannot be implemented as uniform short-sentence reduction.** The author rejected polished punchlines, noun lists and mature summaries on the one hand, but on the other hand asked to restore He Xuyuan's long sentences, circling explanations and uneven expressive desire. An alternative explanation is that this is only a character-specific case. Future skills should therefore first identify character and scene function, then diagnose the felt quality of the writing; they should not make shortness, lightness or restraint the default voice of the whole project.

## Skills Proposal

The recommended structure is one evidence skill, three independently triggerable craft skills and one explicit integrated review skill. It is not recommended to stuff all the conclusions above into one large style prompt, or to create a permanent prohibition for every example sentence.

### 1. `co-writing-judgment-miner`

**Trigger:** The user asks to recover his own judgements from chat, trace, memo or revision history, or needs to update existing author preferences.

**Core responsibilities:**

- attribute to the author only explicit choices, refusals, corrections and ratifications in `user_prompt`;
- distinguish `confirmed`, `rejected`, `provisional concern`, `open candidate`, `quoted external view` and `superseded`;
- distinguish local scene judgement, character-specific rule and project-wide durable rule;
- preserve physical order for conflicting judgements and output "current semantic state + reason it remains valid", rather than placing old and new sentences side by side as two rules;
- only propose candidates for persistence; do not automatically write into Writer OS story state or skill reference without the author's confirmation.

**Output:** A short judgement ledger and a set of candidates marked as "recommended for promotion / keep local / still needs confirmation". Private trace paths and original lines remain in the audit layer; versions entering Writer OS or skill references retain only confirmed operational conclusions with provenance removed.

**Key anti-error tests:** The skill must recognise the supersession from sequence 120 to 133; it must not attribute the whole web ChatGPT passage in sequences 322 / 555 to the author; it must not turn "would this be too strong" directly into "always delete strong wording".

### 2. `subtext-and-distance-calibrator`

**Trigger:** The user says the text is too direct, too obscure, `subtle`, explanation comes too early, narration overreaches, emotion feels unnatural, or one sentence is "good but wrong here".

**Method:**

1. First state the one or two meanings that an ordinary reader must get from this passage, and any second-level meaning that can remain for rereading.
2. Mark whether the current meaning is carried by dialogue, action, narration, structural repetition, visual / sound cues, or another channel.
3. Check whether narration certifies a character's projection as fact, completes understanding that the character does not yet possess, or upgrades a local action into stable personality.
4. Run a deletion test: if the explanation is removed, can an ordinary attentive first-time reader still get the necessary meaning? Do not ask only whether a close reader can infer it.
5. Run an addition test: would an added sentence merely repeat the action, and would it damage a second-level reading on reread?
6. Output one of `keep / clarify / anchor / defer / delete`, and prioritise the smallest change. If the problem belongs to event order, move the sentence instead of polishing it.

**Boundary:** Do not treat "more subtle" as the highest aesthetic value. Do not decide intentional ambiguity on the author's behalf. Do not turn a local judgement into a global rule without plot-stage information.

### 3. `character-dialogue-and-comedy-calibrator`

**Trigger:** Dialogue is stiff, too written, AI-like, character voices converge, jokes are too dense or too complete, or cross-cultural terms / translationese need judgement.

**Method:**

- First ask why the character would say this sentence at this moment, rather than first replacing it with a colloquial synonym.
- Check whether question and answer really connect, and whether pronouns / reactions imply unwanted character history or relationship intensity.
- Check turn length, syntactic shape, interruption pattern and degree of active unfolding by character; prohibit uniform short-sentence reduction.
- Distinguish "the character is able to say complex things" from "the author has written a summary on behalf of the character". Complex argument should form during speech.
- Let jokes be completed first by situation, action or mismatch between two character logics. If the joke still works after the explanation is deleted, do not add another punchline.
- Apply a "dual-readable" test to reference jokes: the scene still works without source knowledge, and source knowledge adds a second layer.
- For `bishoujo`, mild translationese, direct ritual translation and similar cases, judge semantic and character effect only; do not flatten everything through one rule of naturalisation.

**Output:** For concrete turns, give "problem - implied consequence - minimal candidate", and note whether the issue concerns naturalness, voice, semantic precision or comedy density.

### 4. `vn-scene-rhythm-calibrator`

**Trigger:** Rhythm, pacing, montage, too quiet, too noisy, scene too short / too long, insufficient language density, dialogue turns or pauses.

**Method:**

- Establish a light beat map: the relational change, information change, main carrying channel and subjective reading speed of each beat.
- Observe dialogue turn count, individual turn length, action / silence, visual / sound event, cut, repetition and variation separately; do not use word count as a proxy for the whole rhythm.
- For repeated passages, check whether each occurrence changes a condition or relational action; for extended passages, check "why does the camera not cut away this time?"
- Place the target scene beside adjacent scenes to judge whether quietness, density or comedy creates effective contrast across the curve of scenes.
- When language density is low, state whether the answer is to add real exchange or to deliberately use narrative summary to create montage. When there is too much dialogue, state which non-dialogue channel takes over its function.
- Do not assume scenes should have equal length. Do not set permanent thresholds such as 1.4-1.7 times. The reusable principle behind the longer He Xuyuan friend conversation is "fewer switches, longer unfolding per turn", not a fixed word count.

**Output:** A small beat / density map and the highest-leverage adjustments. Only modify the Draft after the user authorises it.

### 5. `vn-draft-integrated-review`

**Trigger:** The user explicitly asks for integrated language review of an entire scene / chapter. Ordinary local wording questions do not automatically trigger the full check.

**Responsibilities and order:**

1. Read the current primary Draft, directly relevant development / story-state constraints, and confirmed author judgements. Do not load the whole chat.
2. Run semantic timing / subtext first, then scene rhythm, then dialogue / comedy. Decide meaning and position before polishing sentences.
3. Additionally check visual-novel channels: spoken text, player-visible narration, direct thought and `Visual/Audio/Scene/Cut` should not be misclassified; character name labels should not reveal information the player does not yet know.
4. For intentional mixture among ordinary narration, free indirect discourse and disguised terminal-AI observation, do not force narrator labels. Add perception or action anchors only when a passage may be mistaken for another character's thought.
5. Output an issue map, effective exceptions that should be retained, minimal patch candidates and questions still needing the author's decision. Do not rewrite whole passages for "unified style", and do not automatically turn temporary checks into permanent style rules.

### Shared Knowledge and Storage Boundaries

- The five skills share **methods**, not a repeatedly copied list of stylistic prohibitions.
- This Record preserves private evidence pointers. Raw traces, absolute paths and long web ChatGPT quotations do not enter Writer OS.
- Durable project tone / voice should still enter the relevant `story_state` or current development file according to the existing Writer OS rules, rather than being hidden in an Agent summary. Skills read these primary creative constraints at runtime.
- A short author-confirmed reference may be maintained for skills. It should include only operational judgements and their scope, for example "the Opening's narrative layer may allow terminal-AI disguise" and "He Xuyuan's voice may permit medium-long technical unfolding". It cannot replace story files, and it cannot universalise every local deletion or revision in the Opening.

### Implementation Order and Acceptance

1. Implement `co-writing-judgment-miner` first, using this trace as a regression sample. If it cannot correctly handle questions, external quotations, withdrawals and later confirmations, the knowledge source for the later craft skills will already be distorted.
2. Then implement the three craft skills, each with a narrow trigger. Do not implement the integrated skill first; use real problems already encountered in the Opening to test them separately.
3. Finally implement `vn-draft-integrated-review`, making it route among the first three rather than copy all their instructions.
4. Behavioural acceptance should not match fixed wording. It should at least check that the skill:
   - can preserve `steady blur` as a Visual cue, rather than deleting it by a universal rule against "presentation leakage";
   - can recommend deferring or deleting the premature summary `He had checked...`;
   - can both preserve the second paragraph of the rice imagining and delete `Neither friend commented.`, proving that it does not follow a universal "delete all explanation" or "keep all explanation" rule;
   - when faced with the friend-conversation rhythm problem, can reduce turn switches and extend the character's unfolding rather than mechanically adding short lines;
   - when faced with a quiet montage, can check sound, cut, action and variation rather than automatically adding idle chat;
   - can preserve the intentional ambiguity of terminal-AI disguised narration while preventing thought attribution from accidentally falling onto Lulu, Anna or Yuan Kai.
5. After these tests are stable, decide whether to make them into a project-level skill bundle. At present, immediate global installation is not recommended: these judgements are highly project-specific, and it is safer to try them first within the private project scope.

## Later Author Correction and Proposal Revision (2026-08-29)

After reading the analysis above, the author added four important corrections:

1. Comic references do not always have to work without knowledge of the source. Readability is a continuum affected by scale, frequency, surrounding atmosphere and the function carried by a given joke. The work may intentionally preserve jokes that are open only to some readers, or even do not work at all without background knowledge.
2. Aesthetic and feeling-oriented skills should not be written as prohibition lists. They should open thinking paths for the Agent, make tensions and possibilities visible, and still carry the skill's proper functions of recognition, analysis, comparison and execution.
3. The current trace is not enough to reconstruct the author's full aesthetic with high fidelity. Skills should accommodate current preferences, but mark them as an aesthetic profile that can continue to be revised, not as a completed style constitution.
4. The general tendency is to use montage as little as possible, in order to reduce reading fragmentation. Because this work has an unusual narrative mechanism, montage is expected to appear slightly more often than in an ordinary novel. This too needs contextual judgement and cannot become a numerical ceiling.

This correction does not erase the physical order of the previous text. It revises two over-strong generalisations:

- "Comedy should be able to work without knowledge of the reference" is only a common, low-risk design direction, not the author's universal requirement. A more accurate authorial tendency is to control the cumulative density and scene consequences of opaque references, rather than requiring every single one to be dual-readable.
- "Repetition must change a condition, relational action or timescale" can be a useful question when analysing whether repetition produces progression, but it is not a formal prohibition. Stasis, mechanical recurrence or deliberate absence of change may also work in a specific atmosphere.

### Whether the Five Skills Should Be Added to or Removed

At present, it is not recommended to add a sixth skill, merge any skill or delete any skill. The five items correspond respectively to evidence updating, explanatory space, character language, scene rhythm and integrated review; their trigger boundaries remain clear. What is really needed is renaming and rewriting of responsibilities:

| Original proposal | Revised name | Main change |
| --- | --- | --- |
| `co-writing-judgment-miner` | `trace-author-aesthetics` | It does not only recover decisions; it also maintains a changing aesthetic profile, tensions, exceptions and unknown areas. |
| `subtext-and-distance-calibrator` | `explore-subtext-and-distance` | It no longer calibrates the passage towards one correct interpretation; it unfolds several possible readings, the distribution of explanatory authority and their respective costs. |
| `character-dialogue-and-comedy-calibrator` | `workshop-dialogue-and-comedy` | It no longer treats "naturalness" or "dual readability" as hard thresholds; it compares different linguistic textures, openness of jokes and character effects. |
| `vn-scene-rhythm-calibrator` | `shape-vn-rhythm-and-montage` | It places the associative benefits and fragmentation costs of montage side by side, and adopts the revisable prior that this work tolerates slightly more montage than an ordinary novel. |
| `vn-draft-integrated-review` | `review-vn-draft` | It retains the integrated function, but adds a quick mode; it outputs optional paths and reasons for recommendation, rather than simulating an automatic scoring gate. |

A separate `author-preferences` skill should not be created, because it would overlap with `trace-author-aesthetics`. Authorial preferences should be continuously organised by the first skill, while the latter four read the same author-confirmed aesthetic profile during project-level use.

### Common Writing of the Skills

The five skills should retain only a small number of truly necessary operational boundaries, such as not misattributing external AI quotations to the author, not modifying the Draft without authorisation, and not promoting provisional judgement into a durable rule. The aesthetic parts should instead use the following structure:

- **Current tendency:** preferences repeatedly supported by existing material, while still having a scope of application;
- **Productive tension:** for example subtlety / readability, comedy density / atmospheric continuity, montage association / reading fragmentation;
- **Local exception:** valid only for a particular character, scene, narrative mechanism or reader layer;
- **Untested:** aesthetic areas that the current trace is still insufficient to judge;
- **Exploratory questions:** prompts that help the Agent generate and compare options, rather than rejecting options in advance;
- **Recommendation and action:** the skill must still give reasoned recommendations or candidate revisions, and cannot avoid work by saying that aesthetics are subjective.

The default output of the three craft skills can use:

1. what effect the current text is producing;
2. at least two reasonable development directions;
3. what each direction would strengthen, sacrifice or change;
4. a directional recommendation based on the current aesthetic profile;
5. the confidence range of the recommendation, and what context would reverse it.

This is a thinking path, not a fixed five-part template. Simple questions can still receive a direct one-sentence judgement and one candidate.

### Minimal Form of the Aesthetic Profile

`trace-author-aesthetics` should maintain a short, revisable `aesthetic-profile`. It does not attempt to "fully replicate the author", and should explicitly mark coverage gaps. At present, it can first include:

- an Opening that tends to be quiet but not homogeneous;
- permission for action, silence, sound and cuts to carry linguistic functions;
- alertness to explanation that comes too early or is too neat, while not making close reading the only route for necessary meaning;
- permission for character voices to be uneven, technical, circling or nerdy, without erasing individuality through uniform naturalisation;
- openness of comic references ranging from fully independently readable to intentionally opaque, with judgement depending on frequency, scene atmosphere, character relation and what is lost by readers who do not understand;
- general reduction of montage to avoid fragmentation, while the narrative structure of this work permits somewhat more frequent use than an ordinary novel;
- intentional seepage among ordinary narration, free indirect discourse and terminal-AI disguised observation.

Each item should be marked as "current tendency / scene-specific / needs more material". It should not use numerical confidence scores and should not attach long raw trace quotations. When updating from new traces later, revise this profile first instead of piling more rules into the skill body.

### Revision Scale for the Comedy Skill

`workshop-dialogue-and-comedy` no longer applies the "dual-readable test". It instead compares how a reference opens:

- works without needing the source;
- can be roughly felt as funny from current context, while the source adds another layer;
- is open only to readers familiar with specific cultural material;
- intentionally forms a private joke, group boundary or estrangement;
- does not work at the moment, but may work on rereading, verification or later callback.

The Agent should consider its cumulative frequency within one scene and adjacent scenes, whether it blocks important emotion, whether the character would naturally use it, and whether a reader who does not understand loses additional pleasure or necessary causality. These are observation dimensions, not a ranking from best to worst.

### Revision Scale for the Montage Skill

`shape-vn-rhythm-and-montage` should treat "as little as possible" as the author's current prior, not as a hard limit. Each time montage is considered, it can compare:

- whether it uses juxtaposition, repetition, compression across time or variation in conditions to produce an effect that an ordinary continuous scene would struggle to produce;
- whether the cumulative density of cuts gives readers too little time to re-enter character, space or emotion;
- whether adjacent material gives enough sustained scene for reading to land again;
- whether the montage serves this work's terminal AI, repetition structure or unusual narration, rather than merely skipping transitions that are difficult to write;
- whether intentional fragmentation is itself the target effect.

It should not set a number of uses, a proportion or a fixed recovery length. The idea that this work "may use slightly more" only changes the Agent's initial tolerance; it does not prove in advance that any given montage works.

### Quick Test Plan

Because time is limited, the first version will not do complete style fitting or multi-round independent evaluation. It uses one short smoke test:

1. Run `quick_validate.py` on the five skill folders, checking only structure, frontmatter and scaffold residue.
2. Use six existing fragments as behavioural tests. Each craft skill should be hit at least once, and the integrated skill twice:
   - opaque reference: should allow "not working without background knowledge", while discussing frequency and atmospheric cost;
   - rice imagining / `Neither friend commented`: should be able to give opposite treatments instead of applying one universal rule for deleting explanation;
   - `He had checked...`: should identify semantic timing and also state what later contexts might make it work;
   - friend conversation: should consider fewer turns and longer unfolding rather than uniform short sentences;
   - traffic montage: should see both fragmentation risk and the additional reasons supplied by this work's unusual narration;
   - terminal-AI disguised narration: should preserve intentional ambiguity and identify accidental attribution of thought.
3. In each example, check only four behaviours: whether more than one reasonable direction is opened; whether the current aesthetic profile is used without being presented as final certainty; whether an actionable recommendation is given; whether local exceptions are written as prohibitions.
4. Perform only one round of concentrated revision. If a failure comes from a shared problem among skills, revise the shared aesthetic profile or common writing method; do not add a new prohibition for a single example sentence.
5. After the smoke test is complete, the skills can be used in real writing. Later failures in actual use should revise them incrementally; there is no need to wait for comprehensive testing.

This test only verifies whether the first version can "think, compare, act and avoid rigidity". It does not claim to have captured the author's full aesthetic with high fidelity.

## Author's Addition on Question Functions and Further Revision of the First Skill (2026-08-29)

The author further pointed out that a question in writing does not necessarily express a negative evaluation of the Agent's sentence or design. It may mean:

- the author has not understood how the current choice works and wants the Agent to explain its reasoning;
- the author is not yet sure whether a better design exists and wants to reopen the option space;
- the author feels slight friction somewhere but cannot yet judge what the problem is;
- the author sees both the strengths and doubts of the current proposal;
- the author has a hard-to-grasp, uncertain and low-confidence meta-feeling about the current goal, his own preference or his own capacity to judge.

Therefore, `trace-author-aesthetics` still over-emphasises long-term aesthetic extraction and cannot adequately describe the first skill's immediate function. The final recommended name becomes:

### `interpret-co-writing-signals`

It does not extract one judgement from every question. It makes two levels of judgement.

**First level: interaction signal in the current turn**

By combining wording, self-correction inside the same prompt, adjacent context and later confirmation, it judges whether the author is currently mainly:

- requesting understanding or paraphrase;
- requesting explanation of the current choice's function and reasoning;
- requesting comparison of alternative directions not yet unfolded;
- reporting aesthetic friction whose cause has not yet been located;
- proposing a provisional counter-option;
- expressing real negative judgement or refusal;
- confirming, selecting or authorising implementation;
- expressing meta-uncertainty about the goal itself.

These are not closed labels, and a turn does not need to contain only one. `would recognising her immediately be a bit fast? Of course, it does save rhythm` can contain friction, acknowledgement of current function and a request for comparison at the same time.

**Second level: long-term aesthetic update**

Only when the author explicitly confirms, repeatedly shows the same tendency, makes a choice after comparison, or directly asks to save something should the skill consider updating `aesthetic-profile`. A single instance of not understanding, seeking explanation, lacking confidence or asking an open question does not generate a durable preference.

This order matters. If the prompt is read first with the goal of "aesthetic extraction", the Agent will tend to crystallise uncertainty into rules too early. If the interaction function is understood first, the Agent can help the author continue thinking without announcing the author's preference on his behalf.

### Response Postures for Different Signals

- **Requesting understanding / reason:** first explain what the current choice is doing and why it might be written this way. Do not automatically treat a request for explanation as a request for revision.
- **Requesting alternative directions:** preserve the current option as one candidate, then unfold a small number of genuinely different directions and their costs. Do not infer that the current option has failed merely because the author asked.
- **Unlocated friction:** propose several possible causes and distinguish them through textual evidence, helping the author confirm which one applies instead of rewriting immediately.
- **Provisional counter-option:** compare what it and the current option would each change. Do not promote the author's tentative idea automatically into a decision.
- **Real refusal / confirmation:** only then enter candidate elimination, implementation or long-term recording.
- **Meta-uncertainty:** acknowledge that the goal is not yet stable, and help the author unfold "I do not know what I want" into smaller perceptible and comparable questions. The skill may give an opinionated temporary recommendation, but should not interpret the author's low confidence as abandonment of aesthetic authority.

If the current signal remains ambiguous, the low-cost default response is: first explain the current option; give one meaningfully different alternative direction; and state what preference would reverse the choice. This usually serves both understanding and exploration without first asking the author to classify his own question.

### Internal Skill Resources

The first skill can use two short references rather than placing everything in `SKILL.md`:

- `references/signal-reading.md`: prompt interaction functions, common mixed signals and response postures;
- `references/aesthetic-profile.md`: the current, revisable author aesthetic profile.

The former helps the Agent handle "how to respond in this turn"; the latter helps the craft skills handle "what this project tends to choose". They cannot replace each other.

### Effect on the Five-Skill Structure

There is still no need to add a sixth skill. Keeping "signal interpretation" and "aesthetic profile update" in the same skill can prevent the second skill from extracting preference directly when it has not correctly understood the question. The revised five skills are:

1. `interpret-co-writing-signals`
2. `explore-subtext-and-distance`
3. `workshop-dialogue-and-comedy`
4. `shape-vn-rhythm-and-montage`
5. `review-vn-draft`

### Corresponding Adjustment to the Quick Tests

The total number of tests remains six, adding no extra time burden, but they are redistributed:

1. Use the change in `presentation` from sequence 120 to 133 to test that the first question is not directly recorded as "presentation must not enter Draft", and that the later correction changes the current state.
2. Use `would recognising her immediately be a bit fast? Of course, it does save rhythm` to test a mixed signal: the skill should explain the current speed's function and offer the two directions of holding one beat or direct recognition, rather than announcing the author's refusal.
3. Use the rice imagining / `Neither friend commented` to test explanatory scale.
4. Combine opaque reference and friend long conversation to test comedy openness and character language.
5. Use traffic montage to test associative benefit, fragmentation cost and this work's higher tolerance.
6. Use terminal-AI disguised narration as an integrated test, checking intentional ambiguity, accidental attribution and aesthetic-profile use.

The six examples together cover the first skill and the four craft / integrated functions. There is still only one concentrated revision pass.

### Granularity Correction: Signals Belong to Semantic Units Inside a Prompt

The "current-turn interaction signal" described above is still too coarse-grained. The author's precise addition is that what needs to be distinguished is not which category the whole turn or whole prompt belongs to, but what each sentence, clause, evaluation after quotation or adjacent semantic unit inside the same prompt is doing.

The first skill therefore uses three levels of reading:

1. **Semantic-unit level:** split by actual discourse function, not mechanically by full stops. Identify whether each sentence or clause is requesting explanation, reporting non-understanding, acknowledging an existing strength, searching for alternatives, expressing friction, testing a counter-option, refusing, confirming, or expressing meta-uncertainty. A semantic unit may also perform two functions at once.
2. **Prompt-combination level:** reconstruct the relation among these units, for example "first acknowledging the current function, then questioning its cost", "quoting an external view and then confirming only part of it", or "proposing a counter-option while keeping the original option for comparison". The Agent's actual response should integrate at this level, rather than mechanically answer sentence by sentence.
3. **Cross-prompt update level:** combine later confirmation and repeated tendencies to judge whether any content is sufficient to enter current working state or `aesthetic-profile`.

Therefore the skill cannot label a whole prompt simply as `critique`, `question` or `approval`. Especially in a long prompt:

- not understanding one sentence does not invalidate adjacent agreement;
- testing a local option does not automatically overturn a design already confirmed in the same prompt;
- one instance of meta-uncertainty does not mean the whole prompt has no clear decisions;
- long external quotations, the author's evaluation of quotations and the author's own new directions must be read separately.

The default behaviour of `interpret-co-writing-signals` should be to complete this fine-grained distinction internally first, then give a coherent response. Unless the analysis itself is the task, it does not need to show the author a table of labels.

The second quick-test example is revised accordingly: it should not only judge the whole sentence `would recognising her immediately be a bit fast? Of course, it does save rhythm` as a "mixed signal". It must separately preserve the friction that the speed may be too fast and the affirmation that direct recognition has rhythmic economy, then compare the two. Sequence 555's long prompt can also be used to check whether the skill compresses confirmation, questions, external quotations and retain-decisions into one overall attitude. This does not increase the number of tests and can be combined with the second example.

## MVP Skills and Smoke-Test Implementation Results (2026-08-29)

The author authorised testing to begin and added a methodological requirement: a skill that needs to identify problems from large amounts of text cannot be tested only on pre-extracted short target fragments. Future actual invocation may also be local, over one paragraph or a few paragraphs. The test must therefore cover both long-range autonomous locating and short-range local routing.

### Prototype Scope

Five uninstalled prototypes were created in `skill_prototypes/`:

- `interpret-co-writing-signals/`
- `explore-subtext-and-distance/`
- `workshop-dialogue-and-comedy/`
- `shape-vn-rhythm-and-montage/`
- `review-vn-draft/`

The first includes `references/signal-reading.md` and the shared `references/aesthetic-profile.md`. The other craft skills read this profile inside the current bundle; it is still explicitly marked as an incomplete initial profile mainly derived from the Opening.

These prototypes were not installed into the Codex skills directory. They do not change the automatic invocation behaviour of the author's everyday sessions, and they did not modify the Writer OS Draft.

### Structural Validation

The official `quick_validate.py` could not start in the current system Python because the `PyYAML` dependency was missing. This is not a skill validation failure. After reading the validator source, the main Agent reproduced its frontmatter, allowed-field, naming, length and unfinished-TODO checks using system Ruby YAML; all five passed. The dependency gap is retained as a limitation, and the equivalent check is not presented as a successful run of the official script.

### Input Scale

- The full user prompt for sequence 555: approximately 2,000 characters, containing multiple quotations, confirmations, questions, candidates and overall evaluation;
- the full primary Draft: 595 lines, 19,055 bytes;
- the complete Mallowbell Maid Café scene: approximately 270 lines;
- two local prose sentences: used only for minimal routing and local explanation tests.

Thus, this round was not a regression using six short sentences. Three initial tests required the Agent to locate material autonomously from a full prompt or full Draft; the maid café test required autonomous selection from a complete scene; local fragments only tested whether future small-scope invocation would over-trigger.

### Six Results

1. `interpret-co-writing-signals` passed the fine-grained reading of a long prompt. It split sequence 555 into semantic units concerning naming, formatting, narration, rhythm, spatial continuity, retain-decisions and overall evaluation, distinguished understanding / comparison requests, mixed judgement, local confirmation, candidates and the only explicit decision to "keep the second rice paragraph", and did not turn every `would it be` into revision authorisation.
2. `explore-subtext-and-distance` passed autonomous locating on the full Draft. Besides the historically discussed The Pattern and rice fantasy, it independently found that the Opening twice has narration defend Xuyuan as "not stalking" in a way that may over-argue, and identified `Rice is usually treated as whatever happens underneath the answer.` as an unusual but probably retainable character expression.
3. `shape-vn-rhythm-and-montage` passed on the full Draft. It did not count cuts, but identified the three bad mornings as the most effective montage, The Walk and Mallowbell as necessary landing points, the stacking of "performance - retelling - explanation" in The Pattern, and the potential fragmentation of entering cross-week compression immediately after the Talk.
4. `workshop-dialogue-and-comedy` passed on the complete maid café scene. It separately selected the *K-ON!* source correction and the long rice passage, allowed the former to open an extra layer only for informed readers, and pointed out that the latter's meaning depends on the whole passage's progression and should not be split into an independent punchline.
5. `review-vn-draft` exposed a real failure in the first test: although the output was usable, it loaded the full 717-line development file, causing `fast review` to lose its speed function and potentially be contaminated by existing design conclusions. After revision to the default scope of Draft plus aesthetic profile, the key retest did not expand into development / story state, but still gave the strongest effect, three high-leverage tensions and one minimal A/B read-aloud step. The reported input tokens fell from 202,584 to 69,630; the absolute number includes runtime context, and is used only for relative comparison within the same test.
6. The minimal routing simulation for the five descriptions passed. Faced with two rice-fantasy sentences and the author's local request about "too complete as explanation / worried it will become unreadable if deleted", the Agent selected only `explore-subtext-and-distance`; it did not additionally invoke `interpret-co-writing-signals` because of uncertainty in the prompt, and did not trigger full-draft review.

### Concentrated Revision and Key Retests

- `interpret-co-writing-signals` added a precise trace-reading strategy: first read the full target prompt, and expand to related user / assistant messages only when reference, state or supersession cannot be judged locally. The retest actually read sequence 555 and supplemented only 529, 553, 556 and 577; it did not read tool results or the Draft.
- `review-vn-draft` separated fast / deep context loading. The retest fully read the 595-line Draft and the shared profile, without reading development or story state.
- After the two changes, the equivalent structure validation passed again. The other four skills did not show problems requiring additional example-specific prohibitions.

Full reproducible cases and results are recorded separately in `skill_prototypes/SMOKE_TESTS.md`.

### Still Not Covered

- Because the prototypes were not installed, this round did not test real product-level automatic discovery / implicit invocation. Frontmatter routing simulation can only test the discriminating force of names and descriptions.
- The current material is still biased towards the Opening, Xuyuan and the early relationship. This round's pass should not be upgraded into validation for later worldlines, action, horror, sustained tragedy, choice text or other character voices.
- The smoke test proves that the first version can "locate autonomously, compare and act without rigidity" across long and short input. It is not a high-fidelity replication of the author's aesthetics.

## Production Wording Review and Cross-Skill Routing (2026-08-29)

After the smoke test, the author reviewed the skill text item by item and proposed the following corrections:

- skills should not preselect `end AI` or `terminal AI` as the translation of the story concept; they should describe the observational function currently carried by that narrative role;
- this character is hidden behind a seemingly third-person, near-omniscient narrative surface, but may still misinterpret phenomena;
- `when attribution remains usable` may make the requirement too narrow, because the work may not always want readers to identify the source of a sentence precisely;
- "long explanation / prepared summary" is not a simple good-or-bad judgement, and the different possible effects should be unfolded;
- `review-vn-draft` does not need a default Fast Mode, `up to three`, or other numerical quotas;
- several craft skills overlap; the integrated skill can remain, but should borrow specialised skills selectively instead of copying all methods or loading everything by default;
- production skill instructions should not contain test language. Test terminology can remain in the separate `SMOKE_TESTS.md` and this Record.

### Functional Description of the Narrative Role

The skill references now use:

> a fallible character concealed behind an apparently third-person, near-omniscient narrative surface

They also state clearly that the near-omniscient surface does not make this character's interpretation an infallible fact, and does not equal authorial judgement. Both `end AI` and `terminal AI` have been removed from the production skill files. Earlier appearances of the discussion term "terminal AI" remain in the Record as part of the historical layer and are not rewritten back into the past.

Original sentence:

> Ordinary narration, free indirect discourse, and disguised end-AI observation may intentionally permeate one another when attribution remains usable.

It has been changed to emphasise the degree of orientation required by the scene, rather than precise attribution at all times:

> Ordinary narration, free indirect discourse, and observations from a fallible character concealed behind an apparently third-person, near-omniscient narrative surface may intentionally permeate one another. Local cues need only preserve the degree of orientation the scene actually requires; the reader need not always identify the source exactly.

This allows the three surfaces to intentionally seep into one another, while still requiring enough orientation when a scene depends on character knowledge, emotional attribution or a difference in misreading.

### Tension Around Long Explanation

`resemble a prepared authorial summary` is not inherently bad, but the old wording could pre-code "sounding like an author summary" as a defect and confuse `authorial` with `authoritative`. It has been changed to:

> Long explanation can reveal thought in motion, crystallise it into a compelling self-account, or sound more settled and authoritative than the character's understanding has earned.

All three effects may be valid: displaying the formation of thought, letting the character form a persuasive self-account, or making language more mature than the character's current understanding has earned. The skill's work is to judge which one is happening in the current scene and whether it is the effect the author needs.

### Integrated Review and Specialised Skills

`explore-subtext-and-distance` is not merged with `review-vn-draft`. The former handles explicit problems of explanatory timing, distance, attribution and subtlety; the latter is invoked only when the interaction among several dimensions is itself the task. Other craft skills are also allowed to retain a small amount of shared operational principle, because a single invocation may load only one of them.

To reduce method repetition, `review-vn-draft` now:

1. first performs an overall reading;
2. when a high-consequence problem clearly falls into one dimension, selectively reads the corresponding sibling skill: `explore-subtext-and-distance`, `workshop-dialogue-and-comedy` or `shape-vn-rhythm-and-montage`;
3. reads `interpret-co-writing-signals` only when mixed signals in the user's prompt actually change the task boundary; ordinary hesitation alone does not trigger it;
4. returns to the integrated level to handle conflicts among locally good choices, visual-novel text / presentation channels, timing of player knowledge, and the way the fallible hidden observer's possible misinterpretation acts across dimensions.

Here, "selective invocation" is implemented at the skill-file level as selective reading of sibling `SKILL.md` files. It cannot guarantee a new system-level invocation during product runtime, so the instruction wording does not present it as a platform mechanism.

### Deleting Fixed Patterns and Test Language

- `review-vn-draft` has deleted default Fast Mode, `up to three` and the fast / deep binary.
- It still starts from Draft plus aesthetic profile, and only narrowly reads development / story state when a concrete judgement lacks necessary constraints. This is a context-relevance rule, not Fast Mode.
- In `workshop-dialogue-and-comedy`, `Do not test this skill only...` has been changed into actual runtime guidance for choosing long / short scope.
- Production `SKILL.md` files and shared references no longer contain `test`, `fast`, `end-AI`, `up to three` or `when attribution remains usable`. Test terminology remains only in test records.
- Other quantity-implying language such as `few / small set / minimum number` has also been removed from craft output requirements, letting the material decide the number of observations and revisions.

### Clarification of Test Running Method

The previous six examples and key retests were run by independent `codex exec --ephemeral` processes. They were new, separate Codex threads / contexts, and explicitly read the prototype skill paths. They were not sub-Agents created from the current main thread through the collaboration API, and they were not real automatic invocation after installation. Separate contexts prevented the evaluations from directly inheriting the main-thread conclusions, but each run still carried its own system and project context and therefore had obvious token overhead.

## Implicit Trigger Calibration and Project-Level Migration (2026-08-29)

The author worried that `interpret-co-writing-signals` had too high a reading threshold inside integrated review, and also asked about the relationship among ordinary prompts, explicit skill names and automatic triggers. According to the official Codex skills documentation, a skill's `name` and `description` enter context first; Codex can select it implicitly by description, and the user can also explicitly specify it in an ordinary prompt with `$skill-name`. Explicit specification is insurance when a method definitely needs to be used, not a prerequisite for everyday use.

Two small calibrations were therefore made:

- the description of `interpret-co-writing-signals` moves sentence-level / clause-level postures and their consequences forward. Its trigger object is explicitly a prompt that simultaneously contains signals such as explanation request, uncertainty, local approval, alternative, criticism or decision. Ordinary unambiguous instructions do not need additional signal analysis.
- `review-vn-draft` no longer reads it only when mixed signals "change the assignment". It reads it when different semantic units affect what the review should explain, compare, retain or revise. A local question with an otherwise clear task can still be handled directly.

### Real Implicit Invocation

After the five skills were moved into the target project, a new `codex exec --ephemeral` was started from the project root with an ordinary Chinese co-writing prompt. The prompt did not mention `$skill-name`, any skill name or any request for invocation. It simultaneously expressed: the design of "characters being silent" was not being rejected; the author wanted to understand the current reason; the author was uncertain whether a better choice existed; the author accepted the sense of distance; but worried that the scene was too cold; and if the current version worked, it did not need to be changed merely to respond.

Codex automatically read:

1. `interpret-co-writing-signals/SKILL.md`;
2. `explore-subtext-and-distance/SKILL.md`;
3. the two required shared references, `aesthetic-profile` and `signal-reading`.

It did not load the other three skills. The final answer did not interpret doubt or low confidence as refusal or authorisation to revise. It first explained the conditions under which silence works, distinguished two kinds of "cold", compared non-verbal response, answering beside the question, unfinished utterance and delayed response as directions, and stated what contexts would overturn the current tendency. This shows that the current description can be implicitly hit by one natural Chinese input, and that sibling selection has relevance. It remains heuristic selection and is not guaranteed by a single test.

### Installation Location

The five skills have been moved into:

`/Users/[username]/Documents/distant-writing-project/.agents/skills/`

They use repository-level `.agents/skills`, rather than global `$HOME/.agents/skills`, because these skills depend on this project's incomplete aesthetic profile, narrative structure and sibling relative references. Project-level discovery can work from the repository root and its subdirectories while avoiding accidental triggering in other writing or code projects. The five `SKILL.md` files, two references and prototypes in the target directory were rechecked item by item for consistency in frontmatter, skill names and local links. Smoke tests and this audit record were not copied into the production project.
