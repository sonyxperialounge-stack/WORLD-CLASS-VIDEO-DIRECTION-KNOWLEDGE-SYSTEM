# Typography, Screen Text and Visual Hierarchy

**Purpose:** Teach how to choose and specify type for moving images — by function, emotional register and viewing condition — across screen sizes, aspect ratios and scripts, and how to build a typography specification that versions inherit.

**Applies to:** Titles, lower thirds, chapter labels, data annotations, calls to action, on-screen copy and open (burned-in) captions as a visual element.

**Prerequisites:** [Design System](../MOTION-DESIGN/Design-System.md).

**Ownership boundaries:** Caption timing, reading rate, line breaking for captions and placement rules are owned by [Captions and Accessibility](Captions-and-Accessibility.md). Script-specific language behaviour and translation are owned by [Localization](Localization.md). Platform safe areas and interface overlays are in [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md).

---

## 1. Separate text by function

Different kinds of screen text do different jobs and need different rules. Treating them as one "text style" causes most typographic problems.

| Function | Job | Reading condition | Priority |
|---|---|---|---|
| Title / title card | Announce, set tone | Often read while nothing else happens | Character and legibility |
| Lower third | Identify a speaker | Read while listening to the speaker | Speed of recognition; low distraction |
| Chapter label | Orient within the piece | Brief; often over footage | Consistency |
| Data annotation | Label values, units, sources | Read while interpreting a chart | Precision; numeral clarity |
| Call to action | Prompt an action | Often at the end; may be screenshot | Clarity; contrast; brevity |
| On-screen copy (claims, key phrases) | Carry meaning for muted viewers | Read while watching action | Brevity; timing with picture |
| Open captions (burned-in) | Transcribe/translate speech | Continuous reading alongside picture | Legibility; consistency; accessibility (see [Captions and Accessibility](Captions-and-Accessibility.md)) |
| Closed captions | Same, rendered by the player | Player-controlled styling | Data accuracy; the player owns appearance |

## 2. The variables of screen typography

| Variable | What it controls | Screen-specific considerations |
|---|---|---|
| Typeface | Voice, register, legibility | Open letterforms and generous x-height help at small sizes; very thin or high-contrast faces suffer from compression and scaling |
| Size | Readability at viewing distance | Must be tested at the smallest real viewing size, not on the edit monitor |
| Weight | Emphasis; resistance to backgrounds | Light weights disappear over busy footage; very heavy weights can clog at small sizes |
| Line length | Reading comfort | Short lines are faster to read on screen; long lines force eye travel across the frame |
| Leading (line spacing) | Line separation | Scripts with marks above and below the baseline (e.g., Devanagari) need more room |
| Tracking (letter spacing) | Texture, legibility, style | Slight positive tracking can help small text in Latin script; wide tracking breaks connected scripts |
| Alignment | Order; relationship to composition | Left alignment gives a stable starting edge; centred suits short titles; right alignment for right-to-left scripts |
| Case | Tone; scanning | All caps suit very short labels; for sentences, mixed case is faster to read `[Heuristic]` |
| Contrast | Legibility | Over moving images, worst-case frames decide |

### Emotional register

Type communicates before it is read. A rounded humanist sans feels approachable; a high-contrast serif feels editorial or luxurious; a condensed grotesk feels urgent; a monospace feels technical. These associations are cultural and genre-dependent `[Heuristic]`. Choose type by the brief's emotional stance, then confirm legibility — never the reverse.

## 3. Composition for small and large screens

### 3.1 No single correct size

Readable size depends on display size, viewing distance, resolution, the typeface's x-height, the background and the viewer's eyesight. A size that reads comfortably on a 27-inch monitor at arm's length may be too small on a phone held at the same distance, and oversized on a cinema screen. Platform players also scale video; a 1080×1920 vertical frame is displayed at many sizes.

**Illustrative starting point** `[Illustrative]`: for a 1920×1080 frame intended mostly for phone viewing, a lower-third name set so that its capital letters are roughly 4–5% of frame height (about 45–55 px), and the role line roughly 3–3.5% (about 32–38 px), in a typeface with a generous x-height. These are starting points for testing, not standards. For projection to a room, smaller relative sizes may suffice; for small phones with a busy background, larger may be necessary.

Express sizes in the specification **as a proportion of frame height** as well as pixels, so they scale coherently into other frame sizes.

### 3.2 Image complexity

