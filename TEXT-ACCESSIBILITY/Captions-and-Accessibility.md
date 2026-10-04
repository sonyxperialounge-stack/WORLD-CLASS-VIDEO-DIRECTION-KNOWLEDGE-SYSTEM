# Captions, Subtitles, Reading Load and Accessibility

**Purpose:** Teach caption and subtitle craft — types, timing against speech, chunking, reading load, line breaks, speaker and sound information, placement, contrast — plus the conflicts between captions and the image, interchange formats, and the accessibility needs of different audiences.

**Applies to:** Every piece with speech or meaningful sound, in every language and version.

**Prerequisites:** [Typography System](Typography-System.md) (visual styling of open captions).

**Owns:** Caption timing, reading-rate reasoning, caption line breaking and placement rules, caption interchange formats, and accessibility alternatives (transcripts, audio description, reduced motion). Script-specific language behaviour is owned by [Localization](Localization.md); destination delivery requirements by [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

---

## 1. Kinds of on-screen text that carry speech or sound

| Type | What it is | Who controls appearance | Purpose |
|---|---|---|---|
| Closed captions | A separate track the viewer can turn on/off; rendered by the player | Player (often user-adjustable) | Accessibility for Deaf and hard-of-hearing viewers; muted viewing |
| Open captions (burned-in) | Text rendered into the picture | Producer | Guaranteed display where players lack caption support or viewers start muted; social video |
| Subtitles | Translation of speech into another language | Either | Language access |
| SDH (subtitles for the Deaf and hard of hearing) | Subtitles that also include speaker identification and sound information | Either | Accessibility plus language |
| Speaker identification | Labels or positioning that indicate who speaks | Either | Clarity with multiple or offscreen speakers |
| Sound labels | Descriptions of meaningful non-speech audio ([door slams], [generator stops]) and music (♪ with description or lyrics) | Either | Equal access to the soundtrack's meaning |
| Kinetic or highlighted text | Expressive animated words, often synced to speech | Producer | Expression, emphasis, social style |
| Other on-screen copy | Titles, labels, claims | Producer | Information (see [Typography System](Typography-System.md)) |

**A key distinction:** stylised word-by-word highlighting popular in social video is not automatically an accessible caption. It often omits sound information and speaker identification, may be hard to read for some users (constant motion, colour-only emphasis), and cannot be adjusted by the viewer. When accessibility is required, provide a proper caption track (closed or open) even if a stylised version also exists.

## 2. Timing against speech

### 2.1 In and out points

- **In point:** a caption should appear when the speech it represents begins — not noticeably early (which gives away the line, especially a punchline or reveal) and not late (which disconnects text from voice and face).
- **Out point:** it should remain until the speech ends and long enough to be read, but not linger so long that it overlaps the next speaker or a shot change awkwardly.
- **Synchronicity matters for lip-readers and for comprehension:** many hard-of-hearing viewers combine captions with lip-reading and residual hearing.

### 2.2 Syntactic chunking

Break text into caption events (and lines within them) at natural linguistic boundaries — clauses, phrases — rather than at arbitrary character counts.

| Poor chunking | Better chunking |
|---|---|
| "I stopped noticing I / was tired after a while." | "I stopped noticing / I was tired after a while." |
| "Brush the candle under / running water, then let it dry." | "Brush the candle under running water, / then let it dry." |

Avoid separating an article from its noun, a preposition from its object, a first name from a surname, or a verb from its auxiliary across lines, where possible.

### 2.3 Reading time and reading rate

Viewers need time to read. Reading speed varies with age, literacy, language, familiarity with captions, the complexity of the text and how much visual attention the picture demands. Destination style guides express limits as characters per second (cps) or words per minute (wpm). These are **destination requirements or editorial heuristics, not universal laws.**

Verified examples (checked 2026-10-04; see [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md)):

| Source | Guidance | Status |
|---|---|---|
| Netflix English (USA) Timed Text Style Guide | Up to 42 characters per line; up to two lines; reading speed up to 20 cps for adult programmes and up to 17 cps for children's programmes | `[Requirement]` for that destination and language |
| BBC subtitle guidelines (as reported by secondary sources; primary page not directly fetched) | Presentation rate around 160–180 wpm, with editorial variation for shot changes, speech speed and content | `[Practice]`; verify against the current BBC document before claiming compliance |
| US FCC caption quality rules (47 CFR 79.1(j)) | Captions should be accurate, synchronous, complete and appropriately placed | `[Requirement]` for covered US television programming |

**How to use rates:** at 20 cps, a two-line caption of 60 characters needs about 3 seconds on screen. At 17 cps, about 3.5 seconds. Where speech is faster than the target reading rate allows, the caption author must either *edit* (condense) the text — permitted in some contexts and forbidden in others — or accept a higher rate. Verbatim versus edited captioning is a policy decision tied to the audience and destination: some audiences and regulators expect verbatim captions; some subtitle styles condense to maintain readability.

**Languages other than English:** cps limits do not transfer across scripts. Devanagari "characters" (code points) do not correspond one-to-one with visible letters or reading effort. Use the destination's language-specific guide where one exists (some platforms publish guides for Hindi and many other languages), or test with readers of the language.

### 2.4 Minimum duration, gaps and maximum duration

Very short captions flash by unreadably; captions that abut without a gap can look like a single flickering caption; very long captions can be mistaken for a stuck display. Many style guides set a minimum event duration of roughly a second or a little less, a small minimum gap between consecutive events (often a couple of frames), and a maximum duration of several seconds. Exact values vary by destination; check before claiming compliance.

## 3. Line breaks, lines and punctuation

- **Lines per caption:** commonly at most two in subtitle and caption guides `[Practice]`; more lines obscure the picture and overload reading.
- **Line length:** destination limits vary (e.g., 42 characters per line for Netflix English). Shorter lines are easier to read on phones.
- **Line shape:** when breaking a two-line caption, prefer a balanced or bottom-heavy shape in many styles, but linguistic boundaries take priority over shape.
- **Punctuation:** keep sentence punctuation; use ellipses or dashes per the style guide for interrupted or continuing speech; avoid ending every caption with "…".
- **Italics:** commonly used for offscreen voices, voices on phones/radios, foreign words, or song lyrics, depending on the style guide.

## 4. Speakers, sound and music

### 4.1 Speaker changes

| Situation | Common technique |
|---|---|
| Two speakers in one caption | Each line begins with a dash (style-guide dependent) |
| Speaker offscreen or not obvious | Label: "ASHA:" or "[Asha]"; or position the caption near the speaker |
| Many speakers | Labels; consistent positioning; avoid colour-only identification |
| Overlapping speech | Prioritise the meaningful line; mark overlap when it matters; do not invent words lost in the overlap |

Colour coding of speakers is used in some regions (e.g., teletext traditions), but should not be the *only* cue: colour-vision differences and player overrides make it unreliable.

### 4.2 Meaningful sound and music

Caption sounds that carry meaning — story-relevant sounds, offscreen events, tone of voice where it changes meaning — not every sound.

| Include | Usually omit |
|---|---|
| [generator stops] when the silence matters | Constant generator hum already established |
| [patient coughing offscreen] if characters react | Background coughs with no story function |
| [door slams] that interrupts the argument | Footsteps of a character we see walking |
| ♪ gentle piano music ♪ when music sets mood with no dialogue | Music under dialogue when it adds nothing to meaning (guide-dependent) |
| [sarcastically] when the words alone would mislead | Manner of speaking that is obvious from the words |

Lyrics: when lyrics matter to meaning (or when a regulator requires them — the FCC accuracy standard includes lyrics of music in the audio track), caption them, marked as lyrics.

## 5. Conflicts: speech, shot changes, action and reading

Captions live in the same frame and time as picture. Four forces compete:

1. **Speech timing** — captions should follow speech.
2. **Shot changes** — a caption that starts or ends a few frames before or after a cut causes a visible "flicker" as the image changes under it.
3. **Visual action** — important action, faces or on-screen text may be covered.
4. **Reading time** — the viewer needs time to read and to look at the picture.

### Resolving them

| Conflict | Options | Choose when |
|---|---|---|
| Caption ends a few frames after a cut | Snap the out point to the cut, or extend clearly past it (well into the next shot) | Snap when reading time allows; extend when the next shot continues the same speaker |
| Caption starts a few frames before a cut | Delay to the cut if speech allows; or start at speech and accept | Delay when the offset is small and lip sync is not critical |
| Caption covers crucial action (hands demonstrating a step) | Move the caption (top position); regroup text into a shorter caption; adjust the shot (hold longer so the step is visible after the caption) | Move first; editorial changes if the conflict recurs |
| Caption collides with a lower third | Raise the caption above it, or delay the lower third, or move the lower third to the top | Decide a consistent rule in the design system |
| Caption collides with on-screen text in the image (signs, documents) | Move the caption; if the on-screen text matters, caption it as well (translated) | Always ensure meaningful on-screen text is accessible |
| Speech is too fast to read | Edit text (if allowed); split into more captions; extend into pauses; ask whether the edit itself should breathe | Discuss with the editor when a whole passage is unreadable |

**Never protect layout at the cost of accuracy.** A caption that fits beautifully but changes meaning ("I didn't know" captioned as "I did know") is a failure regardless of timing quality.

## 6. Placement

| Element to avoid covering | Practice |
|---|---|
| Faces and mouths | Default bottom placement; move up when a face is low in frame; lip-readers need mouths |
| Important action | Move to top temporarily; keep the move consistent |
| Lower thirds and graphics | Define zones in the design system so they never collide |
| On-screen text in the footage | Reposition |
| Safe areas | Keep within the destination's caption-safe region |
| Platform interface overlays | Especially in vertical feeds, bottom areas may be covered by buttons and descriptions; check the destination layout (see [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md)) |

**Aspect ratios:** caption placement must be designed per version. A bottom-centred caption that works in 16:9 may cover the subject's mouth in a tight 9:16 crop, or sit under the interface. Closed captions are positioned by the player (sometimes with positioning information in the file); open captions are fixed by the producer and must be checked per version.

## 7. Contrast over variable backgrounds

| Approach | Strength | Weakness |
|---|---|---|
| Solid or semi-opaque box behind text | Reliable over any background | Covers more picture; heavier look |
| Outline (stroke) | Covers little picture | Thick outlines clog small text; thin ones fail over busy backgrounds |
| Drop shadow (soft or hard) | Subtle | May fail over mid-grey busy backgrounds |
| Outline + shadow | Common compromise | Can look dated or heavy |
| Darkened band at frame bottom | Even, unobtrusive | Depends on the image; may feel like a vignette |

For burned-in captions, test over the brightest and busiest frames. For closed captions, the player and user settings control the appearance; provide accurate data and positioning.

## 8. Audiences and their needs

| Audience | Needs | Design implications |
|---|---|---|
| Deaf and hard-of-hearing viewers | Complete speech; speaker identification; meaningful sound and music; synchronous timing | SDH-style captions; sound labels; no omission of meaningful audio |
| Viewers with colour-vision differences | Information not carried by colour alone | Speaker ID by label or position, not colour only |
| Viewers with motion sensitivity or attention differences | Stable text; minimal animation | No kinetic captions in the accessible track |
| Low-literacy viewers | Simpler vocabulary; shorter lines; slower rates; spoken information | Pair captions with clear audio; avoid captions as the *only* channel for essential instructions; consider audio-first design |
| Second-language viewers | Readable speed; consistent terminology; subtitles in a familiar language | Translation quality; slower rates; consistent glossary |
| Muted viewers (any) | Captions present from the first frame | Open captions on social; closed captions available elsewhere |
| Blind and low-vision viewers | Access to visual information | Audio description; spoken text; readable large type |

### Alternatives and companions

- **Transcripts:** a full text version of speech and meaningful sound, useful for search, review and some accessibility needs; for audio-described content, an extended transcript can include visual descriptions.
- **Audio description:** narration of important visual information in natural pauses, or an extended version that pauses the video. Needed when visual information is essential to understanding and is not spoken — common in demonstrations (Project C's cleaning steps are largely shown, not said). The editorial fix may be to *say* the essential visual information in the main narration, which benefits everyone.
- **Reduced-motion alternatives:** a version without kinetic text or heavy motion, where the destination supports multiple versions.

## 9. Language and accuracy

**Linguistic accuracy and timing accuracy are separate.** A perfectly timed caption can be wrong; an accurate caption can be badly timed. Check both, by different passes and ideally by different people.

- **Names, places, numbers and technical words** are the most common errors, especially in automatic transcription; verify against a name list and the script.
- **Negation and small words** ("can't"/"can", "never"/"ever") change meaning; verify every sentence with negation.
- **Inaudible or unclear speech:** do not fabricate. Use the destination's convention (for example "[inaudible]" or "[indistinct]") and, if a reasonable guess is useful, the convention for uncertainty. In factual work, an invented word in a caption is an invented quote.
- **Hindi/Devanagari:** proper shaping and font support; names spelled as the person prefers; consistent transliteration of English technical terms (e.g., whether "candle" is transliterated or translated); see [Localization](Localization.md).
- **Translation ambiguity:** idioms and politeness forms need adaptation, reviewed for meaning; see [Interview Craft](../STORY/Interview-Craft.md#10-ethics-from-the-first-session) for speaker review.
- **Right-to-left languages:** alignment, punctuation placement and mixed-direction numbers need RTL-aware tools and review.

## 10. Caption and subtitle interchange — capabilities, not products

| Delivery form | Typically preserves | Typically loses or varies | Common contexts |
|---|---|---|---|
| Simple sidecar text format (e.g., SRT) | Timing; text; line breaks | Positioning (no standard method), styling beyond basic tags, speaker metadata | Web platforms, many players, social uploads |
| Web timed-text format with cue settings (e.g., WebVTT) | Timing; text; line breaks; position and alignment; speaker voice tags; CSS-based styling | Styling support varies by player | Web video, HTML5 players |
| XML timed-text families (e.g., TTML and its profiles such as IMSC; EBU-TT) | Timing; text; detailed styling; positioning; regions; metadata | Some players support only subsets of the profile | Streaming services, broadcast, archives |
| Broadcast caption data (e.g., CEA-608/708 data, often carried in SCC files or embedded in video streams) | Timing; text; basic positioning | Character set and row-length limits (608), styling, non-Latin scripts in 608 | Broadcast, some streaming and platform ingest |
| Embedded caption track in the media file | Depends on the format embedded | Survival through re-encoding varies; some workflows strip tracks | Distribution masters |
| Burned-in (open) captions | Exact appearance and position | Cannot be turned off, resized, or extracted as text; must be redone for every change | Social feeds, festival screenings, guaranteed display |

**Conversion warning:** converting between formats commonly loses positioning, styling, speaker colours, line breaks or special characters, and can shift timing if frame rates or timecode conventions differ (see [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md#42-drop-frame-versus-non-drop-frame)). Never assume a delivered caption file survives every platform, player and version unchanged; check each destination's ingested result.

## 11. Worked example 1 — Interview with overlapping speakers (hypothetical, Project A "Second Shift", 25 fps)

**Scene:** at 2 a.m., Asha and her colleague Sunita (consent confirmed) share tea and talk quickly in Hindi, overlapping. The English subtitle version is being prepared (SDH style for the closed track; a condensed open-subtitle version for social).

**Source (hypothetical, translated meaning):**
- Sunita: "Did bed six settle?" 
- Asha (overlapping): "He's sleeping — finally."
- Sunita: "And you? When did you last eat?"
- Asha: (laughs) "Tea counts."
- [generator stops; silence]
- Sunita: "...There it goes again."

**Cue table (illustrative times, 25 fps timecode, English SDH closed track):**

| # | In | Out | Text | Notes |
|---|---|---|---|---|
| 1 | 01:02:10:05 | 01:02:11:20 | – Did bed six settle?<br>– He's sleeping — finally. | Dash per speaker; overlapping lines combined in one caption so both are read together; about 47 characters over 1.6 s ≈ 29 cps — **too fast** |
| 1 (revised) | 01:02:10:05 | 01:02:12:10 | – Did bed six settle?<br>– He's sleeping. Finally. | Extended out point into the pause after Asha's line (2.2 s for about 46 characters ≈ 21 cps); still slightly above 20 cps — accepted only if the destination allows; otherwise condense |
| 1 (condensed alternative) | 01:02:10:05 | 01:02:12:10 | – Bed six settled?<br>– Finally sleeping. | About 37 characters ≈ 17 cps; loses a little voice; acceptable in condensed subtitle styles, not in verbatim policies |
| 2 | 01:02:12:15 | 01:02:14:20 | And you?<br>When did you last eat? | Sunita; speaker clear from shot |
| 3 | 01:02:15:00 | 01:02:16:15 | [laughs] Tea counts. | Asha; laugh labelled because it changes meaning (light-heartedness) |
| 4 | 01:02:16:20 | 01:02:18:15 | [generator stops] | The silence is meaningful; the next line refers to it |
| 5 | 01:02:19:10 | 01:02:21:00 | SUNITA: There it goes again. | Speaker labelled because Sunita is offscreen in this shot |

**Decision:** the closed SDH track uses revised cue 1 if the destination guide permits the rate; otherwise the condensed alternative. The social open-subtitle version uses the condensed text. Both are checked by a bilingual reviewer for meaning.

**Shot change check:** cue 2's out point (01:02:14:20) falls 3 frames before a cut at 01:02:14:23 (hypothetical). Option: extend to the cut (01:02:14:23) to avoid a caption disappearing just before the image changes — chosen.

## 12. Worked example 2 — Dense tutorial labels (hypothetical, Project C "Clear Water", 29.97 fps NDF)

**Moment:** step 2. The narrator says, "Take out the candle and brush it gently under running water — no soap." On screen: hands removing and brushing the candle; a step label "Step 2: Brush (no soap)"; a diagram label briefly points to the candle surface. Burned-in captions are required for the social version; closed captions for the main version.

**Collision (hypothetical first pass):** the caption at the bottom covers the hands brushing the candle; the step label sits top-left; the diagram label pops in mid-frame. The viewer must read three text elements while watching a demonstration whose details (soft brush, no soap) matter.

**Reading/action collision analysis:**

| Element | Needed? | Conflict |
|---|---|---|
| Caption of narration | Yes (accessibility, muted viewing) | Covers the demonstration |
| Step label | Yes (navigation, recall) | Duplicates part of the caption |
| Diagram label | Marginal here (it appears in the mechanism section too) | Adds reading load |

**Repair:**
1. Move the burned-in caption to the top for this step (the action is in the lower half); keep the position rule consistent for all demonstration steps.
2. Move the step label to the upper-left *corner* above the caption zone, reduce to "Step 2" with an icon of a brush and a crossed-out soap symbol — the icon carries "no soap" without additional reading, and the narration/caption also says it.
3. Remove the diagram label from this shot; it appears in the mechanism section.
4. Extend the shot by about 1 second (from handles) so viewers can watch the brushing after reading.

**Verification:** test the social version on a low-cost phone, muted; ask a viewer to describe step 2. Then test the main version with closed captions on, in both languages. Check icon meaning with viewers who read less comfortably (the crossed-out soap must be unambiguous).

## 13. Counterexample and repair — kinetic captions as the only access

**Hypothetical counterexample.** A brand publishes a social video with animated, word-by-word captions: each word pops in with a bounce, key words turn yellow, emojis are inserted. There is no closed-caption track. A hard-of-hearing viewer comments that they cannot follow the dialogue when two people speak; another viewer reports the bouncing text makes them feel ill; the captions omit an important sound (a phone alarm that the joke depends on).

**Diagnosis:** expressive captions substituted for accessible captions; no speaker identification; no sound information; motion-heavy; colour used for emphasis only.

**Repair:**
1. Provide a closed-caption track with complete speech, speaker identification and sound labels where the platform supports it.
2. Revise the open captions: phrase-based (not word-by-word) display, no bounce, emphasis by weight rather than colour alone, sound label "[phone alarm]" added.
3. Keep a small number of expressive moments (one emphasised word in the punchline) where they serve the joke.

**Verification:** review by at least one Deaf or hard-of-hearing viewer where possible; check both tracks on the platform after upload.

## 14. Micro-decisions

- Snap caption in/out points to shot changes when within a few frames; avoid captions that straddle a cut by only a few frames.
- Keep a project glossary of names and terms for caption authors and translators.
- Leave a small gap between consecutive captions so viewers perceive a change.
- Do not split a number from its unit across lines.
- Re-time captions after every picture change; picture lock is not a guarantee (see [Production and Handoffs](../OPERATIONS/Production-and-Handoffs.md)).
- Caption the joke's setup and punchline in separate events when timing matters, so the punchline is not read before it is heard.

## 15. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Captions too fast | Speech density; verbatim policy | Extend into pauses; condense if allowed; edit picture to breathe |
| Captions flicker at cuts | In/out points near cuts | Snap to cuts |
| Captions cover faces or action | Fixed bottom placement | Reposition; design zones |
| Wrong names or negation | Unverified automatic transcription | Human verification; glossary |
| Captions missing on platform | Format not supported; track stripped on upload | Check ingest; use supported format; open captions as fallback |
| Hindi captions broken | Font/shaping; player support | Use supported fonts and formats; test players |
| Viewer can't tell who's speaking | No speaker ID | Labels; dashes; positioning |

## 16. Verification

1. **Accuracy pass** (text only, against audio and script), by a fluent reviewer for each language.
2. **Timing pass** at full speed: captions appear with speech, avoid cut flicker, allow reading.
3. **Placement pass** in every aspect ratio, including platform interface overlays.
4. **Encoded-file pass:** verify captions on the final encoded version — burned-in captions after compression, closed captions after ingest on the actual platform or player — not only inside the editor.
5. **Audience check** where possible with people who rely on captions.

## Dependencies

- Depends on: [Typography System](Typography-System.md), [Localization](Localization.md), [Ingest and Preparation](../OPERATIONS/Ingest-and-Preparation.md) (timecode convention).
- Interacts with: [Rhythm and Pacing](../EDITING/Rhythm-and-Pacing.md), [Design System](../MOTION-DESIGN/Design-System.md), [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md), [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md).
- Gate: [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

Netflix English limits and FCC quality categories are `[Requirement]` for their destinations, verified on 2026-10-04. BBC wpm guidance is `[Practice]` reported via secondary sources and must be verified before claiming compliance. Chunking, two-line maxima, shot-change snapping, sound-labelling principles and accuracy-first rules are `[Practice]`. Minimum duration and gap values are deliberately not specified because they vary by destination. Interchange capability descriptions are `[Practice]`; exact feature support varies by player and platform version. All cue times are `[Illustrative]`.
