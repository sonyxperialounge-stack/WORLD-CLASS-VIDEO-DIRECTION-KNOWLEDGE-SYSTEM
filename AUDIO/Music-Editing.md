# Music Editing to Picture

**Purpose:** Teach how to edit music so that it keeps its musical logic while fitting picture — bars, phrases, pickups, stems, tails, transitions and endings — and how to decide between beat-aligned cuts, offbeat cuts, delayed impact and deliberate disagreement between music and picture.

**Applies to:** Library and licensed tracks, commissioned score delivered as stems, temp tracks, and cut-downs of any duration.

**Prerequisites:** [Music Selection](Music-Selection.md), [Cut Decisions](../EDITING/Cut-Decisions.md), [Decision Method](../FOUNDATIONS/Decision-Method.md) (frame/time conversions).

**Related owners:** Pacing across the piece in [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md); level and space in [Mix Strategy](Mix-Strategy.md); licence restrictions on editing in [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

---

## 1. Musical structure an editor needs

| Term | Meaning | Why it matters for editing |
|---|---|---|
| Tempo | Speed in beats per minute (BPM) | Determines beat spacing in frames |
| Beat | The basic pulse | Smallest common edit grid |
| Bar (measure) | A group of beats (often 4 in popular and library music) | Edits are most natural at bar boundaries |
| Downbeat | The first beat of a bar | Strong edit point; transients there mask joins |
| Phrase | A musical sentence, commonly 4 or 8 bars in much popular and library music | Cutting mid-phrase sounds like interrupting a sentence |
| Section | Intro, verse, chorus, bridge, breakdown, outro | Rearranging sections changes the emotional shape |
| Pickup (anacrusis) | Notes that lead into a downbeat from the previous bar | A pickup belongs to the downbeat after it; cutting it off sounds abrupt |
| Harmony / chord | Notes sounding together | Joining two points with different chords can clash |
| Key | The tonal centre | Joining sections in different keys sounds wrong unless modulating deliberately |
| Tail | Reverberation and decay after notes | Cutting tails sounds chopped; overlapping tails from different chords clash |

### Beats and frames

Beats rarely fall exactly on frame boundaries. At 120 BPM a beat lasts 0.5 s:

| Frame rate | Frames per beat at 120 BPM | Consequence |
|---|---|---|
| 23.976 fps | ≈ 11.99 | Beats drift very slowly against whole frames; nearly every beat is within a fraction of a frame of a 12-frame grid for short pieces |
| 25 fps | 12.5 | Beats alternate between 12- and 13-frame spacing; you cannot cut exactly on every beat |
| 29.97 fps | ≈ 14.99 | Close to 15 frames per beat |

A cut placed on the nearest frame is at most half a frame away from the beat (≈ 21 ms at 23.976 fps, 20 ms at 25 fps, ≈ 17 ms at 29.97 fps). Whether that offset is perceptible depends on the sound and image; viewers generally tolerate small audio-visual offsets, especially when sound arrives slightly after the image `[Heuristic]`. When precision matters (a hit on a visible impact), check by eye and ear at full speed rather than relying on the grid.

## 2. Edits that preserve musical logic

A music edit is successful when a listener who knows the track hears it as a plausible version of the music, and a listener who does not know it hears nothing wrong. Matching waveforms visually is not enough.

### 2.1 Where to cut

| Edit point | Why it works | Caution |
|---|---|---|
| Just before a strong downbeat transient (drum hit, plucked attack) | The new transient masks the join | Check that the outgoing tail does not clash harmonically |
| Phrase boundaries | Musical sentences remain intact | Phrase lengths vary; listen, don't count blindly |
| Between identical or harmonically matching bars | Seamless repetition or removal | Avoid repeating a distinctive melodic phrase too obviously |
| During a sustained note with no rhythmic content | Sometimes invisible | Pitch and tone must match exactly on both sides |

### 2.2 What breaks musical logic

- **Mismatched harmony** across the join (a chord on one side, a different chord sustaining across).
- **Severed pickups** (the lead-in notes cut off from their downbeat).
- **Cut tails** (reverb or sustain disappearing abruptly).
- **Lost phrase symmetry** (a 4-bar phrase becoming 3 bars where the listener expects 4) — sometimes acceptable in fast-moving pieces, often noticeable in melodic sections.
- **Repeated distinctive moments** (the same melodic hook heard twice in quick succession because of a loop).
- **Groove discontinuity** (a drum fill or swing feel that changes at the join).

### 2.3 Crossfades

- **Short crossfades** (a few milliseconds) at transient-masked joins avoid clicks without smearing the attack.
- **Longer crossfades** help in sustained, ambient sections, but can produce a "phasey" doubling when similar material overlaps.
- **Different crossfades per stem**, when stems exist, give the cleanest results (Section 3).

### 2.4 Endings

Endings are the hardest part to fake. Options:

| Ending | How | Fits | Risk |
|---|---|---|---|
| Natural ending (backtimed) | Place the track's real ending at the end of picture, then find an earlier edit point to join from | Most cases | Requires a usable edit point at the right distance |
| Button (final hit) | End on a strong final chord or hit, often with a short tail | Advertising, upbeat pieces | Abrupt if the tail is cut |
| Fade out | Gradual reduction | Rarely ideal; can suit ongoing, cyclical moods | Signals "we didn't finish the music" |
| Stinger / sting | A short separate cue for the end card | Branded endings | Can feel bolted on |
| Ring-out | Let the final chord decay naturally under the end card | Reflective endings | Needs time |

**Backtiming** `[Practice]`: align the music's natural ending with the end of picture (or with the moment the ending should land), then work backwards to find a bar or phrase boundary where the earlier part of the track can join. This preserves the most recognisable and satisfying part — the ending — and hides the edit in the middle.

## 3. Stems, phase, tails and sustained notes

**Stems** are separate audio files for groups of instruments (drums, bass, harmony, melody, effects) that, played together, reproduce the full mix.

| Advantage | How |
|---|---|
| Edit layers independently | Cut drums on a downbeat while letting a pad sustain across the join |
| Create breakdowns | Mute drums and bass for a bar of near-silence before a reveal |
| Make room for dialogue | Lower or remove the melody stem under speech |
| Build alternate durations | Extend with a pad loop while rhythm stems pause |

**Phase:** stems are designed to sum back to the full mix. Moving one stem in time relative to others by even a few milliseconds can cause flamming (doubled attacks) or comb filtering. Move stems together unless you intend a change.

**Tails:** when cutting a section, check whether the outgoing reverb tail continues into the new section; if the harmony changes, the tail clashes. Options: shorten the tail with a fade on that stem only; borrow a tail from a later point in the track that matches the new harmony; let the tail run over a moment of silence.

**Sustained notes** crossing an edit reveal any difference in pitch, dynamics or vibrato; avoid joins inside sustained notes unless both sides are identical.

## 4. Worked example 1 — Phrase-level rearrangement (hypothetical, Project B "Arc" 30 s, 23.976 fps)

**Track:** Track B from [Music Selection](Music-Selection.md#6-worked-example-1--track-evaluation-for-a-persuasive-product-film-hypothetical-project-b-arc-30-second-spot): 120 BPM, 4/4, so one bar = 2.0 s; 30 s = exactly 15 bars. Stems: drums, bass, guitar, pads.

**Original structure (hypothetical):** intro 4 bars (0:00–0:08), verse 8 bars (0:08–0:24), build 4 bars (0:24–0:32; suspended chord in bars 3–4), breakdown 2 bars (0:32–0:36), chorus 8 bars (0:36–0:52), … outro with natural ending in the final 4 bars (2:20–2:28) plus tail.

**Picture structure needed (from the repaired cut in [Cut Decisions](../EDITING/Cut-Decisions.md#10-counterexample-and-repair--the-mechanical-beat-synced-product-montage)):** morning montage → hesitation → ring reveal → drink and claim → end card.

**Rearrangement:**

| Spot time (s) | Bars | Source section | Stems | Picture | Notes |
|---|---|---|---|---|---|
| 0.0–4.0 | 2 | Intro bars 3–4 | All | Alarm, kitchen | Starting at intro bar 3 avoids a long build; the pickup into bar 3 is kept |
| 4.0–12.0 | 4 | Verse bars 1–4 | All | Morning montage | Cuts follow action; a few land on downbeats as accents |
| 12.0–16.0 | 2 | Build bars 3–4 (suspended chord) | All | Desk; hand reaches toward Arc and hesitates | The suspended harmony supports anticipation |
| 16.0–18.0 | 1 | Breakdown bar 1 | Pads only (drums, bass, guitar muted) | The hover; ring lights on a soft product sound at about 17.0 s (beat 3) — not on a downbeat | Near-silence; the product sound is the event |
| 18.0–26.0 | 4 | Chorus bars 1–4 | All | Drink; claim text; ring settles | The chorus downbeat at 18.0 s lands on the cut to the drinking shot — one deliberate sync accent |
| 26.0–30.0 | 2 | Outro final 2 bars (natural ending) | All, then pads ring out | End card | Backtimed: the final chord lands at 28.0 s; tail decays under the logo |

**Join checks:**
- Verse bar 4 → build bar 3: harmony of the verse's last bar leads naturally into the build's suspended chord (checked by listening; in this hypothetical track, both sit on the same chord). Cut just before the build's downbeat snare.
- Breakdown → chorus: pads sustain across (pad stem crossfaded over 1 beat); drums enter on the chorus downbeat — the transient masks the join.
- Chorus bar 4 → outro final bars: the chorus bar 4 ends on the dominant chord in this hypothetical track, which resolves into the outro's final tonic — a natural cadence.

**Frame placement:** at 23.976 fps, 18.0 s ≈ frame 431.6 from the start; the cut is placed on frame 432 (≈ 18.018 s), an offset of under half a frame from the downbeat — checked at full speed.

**Verification:** a musician unfamiliar with the edit listens to the 30-second music alone: does it sound like a real arrangement? Then with picture at full speed, muted and unmuted, on a phone and on studio monitors.

## 5. Beat-aligned and offbeat cutting

This section answers the original question: *should a cut land on exactly the same frame as a musical hit?*

| Relationship | Effect | Use when | Risk |
|---|---|---|---|
| Exact coincidence (cut on the hit) | Reinforcement; impact; a sense of rightness | Reveals, punchlines, a decisive moment | Repeated, it becomes predictable, superficial or coercive |
| Anticipatory cut (a few frames before the hit) | The image is established when the hit lands, so the hit "lands on" the new image | When the new image must be read before the impact — a product, a face | Too early and the sync is lost |
| Delayed impact (cut a few frames after the hit) | The sound announces; the image follows — a sense of consequence or causation | Action, comedy (a sound gag), revelations where sound is the trigger | Can feel late if overdone |
| Offbeat cutting | Cuts on off-beats or syncopations; rhythmic interest | Dynamic montages that should not feel mechanical | Can feel random if not consistent with the music's groove |
| Phrase-level alignment, beat-free cutting within | Sections change with the music; individual cuts follow action | Most narrative and documentary uses of music | — |
| Deliberate disagreement | Picture rhythm independent of music; music as a bed or counterpoint | Observational material; irony; tension | Can read as sloppy if the music is strongly rhythmic |

**The core answer `[Heuristic]`:** precise coincidence can reinforce a reveal. Applied to every cut, it becomes predictable — the viewer anticipates each cut and stops attending to content — and can feel emotionally coercive, as if the film were forcing reactions on schedule. Experienced editors reserve exact sync for moments that deserve emphasis and let action, performance and thought decide most cuts, while respecting phrase boundaries for larger changes.

This does not contradict music-driven forms: in a music video or a dance piece, sustained synchronisation *is* the contract. The distinction is between a genre where rhythm is the content and one where rhythm supports other content.

## 6. Worked example 2 — Fitting a reflective cue (hypothetical, Project A "Second Shift", 25 fps)

**Cue:** a 58-second sparse piece (sustained pads, occasional piano notes), stems: pads, piano. Needed: from the dawn handover (4:45) through the end card (to 6:00) = 75 seconds.

**Problem:** the cue is 17 seconds short; its natural ending is beautiful and should be kept.

**Solution:**
1. **Backtime** the natural ending so the final piano note's decay ends as the end card fades (6:00).
2. **Extend** the middle by repeating a 4-bar pad passage (about 17 seconds at the cue's slow tempo) using the pad stem only, muting the piano during the repeat so no distinctive melodic phrase is heard twice.
3. **Align a harmonic change** — the cue's one chord change — with the generator stopping (a production sound event at about 5:05), so the music's single movement coincides with the night ending. This is a deliberate, single sync point; the rest of the cue floats freely against picture.
4. **Entrance:** the pads fade in under the ward's ambience over about 4 seconds starting at the cut to dawn, so the music's arrival is felt rather than heard as a start.

**Verification:** audio-only pass — does the cue sound like a continuous piece? Full-speed with picture — does the harmonic change feel motivated by the generator stopping, without seeming contrived? Compare with the no-music version (see [Music Selection](Music-Selection.md#7-worked-example-2--a-reflective-documentary-scene-hypothetical-project-a-second-shift)).

## 7. Counterexample and repair — the waveform-aligned join

**Hypothetical counterexample.** For the Arc 90-second brand film, an editor shortens a track by joining the end of the first chorus to the start of the final chorus, aligning the drum transients visually on the waveform. It looks perfect on the timeline. On listening: a "hiccup" — the pad from the first chorus's last chord (a minor chord in this hypothetical track) sustains into the final chorus's first chord (major), clashing for about a second; the reverb tail of a vocal-like synth cuts off abruptly; and the drum fill that led into the final chorus is gone, so the energy jumps.

**Diagnosis:** the edit matched transients but ignored harmony, tails and the pickup (the drum fill).

**Repair:**
1. Move the join to the downbeat of a bar where both sides share the same chord (found two bars earlier in the first chorus).
2. Keep the drum fill: join *before* the fill, so the fill leads into the final chorus as composed.
3. With stems: fade the pad stem's outgoing tail over a beat while the incoming pad enters; keep the drum cut tight on the downbeat.
4. Check for repetition: the melodic hook now appears twice within 10 seconds — acceptable here because it is the chorus's natural repetition.

**Verification:** listen without picture; ask someone unfamiliar with the edit to identify where it is. If they cannot, the edit works. Then check with picture that the final chorus still lands on the intended shot.

## 8. Micro-decisions

- Keep music edits on separate tracks, labelled with source bar numbers, so changes are traceable.
- After any picture change, re-check every music edit downstream; a one-second picture trim can push a hit off its image.
- Avoid cutting music and picture on exactly the same frame at every section change; offset some transitions (music changes slightly before or after the cut) to keep them organic.
- Use the music's own dynamics before mix automation: choose sections that are naturally quieter under dialogue.
- When a hit must align with a visible impact, check by frame-stepping *and* at full speed.

## 9. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Audible "hiccup" | Harmony clash, cut tail or severed pickup | Move join to matching harmony; keep pickup; manage tails |
| Music feels "chopped" | Cutting mid-phrase repeatedly | Edit at phrase boundaries; use stems |
| Repetition noticed | Looping a distinctive phrase | Loop pads/rhythm only; vary sections |
| Ending feels fake | Fade or abrupt cut instead of a real ending | Backtime the natural ending |
| Cuts feel mechanical | Every cut on the beat | Reserve sync for accents |
| Hit lands on the wrong image after a re-edit | Downstream drift | Re-check and re-time after picture changes |

## 10. Verification

- Music-only listening for musical plausibility.
- Full-speed picture with music, muted dialogue, then with full mix.
- Phone speakers and headphones (small speakers may hide or expose edits differently).
- Re-check after every picture change and after loudness normalisation on the destination (see [Audio Delivery](../DELIVERY/Audio-Delivery.md)).

## Dependencies

- Depends on: [Music Selection](Music-Selection.md), [Cut Decisions](../EDITING/Cut-Decisions.md), [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md).
- Feeds: [Mix Strategy](Mix-Strategy.md), [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md) (cut-downs).
- Licence limits on editing: [Rights, Consent and Disclosure](../OPERATIONS/Rights-Consent-and-Disclosure.md).

## Confidence summary

Bar/phrase editing, backtiming, stem-based edits and harmony/tail checks are `[Practice]`. Beat-frame arithmetic is exact. Perceptual tolerance of small audio-visual offsets is a `[Heuristic]`. The guidance on reserving exact sync for emphasis is a `[Heuristic]` with an explicit exception for music-driven genres. Track structures and timings are `[Illustrative]`.
