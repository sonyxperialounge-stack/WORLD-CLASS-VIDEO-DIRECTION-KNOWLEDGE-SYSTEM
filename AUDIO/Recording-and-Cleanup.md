# Dialogue Recording and Cleanup

**Purpose:** Teach the capture decisions that make dialogue easy to finish, and the cleanup interventions that repair what capture could not prevent — each tied to an observed problem, with the tension between pristine cleanup and natural presence made explicit.

**Applies to:** Interviews, location dialogue, voice-over, ADR, remote recordings.

**Prerequisites:** [Decision Method](../FOUNDATIONS/Decision-Method.md) (dBFS vs LUFS distinctions).

**Companion chapter:** [Dialogue and Voice](Dialogue-and-Voice.md) covers the first listen, dialogue editing, VO and ADR direction. Mix-level decisions are owned by [Mix Strategy](Mix-Strategy.md).

---

## 1. Capture is cheaper than repair

Every dialogue problem is easier to prevent than to fix. A microphone moved 30 cm closer to the mouth can do more for intelligibility than hours of restoration, because the ratio of voice to room and noise improves at the source. Restoration tools have become remarkable, but they work by estimating what is speech and what is not; the worse the ratio, the more they guess, and the more their guesses sound artificial.

The principle `[Practice]`: **solve at the source, then in the edit, then with processing** — in that order.

## 2. Capture decisions

### 2.1 Microphone choice and placement

| Microphone approach | Strength | Weakness | Use |
|---|---|---|---|
| Boom (directional mic overhead or below frame, aimed at the mouth) | Natural perspective; consistent tone; no clothing noise | Needs an operator; distance varies with framing; room reflections in reverberant spaces | Drama, interviews, observational scenes where possible |
| Lavalier (small mic on clothing) | Close to the mouth; good in noisy places; frees the operator | Clothing rustle; chest-voice tone; head turns change level; visible if not hidden | Interviews, documentary, moving subjects |
| Both, recorded to separate tracks | Choice in post; backup | More channels to manage; phase issues if mixed carelessly | Interviews where quality matters (Project A) |
| Close voice-over mic in a treated space | Clean, intimate, controllable | Can sound detached from picture if too close and dry | Narration |
| Camera-mounted mic | Convenient | Distant from the subject; captures camera handling and the operator | Scratch audio for sync; ambience; run-and-gun as last resort |

**Placement principles:**
- **Distance:** the closer to the mouth (within practical and visual limits), the better the voice-to-noise and voice-to-room ratios.
- **Consistency:** keep distance and angle consistent through a take and between takes that will be intercut; changes in distance change tone and room sound.
- **Plosives and breath blasts:** angle the mic slightly off the direct breath path; use pop protection for VO.
- **Lav rustle:** secure the cable and capsule; avoid contact with moving fabric, jewellery, beards; check while the subject moves and gestures.

### 2.2 Room control

- Listen before choosing: fans, fridges, air conditioning, traffic, generators, fluorescent ballasts, neighbouring rooms.
- With permission, switch off noise sources during takes; leave a reminder note on the fridge so it is switched back on.
- Reduce reverberation with soft materials (blankets, cushions, curtains) placed off-camera, especially near reflective surfaces close to the subject and mic.
- Choose interview positions away from walls and corners where reflections build up.

### 2.3 Gain staging and recording format

- **Gain staging** sets the recording level so the voice is well above the recorder's noise and safely below clipping. With 24-bit recording, a practical approach `[Heuristic]` is to let normal speech peak comfortably below full scale (for example in the region of −20 to −10 dBFS, with loud moments still well under 0 dBFS); exact values depend on the source, the recorder and the expected dynamics.
- **Clipping** (signal exceeding 0 dBFS in a fixed-point recording) creates distortion that is difficult to repair and impossible to undo fully.
- **32-bit float recording** (offered by some recorders) greatly reduces the risk of clipping at the converter and in the file, because the format can represent levels above 0 dBFS that can be lowered later. It does not prevent overload *before* the converter — at the microphone capsule or in an analogue stage — and it does not improve a poor microphone position.
- **Safety track:** many recorders can record a second copy of a channel at lower gain; useful for unpredictable shouts.
- **Sample rate and timecode:** match the project (commonly 48 kHz for video) and set the recorder's timecode frame rate correctly (see [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#63-dual-system-specifics)).

