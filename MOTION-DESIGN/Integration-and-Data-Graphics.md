# Integration with Live Action and Honest Data Graphics

**Purpose:** Teach how graphics relate to live-action images — from deliberately flat overlays to objects that must appear physically present — and how to visualise data and processes faithfully, including when not to animate at all.

**Applies to:** Labels on objects, tracked graphics, screen inserts, charts, process diagrams, maps and any graphic sharing a frame with footage.

**Prerequisites:** [Design System](Design-System.md), [Animation Grammar](Animation-Grammar.md).

**Related owners:** Photoreal compositing (keying, roto, tracking, screen replacement) is owned by [Compositing and Integration](../VFX/Compositing-and-Integration.md). Colour consistency of graphics against graded footage depends on [Color Management](../COLOR/Color-Management.md).

---

## 1. Two legitimate relationships: overlay and presence

Not every graphic should look real. The first decision is which relationship the graphic has with the image.

| Relationship | Description | Signals to the viewer | Examples |
|---|---|---|---|
| Overlay (flat) | The graphic sits on the screen surface, clearly separate from the photographed world | "This is information added by the film-maker" | Lower thirds, captions, chapter titles, most charts |
| Anchored overlay | Flat in style, but positioned or tracked to something in the image | "This label refers to that object" | A label tracked to the filter's candle; a callout pointing at a product feature |
| Present object | The graphic appears to exist in the scene — lit, occluded, perspective-correct | "This is in the world" | A holographic UI in a sci-fi brand film; text painted on a wall; a 3D product insert |

**Choosing:** use overlay when the graphic is the narrator's voice; anchored overlay when it explains a specific thing in shot; present object when the fiction or brand world requires it. A frequent failure is a graphic stuck halfway: positioned as if present (tracked into perspective) but lit and blurred as an overlay, so it floats unconvincingly.

## 2. Cues that make a graphic feel present

When presence is intended, the graphic must share the image's physical cues. Each missing cue is a "tell".

| Cue | What to match | Typical tell when missing |
|---|---|---|
| Perspective | Vanishing points and lens field of view | Text looks pasted flat against an angled surface |
| Anchoring and tracking | Stable attachment to a surface through camera and object motion | Floating, sliding or jittering relative to the surface |
| Occlusion | Foreground objects pass in front of the graphic | A hand passes "behind" a label that should be on the table |
| Lighting relationship | Brightness, colour and direction of light falling on the graphic | Graphic glows uniformly in a dim, warm scene |
| Shadow and contact | Shadows cast by or onto the graphic; contact with surfaces | Object hovers without shadow |
| Edge treatment | Edge softness matching lens and focus | Razor-sharp edges in a soft image |
| Depth of field | Blur matching the plane of focus | Sharp graphic on an out-of-focus wall |
| Motion blur | Blur matching shutter and motion | Crisp graphic during a fast camera move |
| Grain and noise | Matching noise texture | Clean graphic over noisy footage — a "sticker" look |
| Optical softness and lens character | Chromatic fringing, halation, distortion | Graphic too perfect for the lens |
| Colour pipeline | Same working space and output transform as footage | Brand colours shift; graphic looks oversaturated (see [Color Management](../COLOR/Color-Management.md)) |

For anchored overlays, a subset applies: **tracking stability, motion blur during moves, and colour pipeline** are usually needed even when the style is flat; perspective, lighting and grain usually are not.

## 3. Data visualisation: faithful values, honest motion

Charts in video carry the authority of evidence. Animation adds persuasive power — and new ways to mislead.

### 3.1 Static honesty

| Principle | Practice | Common distortion |
|---|---|---|
| Faithful values | Values match the source exactly; rounding stated | Rounded or "illustrative" values presented as data |
| Clear scales | Axes labelled; bar charts start at zero unless clearly marked otherwise | Truncated axes that exaggerate differences |
| Units | Every number has its unit and, where relevant, the time period and population | "50%" of what? |
| Readable labels | Labels large enough at the smallest viewing size; directly on data where possible rather than in a legend | Tiny legends; colour-coded legends that cannot be read on phones |
| Appropriate chart type | Bars for comparison, lines for change over time, parts-of-whole only when parts sum to a meaningful whole | 3D pies; area/volume scaling that exaggerates |
| Source | Shown on screen or in description, as the brief requires | Unsourced numbers |
| Uncertainty | Ranges or caveats shown when they matter | False precision |
| Colour | Not the only carrier of meaning; consider colour-vision deficiency | Red/green-only distinctions |