Text over a calm, dark, out-of-focus background reads at a smaller size than the same text over a busy, bright, sharp background. Composition and grade decisions (a shallow depth of field, darker negative space) are typographic decisions too.

### 3.3 Safe areas and interface overlays

- **Title/action safe areas** guard against cropping by displays and players; many modern digital platforms crop little, but some displays, projectors and broadcast chains still overscan or crop. Follow the destination's specification.
- **Platform interface overlays** — buttons, captions, usernames, progress bars — cover parts of the frame on many social and video platforms, especially vertical feeds. Their positions change between platforms and app versions. Check the current destination layout (see [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md)).
- **Reframed versions** move text relative to subjects; text placed for 16:9 must be re-laid for 9:16, not cropped.

## 4. Wording, length and the edit

Text length is an edit decision. Longer text needs more screen time, larger areas and calmer backgrounds, which affects shot duration, motion and layout.

**Prefer concise truthful phrasing over shrinking type.** When text does not fit, the order of interventions is: shorten the wording (keeping accuracy) → simplify the layout → extend the hold or shot → reduce size only within tested limits.

| Too long | Concise and still truthful |
|---|---|
| "This bottle features an integrated LED progress indicator that displays your hydration progress throughout the day" | "Glows to show how much you've had today" |
| "Clean the ceramic candle with a soft brush under running water once per week" | "Once a week: brush the candle under running water" |
| "Asha [surname], Senior Staff Nurse (Night Shift), District General Hospital" | "Asha — night-shift nurse, District Hospital" (surname omitted by privacy agreement) |

### Punctuation, case, numerals and naming

- **Punctuation:** omit full stops on single-line labels and titles; keep them in sentences and captions. Use real quotation marks and apostrophes, not straight typewriter marks, unless the style is deliberately technical.
- **Capitalisation:** pick sentence case or title case for each role and use it consistently.
- **Numerals:** use tabular (fixed-width) figures for counters, timers and aligned columns so digits do not jiggle as they change; proportional figures for running text. In Hindi materials, decide between Devanagari digits and international (Western Arabic) digits in the style guide and apply consistently — many Hindi media use international digits, but the audience and client preference decide.
- **Abbreviations and units:** define once; keep consistent ("mL" not "ml" in one place and "mL" in another); put a space between number and unit where the style guide requires.
- **Naming consistency:** product names, people's names and places spelled identically in lower thirds, captions, end cards and descriptions — a common QC failure.

## 5. Multilingual typography

Detailed script behaviour, translation and adaptation are owned by [Localization](Localization.md). The typographic system must still be designed for every script it will carry.

### 5.1 Devanagari (Hindi) essentials for the type system

- **Shaping:** Devanagari requires a font and a text engine that apply shaping rules — combining consonants into **conjuncts** (e.g., क्ष, त्र, ज्ञ, श्र), positioning **vowel signs (matras)** above, below, before and after consonants, and reordering the short-i sign (ि) visually before its consonant. If shaping fails, text displays as broken sequences that native readers find wrong or unreadable. Test every graphics and caption tool with real Hindi text, including conjuncts.
- **The headline (shirorekha):** most letters hang from a horizontal top line that joins letters in a word. **Do not add letter-spacing** to Devanagari: tracking breaks the headline into fragments.
- **Vertical space:** marks above the headline and below the baseline need more leading than Latin text at the same size; clipped matras are a frequent error in tight lower-third boxes.
- **Visual size:** Devanagari at the same point size as a Latin face often appears smaller or larger depending on the fonts; harmonise by visual size (e.g., match the height of the headline region to the Latin x-height region), not by point size.
- **Font support:** choose families with complete Devanagari support and, ideally, a matching Latin design for mixed text (several open-source and commercial superfamilies are designed this way). Verify licensing for video and broadcast use.
- **Never split grapheme clusters:** line breaks, animations ("type-on" effects) and per-character styling must operate on whole grapheme clusters (a consonant with its matras and conjunct parts), not on individual code points. A per-character typewriter effect that reveals a bare consonant and then its matra looks broken.

### 5.2 Mixed scripts

Bilingual frames (Hindi and English together) need decisions on order, relative size and weight, and baseline alignment. Keep one script primary per frame where possible; when both appear, give them distinct positions rather than interleaving lines.

### 5.3 Right-to-left scripts

Where relevant (Arabic, Hebrew, Urdu), alignment, reading order of animated reveals, the side from which elements enter, and the position of numbers all mirror. Arabic-script languages also join letters, so the same rule applies: no letter-spacing, whole-cluster handling.

