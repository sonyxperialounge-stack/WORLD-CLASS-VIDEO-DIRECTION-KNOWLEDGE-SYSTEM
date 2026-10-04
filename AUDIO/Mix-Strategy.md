# Mix Strategy: Space, Hierarchy, Dynamics and Loudness

**Purpose:** Teach how to balance dialogue, music, ambience and effects as competing perceptual tasks; the vocabulary of levels and loudness and what each measure is for; how to build a mix hierarchy that follows the story; and how to translate a mix across headphones, phones, speakers and platform normalisation.

**Applies to:** Every finished piece with sound.

**Prerequisites:** [Dialogue and Voice](Dialogue-and-Voice.md), [Music Editing](Music-Editing.md), [Sound Design](Sound-Design.md), [Perspective and Silence](Perspective-and-Silence.md).

**Owns:** Mix technique. Destination loudness targets, channel layouts and stem deliverables are owned by [Audio Delivery](../DELIVERY/Audio-Delivery.md).

---

## 1. Elements compete for the same ears

Dialogue, music, ambience and effects are often taught as occupying "their own frequency bands" — dialogue in the middle, music around it, effects at the extremes. In reality their spectra overlap heavily: speech energy and intelligibility cues span a wide range; music occupies almost everything; effects can sit anywhere. Mixing is therefore not dividing a spectrum into boxes. It is deciding, moment by moment, **which sound the listener needs to attend to**, and making room for it with several complementary tools.

## 2. Tools for creating space

| Tool | How it creates space | Strength | Failure when overused |
|---|---|---|---|
| Arrangement | Choose what plays when: music enters after a line, an effect waits for a pause | The cleanest solution; no processing artefacts | Requires editorial collaboration; may conflict with picture timing |
| Level automation | Ride levels so the priority sound is clear | Precise, musical, transparent | Time-consuming; "riding" too much creates pumping |
| Timing | Move non-critical sounds off important words | Very transparent | Sync constraints for visible events |
| Spectral balance (EQ) | Reduce competing energy in a region where the priority sound needs clarity | Useful for persistent conflicts | Over-carving thins music and effects; boxy, unnatural sound |
| Dynamic control (compression, limiting) | Even out level variation; control peaks | Consistency, especially for dialogue | Pumping; loss of contrast and life |
| Spatial placement | Dialogue centred; music and ambience wider | Separation by position | Collapses on mono playback |
| Ducking (automatic level reduction triggered by another signal) | Music lowers when dialogue is present | Fast; useful for long, simple programmes | Audible pumping; ducks on breaths and noise; mechanical feel |

### Three ducking approaches compared

| Approach | How | Works well | Fails |
|---|---|---|---|
| Broadband sidechain ducking | Whole music track lowers when dialogue is detected | Podcasts, simple explainers, live streams | Audible "breathing"; music drops on every syllable; ducking triggered by noise |
| Frequency-selective (dynamic EQ) ducking | Only the region where dialogue needs clarity is reduced in the music when dialogue is present | Dense music under continuous dialogue | Can sound phasey or hollow if deep; subtle failure: music timbre changes with speech |
| Manual automation | The mixer draws level changes that anticipate lines and follow musical phrasing | Finished films, ads, any piece where music matters | Time; needs skill |

A common professional combination `[Practice]`: manual automation for musical shape and anticipation, with a gentle frequency-selective process to handle residual masking.

## 3. The vocabulary of level and loudness

These measures are different things; confusing them causes most loudness mistakes.

| Measure | What it describes | Unit | Used for |
|---|---|---|---|
| Sample peak | The highest sample value in the digital signal | dBFS | Preventing digital clipping in fixed-point files |
| True peak | Estimated peak of the reconstructed analogue waveform, including inter-sample peaks | dBTP | Preventing clipping after conversion, resampling or lossy encoding |
| RMS-style average | Average energy over a window, unweighted or simply weighted | dB | Rough indication of density; not a standard loudness measure |
| Momentary loudness | Loudness over a very short window (400 ms, as defined for BS.1770-based metering in EBU Tech 3341) | LUFS | Watching fast changes |
| Short-term loudness | Loudness over a 3-second window (EBU Tech 3341) | LUFS | Watching sections; consistency during the mix |
| Integrated (programme) loudness | Loudness over the whole programme, with gating that ignores silence and very quiet passages | LUFS (= LKFS) | Normalisation and delivery compliance |
| Loudness range (LRA) | Statistical spread of short-term loudness | LU | Describing macro-dynamics |
| Perceived loudness | What a listener experiences | — | The final arbiter, affected by playback level, content and context |

Key distinctions:

