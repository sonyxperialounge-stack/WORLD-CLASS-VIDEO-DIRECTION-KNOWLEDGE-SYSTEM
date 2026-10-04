# Failure Modes, Isolation Tests and Repair

**Purpose:** Provide a symptom-to-cause-to-test-to-repair reference across the whole craft, teach isolation tests that separate the contributions of story, picture, sound, graphics and music, and give a diagnosis sequence that tests fundamental causes before adding effects.

**Applies to:** Rough-cut reviews, fine-cut problems, client notes that resist fixing, and final reviews.

**Prerequisites:** Familiarity with the craft chapters it links to; [Creative Coherence and Taste](../FOUNDATIONS/Creative-Coherence-and-Taste.md) for the whole-piece view.

---

## 1. Diagnose before you treat

When something is wrong, the instinct is to add: more music, more grade, more motion, more cuts. Most failures are not caused by a lack of treatment; they are caused upstream — a missing story question, a weaker performance, an unclear viewer contract. Treating downstream symptoms with more processing often makes the piece *more* polished and *less* effective.

**Diagnosis sequence** `[Heuristic]` — test the cheapest, most fundamental causes first:

1. **Intent:** Is the one-sentence intent clear and still right? ([Creative Brief](../FOUNDATIONS/Creative-Brief.md))
2. **Story:** Is there a central question, a causal chain, a payoff? ([Story Architecture](../STORY/Story-Architecture.md))
3. **Performance and truth:** Are the chosen moments truthful and alive? ([Performance Editing](../EDITING/Performance-Editing.md))
4. **Structure and pacing:** Does density vary purposefully? ([Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md))
5. **Picture:** Composition, continuity, attention, grade. ([Continuity and Attention](../EDITING/Continuity-and-Attention.md), [Creative Grading](../COLOR/Creative-Grading.md))
6. **Sound:** Dialogue clarity, design, music function, mix. ([Mix Strategy](../AUDIO/Mix-Strategy.md))
7. **Text and graphics:** Hierarchy, timing, readability. ([Design System](../MOTION-DESIGN/Design-System.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md))
8. **Finishing and delivery:** Texture, encoding, versions. ([Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md))

## 2. Isolation tests

Each test removes or isolates one layer, so its contribution becomes visible. None proves overall quality; each reveals something specific.

| Test | How | What it isolates | What it cannot prove |
|---|---|---|---|
| Story-only outline | Write the piece as a list of beats in plain sentences; read aloud | Whether the structure makes sense without craft | Whether execution delivers it |
| Picture without sound | Watch muted | Visual storytelling, information density, attention flow, muted-viewing readiness | How sound changes emotion and pace |
| Sound without picture | Listen with the screen covered | Dialogue intelligibility, sonic narrative, music shape, mix balance | Visual comprehension |
| Graphics removal | Disable all text and graphics | Whether the footage carries the story; whether graphics are crutches or necessities | Whether muted viewers can follow |
| Music removal | Mute music | Whether emotion is earned by material; whether music is masking a weak payoff | How the finished piece will feel with music |
| Music substitution | Try a contrasting track | How strongly the current music shapes interpretation | Which music is "right" |
| Fresh-viewer comprehension | Show to someone unfamiliar; ask specific questions | Clarity, recall, perceived intent | Audience-wide response (small samples) |
| Device checks | Watch on phone, laptop, TV, projector | Legibility, mix translation, colour translation | Every device |
| Reverse/slow review of cuts | Frame-step at edits | Mechanical errors (flash frames, jumps) | How the cut feels |

**After isolated repairs, watch the integrated piece again.** Fixing layers in isolation can break their interaction — a cut that now works silently may land against the music differently; a quieter music bed may expose a slow section.

## 3. Symptom → cause → test → repair matrix

