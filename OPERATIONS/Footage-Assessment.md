# Footage Assessment and Select Strategy

**Purpose:** Teach the first expert inspection of raw material, a selection system that preserves context, triage for damaged or missing material, and the acceptance gates that must pass before a rough cut begins.

**Applies to:** Any project after acquisition — shot footage, interviews, archive, third-party clips, screen recordings and generated material.

**Prerequisites:** [Creative Brief](../FOUNDATIONS/Creative-Brief.md), [Ingest and Preparation](Ingest-and-Preparation.md) (media must be safely ingested before it is assessed).

**Ownership boundaries:** Ingest, backup, proxies, sync technique and the frame-rate/timecode convention are owned by [Ingest and Preparation](Ingest-and-Preparation.md). Rights status is recorded here but governed by [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md). Detailed sound restoration is in [Recording and Cleanup](../AUDIO/Recording-and-Cleanup.md).

---

## 1. The first inspection

The first pass through new material is not editing. It is **reconnaissance**: discovering what the footage can and cannot do for the brief, before preferences form. An editor who starts assembling during the first viewing tends to fall in love with early material and miss later, better takes.

### What to inspect, and what each tells you

| Dimension | Observe | Why it matters |
|---|---|---|
| Story coverage | Which beats in the plan have material; which have none; what unplanned material exists | Determines whether the planned structure is possible |
| Performance | Truthfulness, energy, listening, reactions, consistency across takes | The edit's emotional ceiling |
| Technical quality | Focus, exposure, noise, compression, stability, flicker | Determines repair cost and usability |
| Useful beginnings and endings | Where a shot settles, where action starts, handles before/after | Cut options, transitions, J/L edits |
| Movement | Camera and subject motion; whether moves complete; speed | Cutting points, retiming feasibility |
| Continuity | Props, positions, eyelines, light changes, wardrobe | Which takes can be intercut |
| Sound | Intelligibility, noise, clipping, perspective, room tone availability | Dialogue usability; repair cost |
| Metadata | Timecode, frame rate, resolution, color profile, camera/reel IDs, file integrity | Technical pipeline decisions |
| Release status | Who appears; whether consent exists; location and third-party content visible | Whether material can be used at all |

### A practical inspection sequence `[Practice]`

1. **Technical sweep first** (fast): open every clip, note anything that will not play, has missing audio, wrong frame rate or obvious corruption. This catches problems while reshoots or re-transfers are still possible.
2. **Watch at full speed, sound on,** for performance and story. Take notes with timecode. Do not scrub through performance; scrubbing hides timing and truthfulness.
3. **Second pass with specific questions**: continuity, focus, sound defects, best handles.
4. **Rights pass**: identifiable people, logos, artworks, screens, documents, music audible in the background.

## 2. Truth versus technical cleanliness

The technically cleanest take is not automatically the best. Experts routinely choose a take with a minor technical flaw because the performance is more truthful, the listening is more alive, or a spontaneous moment occurred.

| Situation | Usually prefer | Reason |
|---|---|---|
| Take 3 is sharp; take 5 has a soft-focus moment but the subject's emotion is real | Take 5, if the softness is brief and does not obscure the eyes at the critical moment | Viewers forgive minor softness; they detect false emotion |
| Take 2 has perfect sound; take 4 has a car passing during a pause, but a more natural delivery | Take 4, if the car can be reduced or the pause trimmed without harming the delivery | Sound can often be repaired in pauses; performance cannot be repaired |
| A clip is technically flawless but the subject is clearly performing for the camera | Neither, if possible; look for unguarded moments | The audience will feel the performance |

### When a defect makes a take unusable

A defect becomes disqualifying when it:

- **Obscures the information the moment exists to deliver** — the product label is out of focus in the only close-up of it; a key word in testimony is clipped beyond intelligibility.
- **Cannot be repaired without fabrication** — restoring a missing word with synthetic voice in documentary testimony would create speech the person did not produce at that moment.
- **Breaks the viewer contract** — a visible crew member in an observational scene that claims no intervention.
- **Violates consent or privacy** — an identifiable patient in the background without consent, where masking would be impractical or distracting.
- **Is a safety or compliance failure** — e.g., heavy fluorescent flicker that produces a strobing effect that might fail a flash-risk check (see [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md)).

## 3. A selection system

A selects system turns hours of material into a searchable, annotated library. Its fields should serve later decisions, not bureaucracy.