- **dBFS is not LUFS.** A mix can peak at −1 dBFS and be quiet in loudness (very dynamic), or peak at −10 dBFS and be loud (heavily compressed).
- **Sample peak is not true peak.** Inter-sample peaks can exceed the highest sample by a fraction of a dB to over a dB in dense, limited material; lossy encoding can raise them further.
- **Integrated loudness is a long-term average.** A programme can meet an integrated target while individual moments are much louder or quieter.

The measurement standard behind LUFS is ITU-R BS.1770; meters compliant with it (and, in Europe, with EBU Tech 3341) give comparable readings `[Requirement]` where a destination specifies them.

### Gain staging and headroom

**Gain staging** is keeping levels sensible through the signal chain — not too low (noise, wasted resolution in fixed-point processing) and not too high (clipping in plug-ins or buses). **Headroom** is the margin between typical levels and the maximum. Leave headroom through the mix; final peak control belongs at the end.

### Compression, limiting and normalisation

| Process | Purpose | Artefacts when overdone |
|---|---|---|
| Compression | Reduce the range between loud and quiet within a signal; add density or consistency | Pumping, breathing, dullness, loss of transients |
| Limiting | Prevent peaks exceeding a ceiling | Distortion, flattened transients, fatigue, "squashed" sound |
| Normalisation (file) | Change overall gain to reach a target level | None in itself (it is a gain change); peak-normalising and loudness-normalising give different results |
| Normalisation (platform playback) | The player changes playback gain to match a reference loudness | Loud masters are turned down; quiet ones may be turned up (with or without limiting); perceived dynamics change |

**No single LUFS value is universal.** Broadcast recommendations (for example EBU R 128's −23 LUFS target in Europe and ATSC A/85's −24 LKFS in the US), streaming services' delivery specifications, cinema practice and online platform normalisation differ. Destination targets are owned by [Audio Delivery](../DELIVERY/Audio-Delivery.md); the mix should be designed for the primary destination and checked against each other destination.

## 4. A mix hierarchy that follows the story

The loudest sound is not necessarily the most important. The mix should rank sounds by **story importance at each moment**, and that ranking changes constantly.

| Moment (hypothetical) | Priority | What steps back |
|---|---|---|
| Project D: Nisha whispers "When?" | Her whisper | Hum lowered further; nothing else |
| Project D: tape gun screeches during tension | The screech (a punctuation) | Brief; dialogue absent |
| Project A: Asha's instruction during the emergency | Her voice | Footsteps, trolley, ambience |
| Project A: generator stops at dawn | The absence of the generator; birdsong arriving | Music held low |
| Arc spot: ring-light tone | The product sound | Music stems reduced to pads |
| Launch reel: crowd release | Music drop and crowd | Everything else |

A whispered line may outrank an explosion; an ambient detail (the generator stopping) may temporarily become the subject.

### Dialogue consistency without flattening

Dialogue should be **consistently intelligible**, not **constantly at the same level**. A shout should be louder than a whisper, perceptibly — but the whisper must still be understood. Practical approach:

1. Clip-gain and automate dialogue for consistent intelligibility at the intended listening level.
2. Apply gentle compression for residual consistency.
3. Preserve intended dynamics (performance volume differences) at a reduced but perceptible scale.
4. Check intelligibility at low listening levels — the condition under which most complaints arise.

## 5. Monitoring and honest comparison

| Issue | Practice |
|---|---|
| Monitoring level | Mix at a consistent, moderate listening level; a louder monitor makes everything sound better and changes perceived bass and treble balance |
| Level-matched comparisons | When comparing two versions (processed vs unprocessed, mix A vs mix B), match their loudness first; otherwise the louder one wins unfairly |
| Room and monitor limits | Untreated rooms exaggerate or hide bass; small monitors don't reproduce low frequencies; headphones reveal detail but misrepresent spatial balance |
| Reference playback | Check on several systems: studio monitors, headphones, a phone speaker, a laptop, a TV, and (for screenings) the venue or a representative system |
| Fatigue | Take breaks; ears adapt and judgement drifts after long sessions |

## 6. Mono compatibility and small speakers