### 2.4 Monitoring

Monitor with closed headphones at a consistent level. Listen for rustle, distortion, radio interference on wireless systems, distant noises, and changes in room tone. Many problems are only audible on headphones; equally, some low-frequency rumble is only obvious on speakers — note it for post.

### 2.5 Backup and room tone

- Record a backup where possible (dual recording, a second recorder, or the lav and boom on separate tracks).
- Record **room tone** — at least 30 seconds of the room with everyone still and the same noise conditions — at every location and whenever conditions change. Room tone is the raw material for filling gaps in the edit.

## 3. Low-budget improvements, ranked by value

| Improvement | Typical value | Cost |
|---|---|---|
| Choose a quieter room / switch off noise sources | Very high | Time and negotiation |
| Move the mic closer | Very high | None |
| Add soft materials near the subject | High in reverberant rooms | Blankets, cushions |
| Record room tone and handles | High (enables clean editing) | 30 seconds per setup |
| Use a lav when no boom operator exists | High | Low-cost lavs are widely available |
| Phone-as-recorder near the mouth (as a backup lav) | Moderate–high | Phone, adapter |
| Better microphone | Moderate, after the above | Variable |
| Restoration software | Moderate; limited by source quality | Licence, time |

## 4. Cleanup: interventions tied to problems

Each intervention should answer a specific observed problem. Applying a standard "dialogue chain" to every clip treats symptoms that may not exist and creates artefacts that did not.

| Observed problem | Intervention | What it does | Typical artefact when overdone |
|---|---|---|---|
| Clicks, crackles, mouth noises | De-click / mouth de-click | Detects and interpolates short transients | Dulled consonants; smeared plosive attacks |
| Steady broadband noise (fan, HVAC, hiss) | Noise reduction (profile-based or adaptive), or machine-learning dialogue isolation | Reduces energy identified as non-speech | Warbling "musical noise"; underwater or metallic tone; removed breaths; voice thinning |
| Hum (mains frequency and harmonics; 50 Hz in India and Europe, 60 Hz in the Americas) | De-hum or narrow notch filters at the fundamental and harmonics | Removes tonal components | Hollow or phasey voice if too many notches; residual buzz if harmonics remain |
| Low-frequency rumble (traffic, handling) | High-pass filter | Removes energy below the voice's useful range | Thin voice if cutoff is too high for a deep voice |
| Reverberation | De-reverb | Reduces the reverberant tail | Swirling, chorus-like or gated sound; loss of natural space |
| Plosives ("p", "b" pops) | Targeted low-frequency reduction on the event; clip-gain; de-plosive tools | Reduces the low-frequency blast | Weak consonants |
| Sibilance (harsh "s", "sh") | De-esser | Reduces high-frequency peaks on sibilants | Lisping sound |
| Uneven level | Clip-gain and automation first; then gentle compression | Consistency | Pumping; raised noise floor; flattened performance |
| Tonal imbalance (boomy, nasal, dull) | Equalisation | Reshapes spectrum | Unnatural tone; mismatch with other speakers |
| Clipping | De-clip | Reconstructs clipped peaks | Partial improvement only; severe clipping remains distorted |

**No fixed settings.** A boomy voice in a small room and a thin voice on a cheap lav need opposite EQ; a de-noise amount that suits a steady fan destroys a breathy whisper. Settings are chosen by listening to the specific clip, with comparisons at matched loudness.

### 4.1 Order of operations — a reasoned default

A common default `[Heuristic]`:

1. **Edit first:** remove unwanted sections, choose the cleanest takes and words (see [Dialogue and Voice](Dialogue-and-Voice.md)).
2. **Repair transient problems:** de-click, de-plosive, de-clip.
3. **Remove tonal noise:** de-hum.
4. **Reduce broadband noise and reverberation**, sparingly.
5. **Shape tone:** EQ.
6. **Control dynamics:** clip-gain/automation, then gentle compression, then de-essing.
7. **Fill gaps** with room tone and crossfades (editing).

Reasons: compression before noise reduction raises the noise floor between words, making noise reduction work harder; EQ boosts before de-noise can emphasise noise. Exceptions exist — for example, a strong high-pass before noise reduction can help some tools by removing rumble that confuses their estimates.

## 5. Pristine versus natural