| Field | Content | Used later by |
|---|---|---|
| Clip ID / scene / take | Unique identifier matching the camera file and slate | Everyone |
| Source TC in/out | Timecode of the usable section | Editor, conform |
| Story purpose | Which beat it can serve | Editor |
| Emotional beat | What it can make the viewer feel | Editor, composer |
| Transcript reference | Line or summary of what is said | Editor, captions |
| Picture defects | Focus, exposure, flicker, shake | Colorist, VFX |
| Sound defects | Noise, clipping, overlaps, off-mic | Dialogue editor |
| Continuity concerns | Prop, position, eyeline issues | Editor |
| Permissions | Who is visible; consent status; third-party content | Producer |
| Alternatives | Other takes or angles that could replace it | Editor |
| Repair feasibility | Easy / specialist / not feasible | Producer, finishing |
| Rating | Hero / strong / usable / reject | Editor |

### Filled selects log — Project A multicamera interview (hypothetical, 25 fps)

| Clip | TC in–out (A-cam) | Story purpose | Emotional beat | Transcript | Picture | Sound | Continuity | Permissions | Alternatives | Repair | Rating |
|---|---|---|---|---|---|---|---|---|---|---|---|
| A001_C014 | 10:14:20:00–10:15:02:12 | Evidence of competence | Admiration, light humour | Torch-in-mouth story during power cut | Good; slight underexposure late as clouds pass | Fan audible; intelligible | Window light dips at 10:14:58 | Asha: signed | B-cam B014 covers the light dip | Grade to smooth light change | Hero |
| A001_C019 | 10:30:50:00–10:31:20:00 | Reversal | Realisation | "I stopped noticing I was tired" with 4-s pause and self-correction | Good | Generator hum starts mid-answer | — | Signed | B-cam angle on same answer | Hum reduction; keep pause | Hero — protect pause |
| A001_C022 | 10:42:10:00–10:42:40:00 | Relationship | Warmth | Mentions Sunita covering a shift | Good | Interviewer "mm-hmm" overlaps at 10:42:21 | — | Sunita named — check her consent | Re-asked at 10:44:05 without overlap | Use second version or B-cam cut | Strong |
| A001_C031 | 10:55:38:00–10:56:30:00 | Hook | Tenderness | Daughter asks why she sleeps in the day | Slight focus breathing as she leans in | Clean | Subject leans forward — framing tighter | Child mentioned, not shown; confirm Asha's comfort | None — unique moment | Accept softness; it reads as intimacy | Hero |
| B001_C009 | (B-cam phone) | Coverage | — | Same as A001_C019 | Phone camera, different color; variable frame rate flagged at ingest | Not used (A-cam/lav audio is master) | 3/4 angle | — | — | Conform to constant frame rate; match grade | Usable |

### Ranking hero moments without discarding context

Mark hero moments, but keep the surrounding material linked in the log:

- **Context before:** the question asked, what was said just before. A hero line that answers a different question than it appears to is dangerous.
- **Context after:** qualifications, corrections, a laugh that changes the tone.
- **Linked alternatives:** where the same idea is expressed in another take.