- **Mono fold-down:** many phones, small speakers and some playback paths sum stereo to mono (or nearly). Content that is out of phase between left and right partially cancels: wide stereo effects, some reverbs, stereo-widened music. Check the mix in mono; important elements should survive.
- **Phase between microphones:** dialogue recorded on two mics (lav and boom) and summed without alignment can sound hollow; check in mono (see [Recording and Cleanup](Recording-and-Cleanup.md)).
- **Low-end behaviour:** small speakers reproduce little bass. Elements whose identity is only in low frequencies (sub drops, bass lines, a deep voice's body) disappear on phones. Give important low-frequency sounds some mid-range content (harmonics, transients) so they translate.
- **Headphones versus speakers:** headphones exaggerate stereo width and reveal small artefacts; speakers blend. A mix that sounds balanced on headphones can have too little dialogue on a TV, and vice versa.
- **Accessibility and intelligibility:** many viewers have some hearing loss, watch in noisy environments, or are non-native listeners. Dialogue intelligibility is an accessibility issue as well as a craft one; captions help but do not replace clear dialogue.

## 7. Platform normalisation as a creative constraint

Many streaming and online platforms adjust playback volume toward a reference loudness. Consequences:

- A mix made very loud with heavy limiting is **turned down** to the reference — it gains no loudness advantage and has lost its dynamics.
- A quiet, dynamic mix may be **turned up** (some platforms do, some do not, and some limit when they do), changing its peak behaviour.
- Perceived dynamics change even though the delivered file did not.

**Practice** `[Practice]`: decide the dynamic intent for the primary destination (for example, an intimate documentary with wide dynamics versus a punchy ad), mix for that intent, and check the result as it will be heard *after* normalisation — not by raising level for its own sake. Platform reference levels are not always officially published and can change; see [Audio Delivery](../DELIVERY/Audio-Delivery.md) for verified and unverified figures.

## 8. Channel layouts and stems

Stereo, 5.1, 7.1, object-based formats and their stem deliverables are specified per destination (see [Audio Delivery](../DELIVERY/Audio-Delivery.md)). Within the mix, keep dialogue, music and effects on separate buses from the start so that stems (DME — dialogue, music, effects) can be delivered without re-mixing, and so that international versions (music-and-effects tracks without dialogue) are possible.

## 9. The final mix pass

1. **Play from beginning to end** without stopping, at the intended listening level, watching picture. Note problems; do not fix during the pass.
2. **Inspect edits and tails:** clicks, cut reverb tails, abrupt ambience changes, music edits.
3. **Verify dialogue understandability** at low volume and on a small speaker.
4. **Measure** required parameters with a compliant meter: integrated loudness, true peak, and any destination-specific measures (e.g., dialogue-gated loudness where required).
5. **Check sync** on close-ups and key effects.
6. **Check mono** fold-down.
7. **Review the encoded output:** the platform's encoder (or the deliverable codec) can change peaks and tone; listen to and measure the encoded file.

Remember: a peak-safe signal may still be difficult to hear; a loud signal may have lost its musical and emotional contrast. Numbers verify compliance; listening verifies the mix.

## 10. Worked example 1 — A dialogue-heavy explainer (hypothetical, Project C "Clear Water")

**Elements:** narrator VO (dominant), demonstration production sound (water, brushing), light music bed, a few UI sounds for the app segment.

**Listening conditions:** low-cost phone speakers, often in noisy homes.

| Decision | Choice | Rationale |
|---|---|---|
| Hierarchy | Narration always first; demonstration sounds second (they are evidence); music last | Comprehension is the objective |
| Music | Sparse, mostly absent under narration; enters in section transitions | Arrangement before ducking |
| Ducking | Manual automation where music must play under narration; no automatic ducking | Avoid pumping with frequent pauses |
| Narration processing | Consistent level; gentle compression; clarity checked on a phone speaker | Intelligibility in noisy settings |
| Demonstration sounds | Kept realistic and audible in narration pauses (brushing, water) | Sound as evidence of the action |
| Low end | Minimal; voice body kept natural | Phones don't reproduce it |
| Dynamic intent | Moderate range; no sudden loud events | Viewers in homes, often at low volume |

**Verification:** low-volume listening on a phone in a moderately noisy room; a listener repeats each step from audio alone. Measure integrated loudness and true peak for the destination (see [Audio Delivery](../DELIVERY/Audio-Delivery.md)).

## 11. Worked example 2 — An action montage (hypothetical, festival app launch reel)

**Elements:** dense music, crowd recordings, designed impacts, UI sounds, one spoken line ("Your friend is at Stage 2").

| Decision | Choice | Rationale |
|---|---|---|
| Hierarchy | Music leads; impacts accent; the spoken line wins in its moment | The line carries the feature |
| Space for the line | Arrangement: the music drops out (breakdown) for the line | Cleaner than ducking dense music |
| Impacts | Mid-range transient layer plus sub layer | Translation to phones |
| Dynamics | Punchy but not over-limited; preserve the silence-then-drop contrast | Contrast is the design |
| Peaks | True-peak limited at the end of the chain to the destination ceiling | Compliance |

**Verification:** compare the drop's impact on studio monitors and on a phone; confirm the spoken line is understood on first listen at low volume.

## 12. Diagnosis — the muddy mix that is not clipping (hypothetical)

**Symptom:** a brand film's mix measures within loudness and peak limits, but reviewers say it sounds "muddy" and "tiring"; dialogue is understood only with effort.

**Investigation (hypothetical findings):**

| Check | Finding |
|---|---|
| Solo each bus | Music has strong low-mid energy; ambience bed also heavy in low-mids; dialogue has a boomy lav tone |
| Count layers in busy moments | Three ambience layers and a music pad all occupying the same low-mid region |
| Mono check | Ambience partially cancels; dialogue becomes more prominent but tone becomes hollow (lav and boom misaligned) |
| Listening level | The mixer monitored loud; at moderate level, mud is more obvious |

**Repair (in order):**
1. Align lav and boom; use one where they conflict.
2. Remove one redundant ambience layer; reduce another.
3. Reduce low-mid energy in the dialogue (lav chestiness) and moderately in the music pad.
4. Re-automate music under dialogue.
5. Re-check at moderate level, on a phone and in mono.

**Verification:** level-matched A/B against the old mix; reviewers asked which is clearer without being told which is new.

## 13. Counterexample and repair — the over-limited mix

**Hypothetical counterexample.** To "make it punchy", a mixer limits a 60-second brand film heavily so that it measures very loud — far above the platform reference. On the platform, the player turns it down to the reference level. The result sounds flat and smaller than competitors' dynamic mixes; transients are blunted; the music's chorus has no lift because everything is equally loud; listeners describe it as fatiguing.

**Diagnosis:** loudness achieved by eliminating dynamics; normalisation removed the loudness gain and left only the damage.

**Repair:**
1. Return to the pre-limited mix; reduce limiting so transients survive.
2. Rebuild contrast deliberately: lower the verse sections, let the chorus and the product moment rise.
3. Set the master to a moderate integrated loudness appropriate to the destination and a true-peak ceiling per [Audio Delivery](../DELIVERY/Audio-Delivery.md).
4. Compare the new and old mixes **after level-matching** them (simulating normalisation).

**Verification:** after level-matching, listeners prefer the dynamic version for impact; measured LRA increases; true peak stays within the ceiling after encoding.

## 14. Micro-decisions

- Automate music before reaching for processors; most masking is solved by level and arrangement.
- Write dialogue automation with the listener's anticipation in mind: music can dip a fraction before a line starts.
- Keep reverbs on separate returns so they can be balanced and checked in mono.
- Leave the final limiter for the very end; check what it does by bypassing at matched level.
- Mark loud moments in the timeline and check each on headphones for distortion.
- Re-check the mix after every picture change; a one-second trim moves music edits and ambience transitions.

## 15. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Dialogue hard to hear at home | Mixed loud on big monitors; music too dense; low-level intelligibility not checked | Low-level checks; arrangement; automation |
| Pumping | Aggressive ducking or compression | Manual automation; gentler settings |
| Fatigue | Over-limiting; constant intensity | Restore dynamics and contrast |
| Hollow sound on phones | Phase issues; out-of-phase stereo | Align mics; narrow; mono checks |
| Bass disappears on phones | Low-only identity | Add mid-range harmonics/transients |
| Passes meter, sounds wrong | Numbers checked, listening skipped | Full-length listening pass on multiple systems |

## 16. Verification

- Full-length, uninterrupted playback with picture at a calibrated, moderate level.
- Low-level, phone-speaker, headphone and mono checks.
- Compliant measurement of required parameters on the delivered and encoded files.
- Level-matched A/B for any decision between versions.
- Remember the limits: measurements confirm compliance, not quality; small listening samples confirm intelligibility for those listeners, not for all.

## Dependencies

- Depends on: [Dialogue and Voice](Dialogue-and-Voice.md), [Recording and Cleanup](Recording-and-Cleanup.md), [Music Editing](Music-Editing.md), [Sound Design](Sound-Design.md), [Perspective and Silence](Perspective-and-Silence.md).
- Feeds: [Audio Delivery](../DELIVERY/Audio-Delivery.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

The measurement vocabulary is technical fact: integrated loudness with gating is defined in ITU-R BS.1770, and the 400 ms momentary and 3 s short-term windows in EBU Tech 3341 (referenced by EBU R 128). The specific broadcast targets cited are `[Requirement]` for their destinations as verified (see [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md)). Mix-tool comparisons, story-led hierarchy, monitoring practice and normalisation-aware dynamics are `[Practice]`. Examples are `[Illustrative]`.