### 5.4 Translation versus copy adaptation

Translation renders meaning; **copy adaptation** rewrites for length, tone and cultural fit within approved meaning. Screen text almost always needs adaptation, because translated text expands or contracts and line breaks change. Adapted copy must be reviewed by a fluent reviewer for meaning, not only for spelling.

## 6. Text reveals: comprehension or obstruction

| Reveal type | Serves comprehension when | Obstructs when |
|---|---|---|
| Whole line fades in | Almost always; reading starts immediately | Rarely |
| Line-by-line stagger | Lines are separate ideas read in order | Lines form one sentence; viewers wait |
| Word-by-word (kinetic, synced to speech) | Expressive pieces; emphasis on a few words; music-driven | Informational content; viewers cannot scan ahead; fragmentation slows reading |
| Typewriter (character-by-character) | Stylistic signal of "typing" in short phrases | Long text; any connected script without cluster handling |
| Highlighted word in a caption line | Emphasis in social content | Used as a substitute for accessible captions; constant highlighting distracts (see [Captions and Accessibility](Captions-and-Accessibility.md)) |

Readers scan ahead. A reveal that withholds the rest of the sentence prevents scanning and slows comprehension `[Heuristic]`. Use reveals when withholding is expressive, not by default.

## 7. The typography specification

A specification makes typography reproducible across versions, languages and editors.

### Filled specification — Project C "Clear Water" (hypothetical; 1920×1080 master, 1080×1920 social cut; Hindi and English)

| Role | Font (Latin) | Font (Devanagari) | Weight | Size (% of frame height, 16:9) | Size in 9:16 | Line spacing | Colour/contrast approach | Motion | Padding | Max length |
|---|---|---|---|---|---|---|---|---|---|---|
| Title | Humanist sans family "A" | Matching Devanagari design of family "A" | Bold | 7% | 4.2% of height (≈ same physical size relative to width) | 1.15 (Latin), 1.35 (Devanagari) | Off-white on darkened footage or solid band | Fade 12 frames | — | 4 words / 1 line |
| Step label ("Step 2: Brush") | A | A-Devanagari | Semibold | 4.5% | 2.8% | 1.2 / 1.4 | Off-white text with soft local shadow; band if background is busy | Fade 10 frames; no translation | 0.6× cap height around text | 3–4 words |
| Diagram label | A | A-Devanagari | Regular | 3.2% | 2.2% | 1.2 / 1.4 | Dark text on light diagram | Fade after part settles | — | 3 words |
| Data annotation | A (tabular figures) | A-Devanagari + international digits | Medium | 3.2% | 2.2% | — | High-contrast on chart background | Fade with bar settle | — | 6 words + unit |
| Source line | A | A-Devanagari | Regular | 2.4% | 1.8% | — | 80% opacity off-white | No motion | — | 1 line |
| Call to action | A | A-Devanagari | Bold | 4.5% | 3.2% | — | Brand accent band, text dark | Fade | 1× cap height | 6 words |
| Open captions | See [Captions and Accessibility](Captions-and-Accessibility.md) | | | | | | | | | |

Fallback requirement: if family "A" is unavailable on a collaborator's system, work stops rather than substituting a system font; fonts are packaged with the project (licences permitting).

**How variants inherit:** the 9:16 version inherits roles, fonts, weights, colours and motion; only sizes and positions are re-specified; text-length limits remain, which forces copy adaptation rather than shrinking.

## 8. Worked example 1 — Informative corporate overlay (hypothetical)

**Context:** a logistics company's internal training video, 16:9, viewed on office monitors and phones. On-screen text summarises safety rules while a trainer speaks.

| Decision | Choice | Rationale |
|---|---|---|
| Typeface | Neutral sans with large x-height | Clarity; corporate register without coldness |
| Hierarchy | Rule number (large), rule text (medium), note (small) | Scannable |
| Layout | Left-aligned panel on the right third, footage of the trainer on the left | Text and speaker do not compete |
| Timing | Text appears as the trainer begins the rule, stays until the next rule | Viewers can read at their own speed and re-read |
| Motion | Simple fade; none during reading | Reading stability |
| Contrast | Solid semi-opaque panel | Footage background is a busy warehouse |

**Verification:** a fresh viewer pauses at random and reads each rule; check on a phone; check that the panel never covers the trainer's demonstrating hands.

## 9. Worked example 2 — Expressive music-video typography (hypothetical)

