# Platforms, Genres, Aspect Ratios and Formats

**Purpose:** Teach how genre and delivery context shape a piece without assuming each platform has one aesthetic; how to plan aspect-ratio versions through recomposition rather than blind cropping; and how safe areas, interfaces, autoplay, captions, covers, calls to action and duration constraints affect decisions — while verifying current platform specifications rather than inventing them.

**Applies to:** Any piece with more than one destination or format.

**Prerequisites:** [Creative Brief](../FOUNDATIONS/Creative-Brief.md), [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md), [Composition and Optics](../CAMERA/Composition-and-Optics.md).

**Related owners:** Version tracking and localization workflow in [Versioning and Localization](Versioning-and-Localization.md); destination technical specifications and export in [Quality Control and Export](Quality-Control-and-Export.md); loudness in [Audio Delivery](Audio-Delivery.md).

---

## 1. Genres and contexts

The same audience member watches a festival documentary, a phone feed and a training module with different expectations. The table describes common contracts and contexts — tendencies, not rules; every platform hosts many aesthetics.

| Form | Audience contract | Information density | Emotional grammar | Accessibility emphasis | Typical delivery contexts |
|---|---|---|---|---|---|
| Narrative film | Immersion in a fictional world | Variable; subtext-heavy | Performance, silence, score | Subtitles, SDH, audio description | Festivals, streaming, cinema |
| Documentary | Truthful representation | Variable; duration as meaning | Observation, testimony | Subtitles, SDH, transcripts | Festivals, broadcast, streaming, web, screenings |
| Commercial (advertisement) | Persuasion within truthfulness | High; compressed | Desire, wit, warmth | Captions (often muted viewing) | Feeds, pre-roll, TV, cinema |
| Product film | Demonstration of value | High in proof; clear | Admiration, clarity | Captions; text for muted viewing | Product pages, retail, events |
| Corporate / internal | Information and alignment | Moderate | Credibility, warmth | Captions; plain language | Intranets, meetings, LMS |
| Education / explainer | Accurate learning | Paced to comprehension | Curiosity, competence | Captions, transcripts, audio description | Learning platforms, public channels, classrooms |
| Talking-head / presenter | A person speaking to you | Moderate–high | Personality, trust | Captions | Web, social |
| Podcast with video | Conversation | Low visual, high verbal | Intimacy, discussion | Captions, transcripts | Video platforms, podcast apps |
| Music video | Expression of a song | Rhythmic, visual | Mood, style, identity | Lyrics captions where appropriate | Video platforms, TV, social |
| Long-form online video | Sustained engagement with a creator or topic | Variable | Personality, story | Captions, chapters | Video platforms |
| Short-form social | Fast, scrolling, often muted first | High per second; immediate | Surprise, humour, relatability, utility | Open captions; readable text | Vertical feeds |

**No platform has one aesthetic.** A vertical feed carries comedy, news, tutorials, art and advertising. What the platform shapes is the **context**: sound-off starts, scrolling attention, interface overlays, small screens, loop behaviour. Design for the context and the contract together.

## 2. Aspect ratios and versioning strategies

| Ratio | Common contexts |
|---|---|
| 16:9 | Web players, TV, most professional masters |
| 9:16 | Vertical phone feeds and stories |
| 1:1 | Some feeds; multi-platform posts |
| 4:5 | Some feed placements (taller than square) |
| 2.39:1 (within 16:9 or as DCP) | Cinematic framing for festivals/cinema |

Exact accepted dimensions, lengths and placements change — **verify the current destination specification** before export (see [Quality Control and Export](Quality-Control-and-Export.md)).

### Six strategies for alternate aspect ratios