Over-cleaned dialogue is a recognisable failure: it sounds isolated, close, airless and slightly synthetic, and it often clashes with picture (a voice that sounds like a studio over a shot of a busy ward). Breaths, small room sounds and natural ambience are part of how speech is perceived as real and present.

| Clean enough | Too clean |
|---|---|
| Speech fully intelligible at the intended playback level | Speech intelligible, but breaths and room removed |
| Noise reduced so it is not distracting, but some room remains | Gaps between words are digitally silent or gated |
| Consistent ambience across edits | Ambience pumps up and down with speech |
| Voice tone consistent with the shot's perspective | Close, dry voice over a wide shot |

**Repair sequence when cleanup has gone too far:** back off processing (reduce noise-reduction amount; bypass de-reverb); restore breaths that carry meaning; lay a continuous room-tone bed under the dialogue to replace gated silence; match perspective with subtle reverb only if necessary. Add processing *after* removing excess processing, never on top of it.

## 6. When to re-record, and what is irrecoverable

| Situation | Restoration likely enough? | Better option |
|---|---|---|
| Steady fan noise under clear speech | Usually yes | — |
| Loud intermittent noise (car horn) during a key word | Sometimes (spectral repair) | Alternative take; cutaway with re-recorded line if contract allows |
| Speech masked by other speech at similar level | Rarely | Alternative take; caption with "[overlapping]"; drop the line |
| Heavy room reverberation from a distant mic | Partly | ADR (fiction); re-interview (documentary, disclosed if relevant); accept and caption |
| Severe clipping on key lines | Partly | Alternative take; re-record |
| Missing words (dropout) | No — cannot recover what was not recorded | Alternative take; restructure |
| Wireless interference bursts | Partly | Backup track; alternative take |