**Context:** a 3-minute music video for an independent artist; the lyrics are partly displayed as large, expressive type integrated with performance footage.

| Decision | Choice | Rationale |
|---|---|---|
| Purpose | Expression and rhythm, not transcription | The contract is expressive; accessible lyrics are provided separately as closed captions |
| Typeface | Condensed display face with an irregular texture | Matches the song's raw energy |
| Reveal | Word-by-word, synced to vocal phrasing, only on the hook | Emphasis where the song emphasises |
| Placement | Varies, interacting with the performer's movement; occasionally behind the performer (occlusion) | Presence rather than overlay |
| Legibility | Allowed to be partly obscured in verses — deliberate | Expression over reading |
| Accessibility | A separate closed-caption track with complete lyrics, standard styling | Expressive type is not an accessible caption |

**Verification:** the artist approves the expression; the caption file is checked independently; flash and pattern risk reviewed because the type flickers on beats (see [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md)).

**Contrast between the examples:** the corporate overlay subordinates type to information and the speaker; the music video makes type a performer. Both are correct within their contracts; swapping their approaches would fail both.

## 10. Counterexample and repair — the cramped lower third with glow

**Hypothetical counterexample.** A conference highlight video uses a template lower third: a narrow box tight to the text, thin light-weight type, an outer glow for contrast, the name and a long title on one line, appearing for 2 seconds as the speaker begins talking. Over a bright stage background, the glow turns into a grey smear; the long title is set small to fit; in the Hindi version, the box clips the matras. Viewers in a feedback round cannot recall any speaker's name.

**Diagnosis:**

| Problem | Cause |
|---|---|
| Unreadable | Thin weight; glow loses contrast on bright backgrounds |
| Cramped | Box padding smaller than the text's own internal spacing; matras clipped |
| Attention competition | Appears on the speaker's first words |
| Disappears before understood | 2-second hold for about 12 words |

**Repair:**
1. Split into two lines: name (large, semibold) and a shortened title.
2. Replace glow with a solid or semi-opaque band, or a soft, wide drop shadow tested over the brightest frames.
3. Increase padding to at least the cap height; set Devanagari leading for marks.
4. Enter after the speaker's first phrase; hold 4–5 seconds (tested by reading aloud twice).
5. Remove the per-letter entrance animation; use a fade.

**Verification:** test over the brightest and darkest frames in each clip; test Hindi with names containing conjuncts and above-headline marks; recall check with fresh viewers.

## 11. Micro-decisions

- Set optical (visual) alignment for punctuation and round letters at line starts if the tool supports it; hanging punctuation looks more aligned.
- Kern display-size titles manually where pairs look uneven.
- Avoid pure black and pure white for text over footage; slightly off values usually sit better in the image.
- Check text after the final grade — a grade change can reduce contrast behind graphics.
- Use the same type roles for the same functions throughout; a viewer learns them.
- When text sits over moving footage, prefer positions where the footage is consistently calm.

## 12. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Unreadable on phones | Sized on a monitor | Test on device; adjust size/weight |
| Unreadable on bright frames | Contrast approach relies on average background | Worst-case testing; band or shadow |
| Hindi looks broken | Shaping not applied; grapheme clusters split; tracking added | Shaping-capable tool and font; remove tracking; cluster-aware animation |
| Matras clipped | Insufficient leading/padding | Adjust leading; box height by script |
| Text competes with faces | Placement or timing | Move; delay entry |
| Inconsistent names | No naming control | Single source of truth for names; QC |

## 13. Verification

Verify typography **at final size, at actual playback speed, over the brightest and darkest backgrounds it will cover, in every required language and aspect ratio, and on the final encoded file**. Compression softens thin strokes and can introduce ringing around high-contrast edges; check after encoding.

## Dependencies

- Depends on: [Design System](../MOTION-DESIGN/Design-System.md), [Color Management](../COLOR/Color-Management.md) for consistent colour values.
- Companion: [Captions and Accessibility](Captions-and-Accessibility.md), [Localization](Localization.md).
- Feeds: [Platform and Format Strategy](../DELIVERY/Platform-and-Format-Strategy.md), [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

Function-based separation, worst-case contrast testing, concise wording over shrinking and Devanagari shaping/no-tracking rules are `[Practice]`. Associations between typefaces and emotional register are `[Heuristic]` and culturally variable. Sizes and proportions are `[Illustrative]` starting points that must be tested on target devices. Platform overlay positions change and are not specified here.