| Strategy | What it is | Best when | Risk |
|---|---|---|---|
| Crop | Extract a region of the master | Subject central and alone; resolution headroom | Removes story information, graphic context, eye direction, product evidence |
| Reframe (keyframed crop) | Moving crop following the action | Action moves within the frame | Artificial camera movement; misses simultaneous information |
| Alternate takes | Use takes shot for the other ratio | Planned at acquisition | Requires foresight |
| Recomposition | Rebuild the shot from layers (separate subject, background, graphics) | Graphics-heavy pieces; composited shots | Effort; not possible for most live action |
| Layout redesign | Graphics and text redesigned for the new frame | Any text/graphics | Design time |
| Alternate edit | A different cut — different shots, order, duration | Strong vertical versions; different platform context | Time; approvals |

**Do not assume one master can simply be resized into all versions.** A good vertical version is often an alternate edit using alternate framings and redesigned graphics, not a crop.

### What a centre crop removes

| Lost element | Example |
|---|---|
| Story information | Two people in a 16:9 two-shot; vertical crop shows only one |
| Graphic context | A chart's axis labels cut off |
| Eye direction | A character looking off-screen to the side now looks at the frame edge (see [Continuity and Attention](../EDITING/Continuity-and-Attention.md#10-crop-and-reframe-meaning-changes-with-the-frame)) |
| Product evidence | The hand and the product's feature on opposite sides of the frame |
| Text | Signs, captions, lower thirds |

## 3. Context factors to design for

| Factor | Consideration | Verify |
|---|---|---|
| Safe areas | Areas likely to be cropped or obscured on some displays and players | Destination spec |
| Interface overlays | Buttons, captions, usernames, descriptions, progress bars covering parts of the frame — often the bottom and right side in vertical feeds | Current layout of each app (changes with updates) |
| First-frame context | Many viewers decide in the first moments; the first frame may also serve as a preview image | — |
| Silent autoplay | Many feeds start muted; meaning must survive without sound | Brief's viewing assumptions |
| Captions | Open captions on social; closed captions where supported; placement per version | Platform caption support |
| Thumbnails / covers | Often chosen separately; must represent content honestly | Platform requirements |
| Calls to action | On-screen text, end cards, platform buttons; avoid duplicating platform UI | Platform ad rules |
| Duration constraints | Maximum lengths and recommended lengths vary by placement | Current spec |
| Loop behaviour | Short videos may loop; the end flows into the start | — |

## 4. Worked example 1 — Brand film to short vertical (hypothetical, Project B "Arc")

**Source:** the 90-second 16:9 founder-led brand film. **Target:** a 15-second 9:16 vertical for feeds, muted first, with open captions.

**First attempt (failed crop):** the editor centre-crops a 15-second section of the brand film: Dev's workshop line "I wanted something that noticed for you," followed by the ring reveal.

| Problem in the crop | Cause |
|---|---|
| Dev's look toward the interviewer points at the frame edge; Dev seems to look away from the viewer's world | 16:9 framing with look room on one side |
| The workshop's prototypes (context) are cut off | Horizontal composition |
| The ring reveal's macro is fine, but the hand holding the bottle is cut | Hand on the left, ring on the right |
| Captions sit at the bottom, under the platform's interface area | Placement copied from 16:9 |
| The line needs sound; muted viewers see a talking head with captions only | Sound-first edit |
| The 16:9 lower third is cut in half | Graphics not redesigned |

**Repair through alternate composition and editing:**

| Change | Approach |
|---|---|
| Structure | New 15-second edit: opens on the hand hesitating over the bottle (visual hook, works muted); then Dev's line as a short caption-supported moment; then the ring reveal; then the end card |
| Dev's shot | Use the B-cam angle, which was framed with vertical extraction in mind (see [Composition and Optics](../CAMERA/Composition-and-Optics.md#6-multi-format-acquisition-horizontal-and-vertical)); offset crop keeps look room |
| Product | Use the dedicated vertical framing of the reveal shot from the shoot |
| Captions | Upper-middle zone, verified against the current interface layout |
| Graphics | Redesigned vertical end card per the design system's variant rules |
| Sound | Designed to work muted first; sound-on adds the product tone and music |

**Verification:** watch the encoded vertical on two phone models in the actual app's preview (or the platform's ad preview tool), muted and unmuted; check every frame for interface collisions; fresh viewers state the benefit.

## 5. Worked example 2 — Documentary across web, social and projection (hypothetical, Project A)

| Destination | Context | Decisions |
|---|---|---|
| Online series page (16:9) | Laptop and phone; viewers chose to watch; sound usually on | Full 6-minute film; closed captions (Hindi) and subtitles (English) as separate tracks |
| Social excerpt (9:16, 60 s) | Feed; muted start; scrolling | Alternate edit around the "I stopped noticing" passage; open captions; offset vertical crop (see [Continuity and Attention](../EDITING/Continuity-and-Attention.md#11-worked-example--interview-with-missing-coverage-and-later-vertical-extraction-hypothetical-project-a)); end card with link |
| Community screening (projection) | Large image; room acoustics; mixed literacy | Burned-in English subtitles for a mixed audience; Hindi audio; projection copy checked on the actual projector; loudness suitable for small PA (see [Audio Delivery](Audio-Delivery.md)) |

## 6. Counterexample and repair — one export for everything

**Hypothetical counterexample.** A team exports a single 16:9 master and uploads it unchanged to every destination: a vertical feed (where it appears small with large bars), a square placement (cropped automatically by the platform, cutting off captions), and a pre-roll slot (where the first three seconds are a slow fade from black — skippable before anything is seen). Performance is poor and the client asks why.

**Diagnosis:** no format strategy; context ignored (first frames, interfaces, cropping).

**Repair:**
1. Build a version matrix (see [Versioning and Localization](Versioning-and-Localization.md)).
2. Create vertical and square versions by alternate edit and recomposition.
3. For pre-roll, open on a clear image and the brand within the first moments; no fade from black.
4. Check each platform's current specifications and previews.

**Verification:** each version reviewed on its destination preview; collisions and crops checked.

## 7. Micro-decisions

- Decide the primary destination; design for it first, then adapt.
- Keep graphics and text on separate layers for recomposition.
- Plan vertical framings during the shoot for key shots (see [Composition and Optics](../CAMERA/Composition-and-Optics.md)).
- Check the first and last frames of every version: first for hook and context, last for loop and end card.
- Avoid placing essential information in areas covered by interfaces; check with the current app.
- Choose cover/thumbnail frames honestly (no misleading images).

## 8. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Vertical version loses meaning | Centre crop of a horizontal composition | Alternate edit and framings |
| Captions hidden by interface | Placement copied across formats | Per-version placement; preview checks |
| Low early engagement on pre-roll | Slow opening | Clear first frames |
| Platform rejects upload | Spec mismatch | Verify current specs |
| Text unreadable on phones | Sized for monitors | Test on devices |

## 9. Verification

- Each version verified independently on representative devices and on encoded outputs.
- Caption and graphic collisions checked against current interface layouts.
- Audio and CTA changes checked per version.
- Current destination specifications confirmed and recorded (see [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md) for what this library has and has not verified).

## Dependencies

- Depends on: [Creative Brief](../FOUNDATIONS/Creative-Brief.md), [Genre and Viewer Contract](../STORY/Genre-and-Viewer-Contract.md), [Composition and Optics](../CAMERA/Composition-and-Optics.md), [Design System](../MOTION-DESIGN/Design-System.md).
- Companion: [Versioning and Localization](Versioning-and-Localization.md).
- Feeds: [Quality Control and Export](Quality-Control-and-Export.md), [Captions and Accessibility](../TEXT-ACCESSIBILITY/Captions-and-Accessibility.md).

## Confidence summary

Context-led design, the six versioning strategies and the risks of centre cropping are `[Practice]`. Genre/context tendencies are `[Heuristic]`. Platform specifications (dimensions, durations, safe zones, interface layouts) are deliberately **not** stated: they change and must be verified per destination at delivery time. Examples are `[Illustrative]`.