A selects reel containing only hero moments is efficient for building and dangerous for truth. Keep the full-answer bins next to the selects bins, and check context before lock (see [Interview Craft](../STORY/Interview-Craft.md#16-verification-before-picture-lock)). The selects log is also the input to the paper edit, where the chosen lines are ordered into a story before timeline assembly (see [Paper Edit and Assembly](Paper-Edit-and-Assembly.md)).

## 4. Logging versus creative selection

On large projects, logging (describing what exists) and selection (judging what to use) should be separated, either in time or between people.

| | Logging | Creative selection |
|---|---|---|
| Purpose | Make material findable | Choose the material that serves the story |
| Done by | Assistant, logger, or automated tools reviewed by a person | Editor, director |
| Output | Descriptions, keywords, transcripts, technical notes | Selects, ratings, story notes |
| Risk if merged | Editor spends weeks describing rather than shaping | Logger's taste filters out material before the editor sees it |

### Transcript and metadata search — and their limits

Transcripts make speech searchable; metadata (location, camera, scene, people) makes picture searchable. Both are powerful and both mislead in characteristic ways:

- **A transcript is not the performance.** It does not record a 4-second pause, a wry tone, a contradicting facial expression, or a sob. Search finds words; only watching finds meaning.
- **Automatic transcripts mishear names, technical terms and negation.** "I didn't want to leave" transcribed as "I did want to leave" inverts meaning. Names of people and places are frequently wrong. For any line that will carry story weight or appear in captions, verify the transcript against the audio.
- **Code-switching and accents** reduce automatic transcription accuracy; Asha's Hindi with English medical terms is a likely failure case.
- **Metadata is only as good as its entry.** A shot logged "corridor" may also contain an identifiable patient; the log does not replace a rights pass.

See [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md) for the approval process when automated logging and transcription are used.

## 5. Archival and third-party material

Archive, user-generated content, stock footage and third-party clips are a separate source class with their own risks.

| Issue | What to check | Consequence if ignored |
|---|---|---|
| Provenance | Who created it, when, where; chain of custody | Misattributed or fake material in a factual piece |
| Resolution and frame rate | Native size and rate; whether it was already converted | Upscaling artefacts; judder from rate conversion; mismatch with the timeline |
| Original audio | Present, absent, replaced, or unusable | May need sound design or silence; adding sound to archive can mislead |
| Re-use restrictions | Licence scope: territory, term, platforms, paid use, duration of use | Takedowns, legal exposure |
| Display versus alteration | A licence to show a clip may not permit cropping, colourising, speed changes, reframing for vertical, or AI enhancement | Licence breach; misrepresentation |
| Captions and burned-in text | Existing logos, captions, watermarks | Clutter; licence obligations |

**Resolve archival choices before the edit depends on them.** A late substitution — because a licence fell through — can change duration, aspect ratio, clearance, the graphic treatment built around the clip, and the music edit. Mark unconfirmed archive clearly in the timeline (for example, a coloured clip label and a "PENDING CLEARANCE" marker), and keep an alternative in the log.

## 6. Triage for damaged, missing or weak material

### The triage options

| Option | What it means | Good when | Costs |
|---|---|---|---|
| Repair | Technical fix (grade, denoise, stabilise, restore) | Defect is moderate and the information exists in the signal | Time; artefacts if pushed too far |
| Substitute | Use another take, angle or similar shot | Coverage exists | Continuity; possibly weaker performance |
| Reframe | Crop or reposition to hide a defect | Resolution headroom exists; the defect is at the edge | Quality loss; changes composition and body language |
| Shorten | Use less of the shot | The defect is localised in time | May lose timing or context |
| Explain through graphics | Replace or support missing visuals with design | Abstract information; missing visual evidence of a process | Credibility; time; design cost |
| Reshoot / re-record | Capture again | Access exists; the defect is fatal | Cost; continuity; subject's fatigue; truth in documentary (a re-enactment must be disclosed) |
| Revise story | Change structure to avoid needing the missing piece | No repair is honest or feasible | May weaken the planned arc |

### Defect-specific guidance

| Defect | What is recoverable | What is not | First move |
|---|---|---|---|
| Sparse coverage | Structure can be adapted; jump cuts can be honest; cutaways can help | Angles that were never shot | Revise structure; see [Continuity and Attention](../EDITING/Continuity-and-Attention.md) |
| Corrupted clips | Sometimes partial recovery from card or file repair tools; re-copy from the card if it has not been formatted | Data that was never written | Check backups and source cards before anything else |
| Missing room tone | Tone can sometimes be extracted from pauses in the take; similar tone can be constructed | An exact match to every moment | Gather clean pauses; see [Recording and Cleanup](../AUDIO/Recording-and-Cleanup.md) |
| Noisy dialogue | Steady noise (hum, fan) can often be reduced considerably | Speech masked by loud broadband noise at the same moment; words buried under other speech | Assess intelligibility on headphones; test restoration on a short section |
| Clipped highlights | Partial recovery if only one channel clipped, or if the camera's log/raw retained more than the monitor showed | Detail in fully clipped regions; recovery cannot invent texture | Inspect in the log/raw source, not the display LUT |
| Focus misses | Slight softness can be masked by sharpening, grain, smaller viewing size, or a shorter shot | Detail that was never resolved; sharpening creates halos, not information | Shorten, substitute, or accept if the moment is truthful |
| Compression damage (macro-blocking, banding) | Grain and debanding can hide some damage | Lost texture and gradation | Avoid pushing the grade; add grain carefully |
| Camera mismatch | Grading can bring cameras close; texture can be matched partly | Different dynamic range and sensor behaviour cannot be fully equalised | Match through [Correction and Shot Matching](../COLOR/Correction-and-Shot-Matching.md); use the mismatch structurally if needed |

### What enhancement and AI cannot honestly do

Enhancement tools — including AI upscalers, deblur, face restoration and voice reconstruction — can produce convincing *plausible* detail. Plausible is not the same as recorded. In factual work, generated detail in a face, a document, a licence plate or a voice is invented evidence. Use such tools only where invented detail would not mislead (a background texture in a brand film), document their use, and disclose where the viewer contract requires (see [Generated Media QC](../AI-WORKFLOWS/Generated-Media-QC.md) and [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md)).

## 7. Worked example 1 — Multicamera interview (hypothetical, Project A)

**Material:** A-cam (mirrorless, 25 fps, log profile, timecode set to time of day), B-cam (phone, nominally 25 fps but variable-frame-rate capture), external recorder with lav and boom (timecode jam-synced to the A-cam at the start of the day), about 70 minutes.

**Sync confidence:**

| Source pair | Method | Confidence | Check |
|---|---|---|---|
| A-cam ↔ recorder | Timecode (jammed at 08:30; re-checked at lunch) | High, if drift is checked | Slate clap at the start and end of each roll; compare at end |
| B-cam ↔ A-cam | Audio waveform sync (phone's scratch audio) | Medium; variable frame rate can drift | Check lip sync at the beginning, middle and end of each B-cam clip after conforming to constant frame rate |

*Hypothetical finding:* the B-cam's 18-minute clip is in sync at the start and about 3 frames late by the end after an unconformed import. After conforming to constant 25 fps (see [Ingest and Preparation](Ingest-and-Preparation.md#variable-frame-rate-sources)), drift is within one frame across the clip.

**Select criteria applied:**
- Truthfulness over fluency (the self-correction in A001_C019 is kept).
- Intelligibility after realistic repair, not ideal repair.
- Continuity of window light between intercut answers.
- Consent for any named third party (Sunita).

**Missing coverage decision:** The light dip at 10:14:58 coincides with the torch story's punchline. Options: grade the dip (repair), cut to the B-cam during the dip (substitute), or accept it. Choice: cut to the B-cam for the dip — it is the cheapest honest fix and also gives the edit a natural angle change on the laugh.

**Source preservation:** Original camera files, recorder files and the phone files are kept unmodified on two verified copies; the conformed phone files are new derived media, labelled as such.

## 8. Worked example 2 — Imperfect handheld event (hypothetical)

**Material:** A single-operator handheld recording of a 90-minute community health camp in a school courtyard, for a 3-minute report. One camera with on-camera microphone plus a wireless lav on the camp organiser. Midday sun; harsh contrast; crowd noise; a generator.

**First inspection findings (hypothetical):**
- About 40% of the material is unusable for picture reasons: operator searching for the subject, whip pans, highlight clipping on white walls.
- The most important moment — an elderly man's blood-pressure reading being explained to him — is covered in one 50-second take with the reading shown on the device for about 2 seconds in focus.
- Crowd noise masks the doctor's explanation; the lav was on the organiser, not the doctor.
- Several children are identifiable in the background; consent from guardians is uncertain.

**Triage decisions:**

| Issue | Choice | Rationale |
|---|---|---|
| Key moment with poor dialogue | Keep picture; use subtitled lines only where the doctor's speech is genuinely intelligible on careful listening; mark unclear words as unclear rather than guessing | Captions must not fabricate inaudible words; see [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |
| Device reading in focus for 2 s | Hold the 2 seconds; do not freeze-frame to extend it if that would imply a different moment; a short text label can repeat the reading if the organiser confirms it | Honest emphasis |
| Identifiable children without consent | Crop, choose other shots, or blur; prefer choosing other shots because blurring many faces becomes distracting | Privacy; see [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md) |
| Harsh highlights | Grade highlights down with a soft roll-off; accept some clipped walls | Recovery beyond the recorded signal is not possible |
| Missing coverage of the queue | Revise story: the organiser's lav provides a clean description of the queue; use her line over a short wide shot | Revised structure rather than invented visuals |

**Acceptance gates:** see Section 10.

## 9. Counterexample and repair — promising what restoration cannot deliver

**Hypothetical counterexample.** In a product shoot for a different client, the only close-up of a watch's engraved serial number is slightly out of focus. The producer tells the client, "We'll fix the focus with AI in post." The AI tool produces a sharp image in which the engraved characters are plausible but *different* from the real serial number. The client's legal team catches it during review; the deadline is missed.

**Diagnosis.** Focus that was never captured cannot be recovered; generative sharpening invents detail. The promise was made before the defect was assessed.

**Repair.**
1. Assess the shot honestly: the engraving is not legible.
2. Options: a pickup shot of the watch (cheap — the product is available), a graphic overlay of the serial format, or removal of the engraving beat.
3. Choice: pickup shot on a small tabletop setup matching the lighting reference, completed in half a day.
4. Process change: no promise about repair is made to a client before a technical assessment; AI enhancement is never used to generate legible text, numbers, faces or evidence in factual or claims-bearing contexts.

**Verification.** Legal confirms the pickup shows the correct engraving; the colorist matches the pickup to the surrounding shots.

## 10. Acceptance gates before rough cut

Rough cutting should not begin until these gates pass. Each gate has an observable pass criterion and a failure action.

| Gate | Pass criterion | Failure action |
|---|---|---|
| Material opens | Every clip plays in the edit system; duration matches the source | Re-copy from verified backup or source card; log unrecoverable clips |
| Masters are safe | At least two independent verified copies of original media exist, one off-site or on a separate device | Stop; complete backup before further work |
| Sync is checked | Every multi-source clip is checked at start, middle and end | Re-sync; conform variable-frame-rate sources |
| Frame rate and timecode documented | Project rate, timecode convention (DF/NDF) and treatment of off-rate sources written in the project notes | Decide and document before editing; see [Ingest and Preparation](Ingest-and-Preparation.md) |
| Color assumptions documented | Camera profiles, intended input transforms and monitoring LUT noted | Document; see [Color Management](../COLOR/Color-Management.md) |
| Critical rights known | Consent status of featured people; archive/third-party licence status; music status | Mark pending items in the timeline; plan alternatives |
| Selects log exists | Hero moments marked with context links | Complete before structuring |

## 11. Micro-decisions

- Watch the last few seconds of every interview clip — subjects often say something important as the camera is about to stop.
- Note the *best handle* (a clean breath, a settled frame) for each select; it saves time at the cutting stage.
- Rate performance and technical quality separately; a single combined rating hides trade-offs.
- Use colour labels consistently: for example, red for rights pending, yellow for technical repair needed. Document the scheme.
- When a transcript line will carry story weight, listen to it at least twice before relying on it.

## 12. Failure signatures and corrections

| Symptom later in the edit | Assessment failure | Correction |
|---|---|---|
| A crucial clip turns out to be corrupted at online | Technical sweep skipped | Restore from backup; if none, re-plan the beat |
| Sync drifts in long phone clips | Variable frame rate not detected | Conform and re-sync |
| A hero line is challenged as out of context | Context not linked in selects | Re-check full answer; repair the edit |
| Late licence failure on archive | Archive status not tracked | Swap to logged alternative; re-time graphics and music |
| Client expects impossible repair | Promise made before assessment | Assess first; offer honest options |

## Dependencies

- Depends on: [Ingest and Preparation](Ingest-and-Preparation.md), [Creative Brief](../FOUNDATIONS/Creative-Brief.md), [Interview Craft](../STORY/Interview-Craft.md).
- Feeds: [Paper Edit and Assembly](Paper-Edit-and-Assembly.md), [Story Architecture](../STORY/Story-Architecture.md), [Performance Editing](../EDITING/Performance-Editing.md), [Recording and Cleanup](../AUDIO/Recording-and-Cleanup.md), [Correction and Shot Matching](../COLOR/Correction-and-Shot-Matching.md), [Repair and Finishing](../VFX/Repair-and-Finishing.md).
- Rights: [Rights, Consent and Disclosure](Rights-Consent-and-Disclosure.md).

## Confidence summary

The inspection sequence, separate logging and selection, verified backups and the acceptance gates are `[Practice]`. The claims about what cannot be recovered (clipped detail, unrecorded focus, masked speech) are technical facts about information loss `[Practice]`; the degree of partial recovery depends on tools and material. The preference for truthful performance over technical cleanliness is a `[Heuristic]` bounded by the disqualifying conditions in Section 2.