| Symptom | Likely causes | Test | Repair | Owner chapter |
|---|---|---|---|---|
| Technically clean but generic | No specific intent; templates; references copied at surface level | Story-only outline; ask "what is only true of this piece?" | Re-derive choices from intent; translate references by function; remove template elements | [Reference Analysis](../FOUNDATIONS/Reference-Analysis.md), [Creative Coherence and Taste](../FOUNDATIONS/Creative-Coherence-and-Taste.md) |
| Excessive beat syncing feels mechanical | Every cut on the grid; no hierarchy | Music substitution or removal: does the cut still feel shaped? | Let action decide most cuts; reserve sync for accents | [Cut Decisions](../EDITING/Cut-Decisions.md#10-counterexample-and-repair--the-mechanical-beat-synced-product-montage), [Music Editing](../AUDIO/Music-Editing.md#5-beat-aligned-and-offbeat-cutting) |
| Unmotivated camera movement | Movement to avoid static frames; gimbal habit | Picture without sound: does each move reveal, follow or change proximity? | Lock off; motivate moves; reserve for key moments | [Motivated Movement](../CAMERA/Motivated-Movement.md) |
| Generic lower thirds | Templates; no relation to piece | Graphics removal: does anything feel lost? | Design from the piece's character; restraint | [Design System](../MOTION-DESIGN/Design-System.md#7-worked-example-1--a-restrained-interview-lower-third-hypothetical-project-a-second-shift-25-fps-19201080) |
| Mismatched texture between cameras | Different noise, sharpening, compression | A/B cuts at full speed | Texture matching; common grain | [Texture and Post Relighting](../COLOR/Texture-and-Post-Relighting.md) |
| Music fighting dialogue | Dense arrangement in voice range; level; wrong track | Sound without picture at low volume | Arrangement first; automation; sparser music | [Mix Strategy](../AUDIO/Mix-Strategy.md) |
| Unreadable captions | Speed; placement; contrast; small size | Device check muted; reading-rate calculation | Re-chunk; reposition; contrast system; edit to breathe | [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |
| Overprocessed voices | Aggressive noise reduction; gating | Sound without picture on headphones | Back off processing; room-tone bed | [Recording and Cleanup](../AUDIO/Recording-and-Cleanup.md#9-counterexample-and-repair--the-robotic-interview) |
| Weak opening promise | No question; slow orientation; misleading hook | Fresh viewer at the 10–20% mark: "what is this about?" | Move a genuine question earlier; state the promise | [Story Architecture](../STORY/Story-Architecture.md), [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md) |
| Missing payoff | Setup not planted; ending relies on music | Music removal: does the ending still feel like an ending? | Plant setups; fix the story's answer | [Story Architecture](../STORY/Story-Architecture.md), [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md#52-endings-that-feel-earned) |
| Emotionally flat polish | Performance chosen for fluency; emotion imposed by music and grade; no silence | Music removal; performance review against full takes | Choose truthful moments; protect pauses; reduce imposed emotion | [Performance Editing](../EDITING/Performance-Editing.md), [Perspective and Silence](../AUDIO/Perspective-and-Silence.md) |
| "Too slow" | Repetition; low information density | Intensity map; fresh-viewer "where did you drift?" | Remove repetition; restructure | [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md) |
| "Too fast / didn't get it" | Comprehension outpaced | Timed recall questions | Pauses after concepts; remove secondary information | [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md) |
| Viewers feel manipulated | Imposed emotion; misleading order | Music removal; source-context check | Truthful order; restraint | [Story Architecture](../STORY/Story-Architecture.md#11-counterexample-and-repair--the-misleading-reorder) |
| Geography confusion | Axis crossing; eyeline mismatch | Fresh viewer sketches the room | Neutral shot; motivated crossing | [Continuity and Attention](../EDITING/Continuity-and-Attention.md#12-counterexample-and-repair--the-accidental-axis-crossing) |
| Graphic looks pasted on | Missing blur, grain, colour match; ambiguous relationship | Full-speed on large display | Decide overlay vs presence; match cues | [Integration and Data Graphics](../MOTION-DESIGN/Integration-and-Data-Graphics.md#6-counterexample-and-repair--the-pasted-on-graphic) |
| Image looks wildly contrasty in grading | Double transform | Trace transforms | Remove duplicate transform | [Color Management](../COLOR/Color-Management.md#8-counterexample-and-repair--the-double-transform) |
| Flicker in footage | Light/shutter mismatch | Frame-by-frame brightness check | Deflicker; reshoot with safe shutter | [Capture Decisions](../CAMERA/Capture-Decisions.md#6-light-flicker) |
| Sync drift | VFR; sample-rate or rate mismatch | Check sync at start/middle/end | Conform; re-sync | [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#variable-frame-rate-sources) |
| Wrong version delivered | Naming/matrix failure | Reconcile matrix with folder | Discipline; superseded folders | [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md) |
| Generated element "feels off" | Temporal or physical inconsistency | Full-speed on large display | Reject; conventional alternative | [Generated Media QC](../AI-WORKFLOWS/Generated-Media-QC.md) |
| Loudness QC failure | Wrong target/method | Measure per spec | Remix for destination | [Audio Delivery](../DELIVERY/Audio-Delivery.md) |

## 4. Worked example 1 — "It's not working": diagnosing an early brand-film cut (hypothetical, Project B, 90-second film, v02)

**Reviewer notes:** "Beautiful but I don't feel anything." "Too long." "Maybe the music?"

| Step | Test | Finding (hypothetical) |
|---|---|---|
| 1. Intent | Re-read brief | Intent: viewers feel Arc comes from a real person's concern |
| 2. Story | Story-only outline | The outline reads: workshop → prototypes → product macro → Dev on design → family story at 1:05 → logo. The motivation arrives late; the first minute is "how", not "why" |
| 3. Performance | Compare chosen founder takes with full interview | The cut uses fluent pitch lines; the hesitant family story is trimmed to 8 seconds |
| 4. Music removal | Mute music | Without music, the first minute is visibly a sequence of beautiful shots without a question; with music, it "feels like an ad" |
| 5. Picture without sound | Muted | Product macros dominate; Dev's face appears late |

**Diagnosis:** the problem is story order and performance selection, not music or grade.

**Repair:** restructure so the family story (with its hesitation) opens the second beat (around 0:12), the prototypes become the "but" of the causal chain, and product macros are cut by half (see [Story Architecture](../STORY/Story-Architecture.md#10-rough-cut-diagnostic-for-beautiful-but-shapeless-material)). Music re-edited afterwards, not replaced.

**Verification:** fresh viewers asked "why did Dev make Arc?" can answer; "too long" notes disappear even though duration is unchanged.

## 5. Worked example 2 — An emotionally flat scene (hypothetical, Project D)

**Note:** "The key reveal doesn't land."

| Step | Test | Finding |
|---|---|---|
| Story | Outline | The setup (Ravi's pocket) exists |
| Picture without sound | Muted | The insert of Ravi touching his pocket is only 12 frames — easy to miss |
| Performance | Takes review | Nisha's reaction uses take 3 (composed) |
| Sound | Audio-only | A music cue swells at the reveal, telling the emotion before Nisha shows it |

**Repairs:** lengthen the pocket insert and add a second subtle one earlier; use Nisha's take 5 reaction; remove the swell — reduce ambience instead (see [Perspective and Silence](../AUDIO/Perspective-and-Silence.md#7-worked-example-1--designing-the-key-reveal-silence-hypothetical-project-d-23976-fps)).

**Verification:** fresh viewers anticipate "something in his pocket" and describe Nisha's re-evaluation.

## 6. Counterexample and repair — treating a story problem with effects

**Hypothetical counterexample.** A nonprofit film "feels flat" in review. Over three rounds the team adds a grade with more contrast, a bigger music cue, drone shots and animated statistics. Each round looks more expensive; reviewers still say "flat". Budget runs out.

**Diagnosis (late):** a story-only outline reveals that the film never shows a single person's changed situation — it is a list of activities. No amount of treatment creates stakes.

**Repair:** find the one beneficiary whose story the footage already contains (a farmer interviewed briefly); restructure around her before-and-after; cut the drone shots and half the statistics.

**Lesson:** run step 2 of the diagnosis sequence before spending on steps 5–8.

## 7. Stopping criteria

Diagnosis and repair can continue forever. Stop when:
- The brief's key objectives are met (verified with fresh viewers or stakeholders as appropriate).
- No material defect remains (technical, factual, accessibility, rights).
- Further changes show diminishing returns (each round's improvements are small and disputed).
- Stakeholders understand the remaining trade-offs.
- Delivery gates pass.

Remaining artistic disagreement is not automatically a failure; record it and decide by the approval owner.

## 8. Micro-decisions

- Run music removal on every piece at least once before final mix.
- Keep a "symptom log" across reviews; repeated symptoms point to an upstream cause.
- When a fix in one layer seems to require changes in many others, suspect an upstream cause.
- Always re-watch the integrated piece from the start after isolated repairs.

## 9. Verification

- A repair is verified only by the test that revealed the symptom, repeated after the change (the same isolation test or fresh-viewer question), followed by an uninterrupted viewing of the whole integrated piece.
- Record symptom, test, repair and result in the review log (see [Review and Revisions](../OPERATIONS/Review-and-Revisions.md#5-review-annotation-format)) so recurring symptoms can be traced upstream.

## Dependencies

- Links to all craft chapters as owners of repairs.
- Companion: [Creative Coherence and Taste](../FOUNDATIONS/Creative-Coherence-and-Taste.md).
- Review process: [Review and Revisions](../OPERATIONS/Review-and-Revisions.md).

## Confidence summary

The diagnosis sequence and isolation tests are `[Practice]`-based teaching tools; their ordering is a `[Heuristic]`. The matrix summarises the craft chapters' failure/repair pairs; each entry's confidence follows its owner chapter. Examples are `[Illustrative]`.