### 3.2 Honest animation

| Animation choice | Honest use | Misleading use |
|---|---|---|
| Bars growing from zero | Shows magnitude | Overshoot past the true value (even briefly) |
| Line drawing over time | Shows change over time at a constant time rate | Easing that makes recent change appear faster |
| Transitions between charts | Help track the same item across views | Morphing between unrelated measures implies they are comparable |
| Sequential reveal | Guides attention in reading order | Revealing a cherry-picked subset as if it were the whole |
| Causal arrows or flows | Show a documented mechanism | Implying causality where only correlation is known |
| Counters ("ticking up") | Celebrate a real total | Implying precision or speed of change that does not exist |

### 3.3 Number timing

A number on screen must remain long enough to be read *and understood* — including its unit and comparison. Viewers typically need more time for numbers than for words of similar length, especially unfamiliar or multi-digit values `[Heuristic]`. Test by reading aloud twice with the unit.

## 4. Worked example 1 — A complex process visualisation (hypothetical, Project C "Clear Water")

**Content:** how the gravity filter works, then the four cleaning steps.

**Approach:** footage-first for the real filter, shape-first for the cross-section, with a deliberate visual bridge.

| Decision | Choice | Rationale |
|---|---|---|
| Relationship to footage | Begin on the real filter (live action); dissolve to a cross-section drawn in the same proportions and colours as the real object, aligned to its silhouette | Viewers connect diagram to object; trust established by the real thing first |
| Style | Flat, clean illustration; no photoreal rendering | Diagram should read as explanation, not as "this is what it looks like inside" (which might mislead about scale of particles) |
| Scale honesty | Particles shown enlarged with an on-screen note "not to scale" | Bacteria are invisible; enlargement must be acknowledged |
| What moves | Water level (linear), particles (to the candle surface), clean drops (linear loop) | Only what carries the mechanism; see [Animation Grammar](Animation-Grammar.md#9-worked-example-2--a-process-step-hypothetical-project-c-clear-water-2997-fps) |
| What stays still | The filter body, labels, the virtual camera | Anchors for comparison |
| Labels | Anchored overlays pointing to parts; Hindi and English versions designed for text expansion | See [Localization](../TEXT-ACCESSIBILITY/Localization.md) |
| Limits | A final frame states what the filter does not remove (as approved by the advisor) | Avoids implying complete safety |
| Return to footage | Cut back to the real hands performing step 1 | Diagram explains; demonstration proves |

**Timing test:** the sequence is built first as an animatic timed to the scratch narration in both languages. The Hindi narration runs about 15% longer in the mechanism section (hypothetical); the animatic reveals that a label disappears before the Hindi line naming it ends. The label hold is lengthened in the Hindi version rather than shortening the narration.

**Verification:** advisor reviews accuracy; fresh viewers (one per language) explain the mechanism; check labels on a low-cost phone at arm's length.

## 5. Worked example 2 — A chart with a revised claim (hypothetical, Project C)

**Source (hypothetical, from the advisor):** lab test of bacterial counts in water from three conditions: unfiltered, filter with uncleaned candle (8 weeks), filter with candle cleaned weekly. Values reported as colony counts per 100 mL, with ranges.

**First draft (rejected):** a bar chart with an animated counter showing "99% REMOVED" over the cleaned-filter bar, bars bouncing into place, y-axis unlabelled.

**Problems:** the 99% figure was derived by the motion designer from the midpoint values, not stated by the source; the bounce overshoots values; the axis lacks units; the ranges are omitted.

**Revision:**
- Bars grow from zero with ease-out, no overshoot, to the reported median values.
- Y-axis labelled with units; range shown as a thin line on each bar.
- Annotation: "Much lower when cleaned weekly" — wording approved by the advisor in place of a percentage.
- Source line at the bottom: "Lab test, [organisation], [year] — illustrative values for this teaching example."
- Hold the settled chart for at least the full narration sentence about it.

This revision is the dependency case in the [change-impact map](../FOUNDATIONS/Constraints-and-Priorities.md#change-impact-map--filled-example-hypothetical-project-c-clear-water).

## 6. Counterexample and repair — the pasted-on graphic

**Hypothetical counterexample (Project B, early version of the 90-second brand film).** A tracked label "Brushed 18/8 steel" is attached to Arc in a slow handheld orbit shot in the workshop. Reviewers say it "looks cheap" and "floats".

**Diagnosis (cue by cue):**

| Cue | Observation (hypothetical) | Contribution |
|---|---|---|
| Tracking | Slight sliding during the fastest part of the orbit | Floating |
| Motion blur | None on the label; the footage has visible blur during the move | Sticker look |
| Edge | Razor-sharp edges; footage is soft at the frame edges due to the lens | Too clean |
| Grain | Label noise-free; footage has fine sensor noise | Sits "on top" |
| Colour | Pure white text; the scene is warm, white balance around tungsten-motivated practicals | Looks like another light source |
| Relationship ambiguity | Perspective-tracked (as if on the bottle) but styled flat | Neither present nor overlay |

**Repair options:**

| Option | Approach | Effort |
|---|---|---|
| A. Commit to anchored overlay | Track a small leader line to the bottle; keep the text flat in screen space (not perspective-warped), add matching motion blur to the leader, warm the text slightly toward the scene's white point, add matching grain | Low |
| B. Commit to presence | Render the text as if engraved on the bottle surface, with reflections and occlusion | High; may look like an actual engraving, which Arc does not have — misleading |
| C. No graphic in this shot | Move the material claim to the end card or the founder's line "we chose steel that…" | Lowest; the claim is carried by voice |

**Choice:** **C** for the brand film (the founder already speaks about the material; a label adds an advertising register the film avoids), **A** for the 30-second spot's macro shot, where muted viewers need the claim.

**Verification:** watch the shot at full speed on a large display and a phone; ask "does the label belong to the bottle?" For A, frame-step the fastest part of the orbit to confirm no slip greater than a pixel or two at delivery resolution.

## 7. When no motion communicates better

Motion attracts attention, takes time and adds interpretation. A still graphic is often better when:

- The viewer must **compare** values (motion makes comparison harder until it stops).
- The content is **serious** and motion would trivialise it.
- The information is **dense** and needs scanning time.
- The audience includes viewers for whom motion is distracting or uncomfortable.

A practical test: build the still version first. Animate only if animation adds understanding (showing change, sequence or mechanism), not merely entrance.

## 8. Micro-decisions

- Sample the scene's white point for "white" text in integrated graphics; pure display white often looks like a light source.
- Add grain to graphics *after* any blur, at the same scale as the footage grain, and check after delivery compression — fine grain may be removed by encoding.
- For anchored labels, prefer a leader line plus flat text over perspective-warped text; it reads better and tracks more forgivingly.
- In charts, put labels on the data; legends cost eye movement.
- Use one decimal place consistently or none; mixed precision suggests mixed sources.
- Never ease or overshoot the value of a data element; ease only its entrance opacity or position of non-data elements.

## 9. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "Graphic floats" | Tracking slip; missing motion blur; ambiguous relationship | Fix track; add blur; choose overlay or presence clearly |
| "Looks cheap" | Mismatched colour, edges, grain | Match pipeline, softness, noise |
| "Chart is confusing" | Too many series; legend-dependent; motion during reading | Simplify; direct labels; settle before reading |
| "The number seems wrong" | Derived or rounded values not from source | Use source values; get approval |
| "It implies causation" | Arrows or morphs between unrelated data | Remove causal grammar; add caveats |
| "I couldn't read the labels on my phone" | Sizes tested only on a monitor | Test on target device; enlarge or reduce text |

## 10. Verification

- For integrated graphics: full-speed playback, then frame inspection of the fastest motion; check on the final encoded file.
- For data graphics: compare every value, unit and label against the source document; an independent reviewer checks.
- Ask a fresh viewer to state the chart's main point; it should match the source's supported conclusion.
- Check colour-vision accessibility (e.g., by viewing a desaturated version).

## Dependencies

- Depends on: [Design System](Design-System.md), [Animation Grammar](Animation-Grammar.md), [Color Management](../COLOR/Color-Management.md).
- Companion: [Compositing and Integration](../VFX/Compositing-and-Integration.md) for photoreal integration and screen replacement.
- Feeds: [Typography System](../TEXT-ACCESSIBILITY/Typography-System.md), [Localization](../TEXT-ACCESSIBILITY/Localization.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

Integration cues and data-honesty principles (zero baselines for bars, units, sources, no implied causality) are `[Practice]` in information design and compositing. The overlay/anchored/present framework is this library's teaching structure. Number-reading time observations are `[Heuristic]`. All values and project details are `[Illustrative]`; the lab data in the Clear Water example is hypothetical.