**Irrecoverable** means the information was never captured: a word lost in a dropout, speech fully masked by louder speech, distortion that destroyed the waveform. AI voice reconstruction can *generate* plausible words, but in factual work that is fabricated speech (see [Performance Editing](../EDITING/Performance-Editing.md#6-rearranged-fabricated-and-ai-modified-performance)). Specialist dialogue restoration services can sometimes achieve more than general tools — worth considering for irreplaceable testimony.

## 7. Worked example 1 — Noisy location interview (hypothetical, Project A)

**Recordings:** lav (track 1) and boom (track 2) on Asha's interview; ceiling fan, intermittent generator hum (50 Hz plus harmonics), corridor traffic, window open to the street.

**Before diagnosis (hypothetical observations on headphones and speakers):**

| Track | Observation |
|---|---|
| Lav | Clear voice; slightly chesty tone; occasional rustle when Asha gestures; fan noise lower than on the boom |
| Boom | More natural tone; more fan and room; the generator hum is more audible |
| Both | Generator starts mid-answer at 10:30:58 (the "I stopped noticing" passage); a motorcycle passes at 10:31:12 during a pause |

**Decision record:**

| Field | Entry |
|---|---|
| Intent | Asha's words fully intelligible on phone speakers and at a community screening; the ward's world still present; her pauses intact |
| Evidence | As above (hypothetical) |
| Constraint | Editor also mixes; standard restoration tools; two-week schedule |
| Alternatives | (1) Lav only, heavy de-noise. (2) Boom only, de-hum and moderate de-noise. (3) Lav as the main voice with a small amount of boom blended for natural tone, phase-aligned; de-hum on the generator section; light de-noise; room-tone bed. |
| Choice | (3) |
| Trade-off | More editing work (phase alignment, rustle repair on the lav); some fan remains — accepted as "the room" |
| Exception | If blending creates comb-filtering (hollow tone) that cannot be resolved, use the lav alone with a touch of EQ to reduce chestiness |
| Validation | Listen at low volume on a phone speaker and on headphones; ask a Hindi-speaking listener to transcribe a difficult passage without captions; compare with and without processing at matched loudness |

**Processing sequence applied (described, no fixed settings):**
1. Align boom to lav (the boom is farther away and arrives later; align by a few milliseconds to avoid comb filtering), check polarity.
2. Spectral repair on three rustle events and the motorcycle in a pause (the motorcycle sits in a pause, so it can be replaced with room tone instead).
3. De-hum on the generator section only, with automation so the effect starts when the generator does.
4. Light broadband de-noise across the interview, set by ear until the fan recedes without warble; breaths preserved.
5. Gentle EQ: reduce chestiness on the lav; high-pass set by ear for her voice.
6. Clip-gain for consistency; gentle compression.
7. Room-tone bed (from recorded tone) under all interview sections so pauses are not silent.

**After diagnosis:** voice intelligible on a phone at low volume; the 4-second pause sounds like a room, not a dropout; the generator's arrival is barely perceptible in the voice but still audible as a distant presence — appropriate, because the ward observational scenes include it.

## 8. Worked example 2 — Budget voice-over recording (hypothetical, Project C)

**Situation:** the narration for both language versions is recorded in an office meeting room with hard walls.

| Problem | Low-budget fix | Result |
|---|---|---|
| Hard-wall reflections | Narrator faces into a corner hung with two heavy blankets; mic close (with pop protection), blankets behind the narrator too | Most early reflections reduced |
| Air-conditioning noise | Switched off for takes, with breaks to cool the room | Clean noise floor |
| Plosives | Mic angled slightly off-axis | Fewer pops |
| Inconsistent distance between sessions | Mark mic and chair positions with tape; photograph setup | Consistent tone across days |

**Verification:** compare the first and last takes of each session, and sessions on different days, at matched loudness; check consistency before editing.

## 9. Counterexample and repair — the robotic interview

**Hypothetical counterexample.** A documentary editor applies an AI dialogue-isolation tool at full strength to an interview recorded in a café. The background disappears completely. Feedback: "She sounds like she's in a different room from the picture." "Something is weird about her voice." On close listening: warbling on sustained vowels, breaths removed, consonant tails chopped, and dead silence between phrases while the picture shows a busy café.

**Diagnosis:** over-processing; gated silence; perspective mismatch between a close, dry voice and a wide café image.

**Repair:**
1. Reduce isolation strength until warble disappears; accept some café sound.
2. Blend a little of the unprocessed signal back in (if the tool allows), or use a lighter noise-reduction method on the whole and stronger processing only on difficult phrases.
3. Lay continuous café ambience (recorded on location, or the room tone extracted from pauses) under the dialogue, so pauses have a world.
4. Check perspective on wide shots; consider a slightly lower dialogue level or subtle early reflections if the voice still feels pasted on.

**Verification:** A/B the repaired and over-processed versions at matched loudness, with picture; the repaired version should sound like a person in that café, while every word remains intelligible.

## 10. Micro-decisions

- Record room tone with the same mic positions and gain as the takes.
- Note on the sound report any noises you could not control, with timecode.
- Keep processing non-destructive (rendered copies plus originals) so decisions can be revisited.
- Compare processed and unprocessed versions at *matched loudness*; louder always sounds "better" at first.
- Automate processing amounts per section rather than one setting for a whole interview.
- Do not de-noise music or effects with dialogue tools; process stems separately.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Warbling, metallic voice | Excessive noise reduction | Reduce amount; process in smaller sections |
| Voice pumps with background | Gating or aggressive compression | Room-tone bed; gentler dynamics |
| Thin voice | High-pass too high; EQ cuts | Lower cutoff; restore body |
| Hollow, phasey tone | Two mics combined out of alignment or polarity | Align; check polarity; use one mic |
| Lisp-like "s" | De-esser too strong | Reduce; target more precisely |
| Voice feels detached from picture | Over-cleaned; no ambience; perspective mismatch | Ambience bed; restore natural room |

## 12. Verification

- Headphones (detail and artefacts), ordinary speakers (balance), phone speaker at low volume (intelligibility), and the target playback situation (e.g., projection with a small PA).
- Matched-loudness A/B comparisons.
- Source-context checks: restoration must not change words or meaning.
- State honestly when a defect is irrecoverable or requires specialist intervention.

## Dependencies

- Depends on: [Interview Craft](../STORY/Interview-Craft.md) (location and mic choices), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md).
- Companion: [Dialogue and Voice](Dialogue-and-Voice.md).
- Feeds: [Mix Strategy](Mix-Strategy.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md).

## Confidence summary

Source-first capture, room tone, problem-specific processing and matched-loudness comparison are `[Practice]`. Mains-frequency facts (50/60 Hz) are technical facts. Level ranges and order of operations are `[Heuristic]` defaults with stated exceptions. Claims about 32-bit float recording describe the format's general capability; specific recorder behaviour must be checked in manufacturer documentation. Examples are `[Illustrative]`.
