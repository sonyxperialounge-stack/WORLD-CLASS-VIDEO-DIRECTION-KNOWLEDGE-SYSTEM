# Dialogue Editing, Voice-Over and ADR

**Purpose:** Teach the first listen to dialogue, the editorial craft of assembling clean, continuous, truthful speech (take selection, breaths, pauses, overlaps, joins, room tone, fill), and the direction of voice-over and ADR for intent, emphasis, pace and relationship to picture.

**Applies to:** Interviews, scenes, presenters, narration, ADR and remote recordings.

**Prerequisites:** [Recording and Cleanup](Recording-and-Cleanup.md) (capture and processing), [Performance Editing](../EDITING/Performance-Editing.md) (what may be compressed).

**Ownership boundaries:** Processing tools and capture are in [Recording and Cleanup](Recording-and-Cleanup.md). Balance against music and effects is owned by [Mix Strategy](Mix-Strategy.md). Synthetic voice is in [Voice and Music QC](../AI-AUDIO/Voice-and-Music-QC.md).

---

## 1. The first listen

Before editing dialogue, listen through every relevant take on headphones and on speakers, noting:

| Listen for | Why |
|---|---|
| Intelligibility | Can every important word be understood at a normal listening level? |
| Performance | Is the delivery truthful, with intention and listening? (see [Performance Editing](../EDITING/Performance-Editing.md)) |
| Distance and perspective | Does the voice sound near or far, and does it match the shot? |
| Room noise and changes | Steady noises; noises that start and stop between takes |
| Clipping and distortion | Usually unrepairable in full |
| Plosives and sibilance | Repairable in moderation |
| Mouth noises | Clicks, lip smacks — repairable, but some are part of the person |
| Phase between mics | Lav and boom combined may sound hollow |
| Sync | Lip sync, especially after frame-rate conversions |
| Emotional continuity | Does the voice's emotional state connect across edits? |

The first listen produces a **dialogue notes list** with timecodes, so that problems are tackled deliberately rather than discovered during the mix.

## 2. Dialogue assembly

### 2.1 Take and word selection

The picture editor chooses performance; the dialogue editor then may substitute *sound* from other takes where picture allows (off-screen lines, lines on the back of a head, wide shots where lip sync is not critical). This is common in fiction and must follow the factual limits of documentary: in testimony, substituting a word from another moment can change meaning or create a statement — only acceptable when meaning is unchanged and the sound is the same utterance in a cleaner recording (e.g., the boom instead of the lav of the same take).

### 2.2 Breaths

| Keep | Remove or reduce |
|---|---|
| Breaths that carry emotion (a sharp intake before a confession) | Loud breaths that are distracting and carry no meaning |
| Breaths at natural phrase boundaries | Breaths left at edit points that create double breaths |
| Breaths that make speech sound human | Breaths that sit unnaturally close to the next word after an edit |

Removing all breaths makes speech feel machine-like and breathless; listeners use breaths as phrase markers `[Heuristic]`.

### 2.3 Pauses

Pauses are content. In Project A, the 4-second pause before "I stopped noticing I was tired" is protected. In a presenter piece, long hesitations can be trimmed. The dialogue editor's job is to make retained pauses sound continuous (room tone present, no gaps), not to decide editorial length alone.

### 2.4 Overlaps

Real conversation overlaps. Choices:

- **Keep natural overlaps** when the two voices are on separate tracks (lav per person) and both are intelligible.
- **Create overlaps** in fiction to restore liveliness after picture editing has removed them — using separate takes for each voice.
- **Never create overlaps in documentary** that change who interrupted whom or imply a reaction that did not occur.

### 2.5 Edit joins

A join between two pieces of speech must be inaudible unless intended. Techniques:

- Cut at the start of a consonant (especially plosives and fricatives: "p", "t", "k", "s", "f"), where the waveform changes sharply and the ear accepts a change.
- Avoid cutting in the middle of vowels, where pitch and tone are continuous and a join is audible.
- Match the room tone on either side of the join.
- Use short crossfades to avoid clicks; longer crossfades for room-tone transitions.
- Check pitch and intonation: a phrase that ends with a rising (questioning) intonation joined to a falling one sounds unnatural.

### 2.6 Room tone and fill

Every edit in dialogue can change the background: two takes recorded minutes apart have different traffic, different fan speed, a fridge cycle. **Fill** is room tone laid under and between dialogue to create a continuous background:

- Lay room tone in gaps (between lines, where words were removed).
- Overlap room tone slightly into the dialogue on either side with crossfades, so the background does not "switch".
- Where room tone was not recorded, build it from pauses in the takes (see [Footage Assessment](../OPERATIONS/Footage-Assessment.md#6-triage-for-damaged-missing-or-weak-material)).
- Keep a continuous bed across a scene when backgrounds differ between takes; Project D's refrigerator hum (present in some takes, absent in others) requires a decision: a continuous low hum laid under the whole scene, or the hum removed from all takes. The continuous hum supports the scene's domestic realism and is chosen; the takes without hum get the bed.

### 2.7 Track organisation

Split dialogue across tracks by character or microphone and by perspective (e.g., interior vs exterior), so the mixer can treat them separately. Keep production effects (a cup put down, a door closed during dialogue) on their own tracks where possible — in international versions where dialogue is replaced, these effects must survive (see [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md)).

## 3. Sync after conversions, resampling and ADR

| Cause | Symptom | Correction |
|---|---|---|
| Variable-frame-rate source | Gradual drift | Conform to constant frame rate; re-sync (see [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#variable-frame-rate-sources)) |
| Speed change (e.g., 25 fps footage interpreted at 23.976) | Audio slower; pitch lower; drift if audio not conformed | Conform audio speed (with pitch correction) to match picture, or avoid the interpretation |
| Sample-rate mismatch (48 kHz vs 44.1 kHz) | Drift or pitch change if misinterpreted | Correct sample-rate conversion |
| ADR | New lines must fit the original mouth movements | Edit ADR syllable by syllable; time-stretch tools sparingly |

Lip-sync tolerance depends on shot size and viewer; on close-ups, errors of a frame or two can be noticeable `[Heuristic]`.

## 4. Room perspective changes between takes

When takes recorded at different distances or in different rooms are intercut, the voice's perspective jumps: closer, drier, brighter in one; farther, roomier in another. Options: choose consistent takes; match with EQ and subtle reverb; use the lav from one take and the boom from another only if they match; or let the perspective change where the picture also changes perspective (a wide and a close-up). Perspective in sound design is developed in [Perspective and Silence](Perspective-and-Silence.md).

## 5. Voice-over and ADR direction

### 5.1 Direction through intent, not adjectives

"Say it warmer" and "more energy" are weak directions. Strong direction gives the narrator a reason to speak:

| Weak | Stronger |
|---|---|
| "Warmer, please." | "You're telling a neighbour who's worried about her family's water. You know the answer and you want to reassure her." |
| "More energy." | "This is the part where you discovered the mistake — you're surprised it's so simple." |
| "Slower." | "Give her time to look at the filter after each step. Imagine she's following along with her hands." |
| "Emphasise 'weekly'." | "The whole point of this line is that people do it once a year. 'Weekly' is the surprise." |

### 5.2 Emphasis, pace and phrasing

- **Emphasis** changes meaning: "Clean it *weekly*" (frequency) vs "*Clean* it weekly" (action).
- **Pace** must leave room for picture: viewers watching a demonstration need time to look, not just listen.
- **Phrasing** should follow sense groups; breath points should fall at phrase boundaries.
- **Relationship to picture:** narration that describes what is plainly visible wastes attention ("Here you can see a filter"); narration should add what the picture cannot say ("This is where the dirt gets trapped").

### 5.3 Warm voice versus credible content

A pleasant, authoritative voice increases perceived credibility. That is a responsibility. A voice must not be used to lend authority to claims the content does not support — a reassuring voice reading an unsubstantiated health claim is still an unsubstantiated claim. In factual work, credibility should come from evidence; the voice should be clear and respectful, not falsely confident about uncertain things.

### 5.4 Editing copy for speakability

Copy written for reading often fails when spoken: long noun phrases, parentheses, abbreviations, numbers and lists are hard to say and to hear.

| Written | Speakable |
|---|---|
| "The ceramic candle (approx. 20 cm) should be cleaned w/ a soft brush weekly." | "Once a week, take out the candle and clean it with a soft brush." |
| "Results: unfiltered 1,200 CFU/100 mL; uncleaned 400; cleaned 15." | "Unfiltered water had the most bacteria. A filter that wasn't cleaned still let a lot through. A clean filter let very few through." (Numbers on screen, words in the voice.) |

Read the script aloud with picture before recording. Mark breath points and emphasis. Time it.

### 5.5 ADR

ADR (re-recording dialogue in post for fiction) is used for noise, performance or line changes. Direct for the same intent as the on-set performance; match the actor's physical state (out of breath after running, lying down); record with mic distance appropriate to the shot's perspective; play the original as a guide. In documentary, re-recording a subject's words is not ADR in the fiction sense — it is a new statement and must be handled transparently (see [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md)).

## 6. Worked example 1 — Dialogue edit decision log (hypothetical, Project A, 25 fps)

| # | Timeline TC | Source | Problem | Decision | Reason | Check |
|---|---|---|---|---|---|---|
| 1 | 01:00:12:10 | A001_C031 lav | Interviewer's "hmm" at the end of Asha's line | Remove with spectral repair; fill with room tone | Interviewer is not part of the film's sound | Listen on headphones; no hole |
| 2 | 01:04:05:00–01:04:45:00 | A001_C019 lav+boom | Generator starts mid-answer | De-hum automated from generator start; room-tone bed adjusted to include hum after its start | Natural continuity; the generator's presence is real | Audio-only pass; hum arrival not abrupt |
| 3 | 01:04:15:00 | A001_C019 | 4-s pause | Keep in full; room tone continuous | Pause is content | Silent pass of picture + audio-only pass |
| 4 | 01:04:20:12 | A001_C019 | Self-correction "I mean — not stopped, I just —" | Keep | Changes meaning (see [Performance Editing](../EDITING/Performance-Editing.md)) | Compare with full answer |
| 5 | 01:02:10:05 | Observational, on-camera mic | Asha and Sunita overlapping at tea | Keep overlap; light de-noise; no lav available | Natural; both intelligible enough with subtitles | Bilingual listener confirms both lines are audible |
| 6 | 01:03:40:00 | Observational | Patient's voice audible, identifiable by name | Remove name (dip the word, replace with room tone) per consent agreement; caption "[patient speaking]" | Privacy | Producer confirms consent compliance |

## 7. Worked example 2 — A clean but lifeless explainer VO (hypothetical, Project C)

**Problem:** the first English narration is technically clean — well recorded, no noise — but reviewers say it "sounds like a phone menu". Viewers in a test remember fewer steps than expected.

**Diagnosis (hypothetical listening notes):**
- Every sentence has the same falling intonation and the same pace.
- No emphasis on the key surprise ("no soap") — it is read like any other phrase.
- No pauses after steps; the narrator reads continuously.
- The narrator never refers to the viewer ("you"), because the script didn't.

**Repair:**
1. **Rewrite for speech:** second person ("you"), shorter sentences, the surprise placed at the end of the sentence where natural emphasis falls ("Most people use soap. Don't.").
2. **Direct by intent:** "You're showing a friend at her kitchen counter."
3. **Pace with picture:** record to picture playback so the narrator feels the pauses after each step.
4. **Emphasis marking:** script marks one stressed word per sentence at most.
5. **Keep the clean recording chain;** the problem was performance and writing, not sound quality.

**Verification:** compare old and new narration with picture on a phone speaker; repeat the recall test.

## 8. Counterexample and repair — the "authoritative" voice that overclaimed

**Hypothetical counterexample.** A supplement company's video uses a deep, calm, doctor-like narrator who says, "Clinically proven to boost immunity." There is no clinical evidence; the voice was cast "to sound like a doctor". Viewer comments ask whether the narrator is a physician.

**Diagnosis:** casting and delivery used to create false authority; an unsubstantiated claim delivered as fact.

**Repair (as a practitioner on the job):** name the conflict to the producer: the line cannot be delivered as written without substantiation; the voice casting implies medical authority. Offer alternatives: remove the claim; state only what is supported; cast a voice that does not imply a medical role; add a clear statement that the narrator is not a medical professional if the style remains. Escalate to the responsible decision owner (client legal) rather than silently complying (see [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md)).

**Verification:** legal approval of the final wording; a fresh-viewer question "who is speaking?" does not elicit "a doctor".

## 9. Micro-decisions

- Cut dialogue a few frames before the first syllable where a breath precedes it, so the breath belongs to the line.
- Use crossfades of a few milliseconds at hard dialogue cuts to avoid clicks; longer for room-tone transitions.
- Keep a copy of every line removed for privacy or editorial reasons in a separate, labelled track (muted), so the decision is traceable.
- When ADR or pickup lines are intercut with production sound, match the room with tone and subtle reverb before matching EQ.
- Write narration to *add* to picture, not describe it.

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Background "switches" at edits | No fill; takes with different tone | Room-tone fill; continuous bed |
| Audible clicks at cuts | No crossfades; cuts mid-waveform | Crossfades; cut at zero-crossings or consonant onsets |
| Machine-gun speech | Breaths and pauses removed | Restore phrase-boundary breaths |
| Unnatural joins | Cuts mid-vowel; mismatched intonation | Re-cut at consonants; choose matching intonation |
| Narration feels detached | Clean but performance-less; describes the obvious | Re-write for speech; direct by intent; record to picture |
| Lip sync drift | VFR, speed or sample-rate issues | Conform and re-sync |

## 11. Verification

- Headphones for joins and artefacts; ordinary speakers for balance; phone speakers at low volume for intelligibility.
- Full-scene audio-only pass for continuity of backgrounds.
- Source-context checks for every documentary dialogue edit.
- Sync checks on close-ups after any conversion.
- State when a defect requires specialist intervention or re-recording.

## Dependencies

- Depends on: [Recording and Cleanup](Recording-and-Cleanup.md), [Performance Editing](../EDITING/Performance-Editing.md), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md).
- Feeds: [Mix Strategy](Mix-Strategy.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md), [Localization](../TEXT-ACCESSIBILITY/Localization.md).
- Synthetic voice: [Voice and Music QC](../AI-AUDIO/Voice-and-Music-QC.md).

## Confidence summary

Room-tone fill, consonant-onset cutting, track splitting and the first-listen checklist are `[Practice]`. Breath and lip-sync tolerance observations are `[Heuristic]`. Direction-by-intent is a widely used `[Practice]` in voice and acting direction. Examples are `[Illustrative]`.
