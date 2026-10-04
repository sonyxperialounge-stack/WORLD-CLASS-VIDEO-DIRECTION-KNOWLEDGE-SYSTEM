# Animation Grammar: Timing, Spacing and Easing

**Purpose:** Teach how timing, spacing, acceleration, holds, overlap, anticipation, overshoot and settle communicate mass, responsiveness and character; how to read position and velocity curves; when linear motion is right; and how to respect motion sensitivity.

**Applies to:** Graphics, titles, data animations, UI animations, logo animations and virtual camera moves.

**Prerequisites:** [Design System](Design-System.md) (what moves and why), [Decision Method](../FOUNDATIONS/Decision-Method.md) (frame/ms conversions).

**Related owners:** Live-action integration and data honesty in [Integration and Data Graphics](Integration-and-Data-Graphics.md); virtual camera moves in [Retiming and Virtual Motion](../CAMERA/Retiming-and-Virtual-Motion.md); flash and pattern safety as a QC gate in [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

---

## 1. Timing and spacing

Two separate quantities determine how motion feels:

- **Timing:** when a movement starts and how long it lasts, measured in frames (and therefore milliseconds at a stated frame rate).
- **Spacing:** how far the object travels between consecutive frames. Large spacing = fast; small spacing = slow. Changing spacing over the movement creates acceleration or deceleration.

Two animations with identical timing (both 12 frames) feel completely different with different spacing: even spacing (constant speed) feels mechanical; spacing that starts wide and narrows (fast start, slow end) feels like an object arriving and settling.

### Illustrative conversions (see [Decision Method](../FOUNDATIONS/Decision-Method.md#6-units-frames-and-time))

| Frames | 23.976 fps | 25 fps | 29.97 fps |
|---|---|---|---|
| 6 | ≈ 250 ms | 240 ms | ≈ 200 ms |
| 12 | ≈ 500 ms | 480 ms | ≈ 400 ms |
| 18 | ≈ 751 ms | 720 ms | ≈ 601 ms |
| 24 | ≈ 1001 ms | 960 ms | ≈ 801 ms |

When a motion spec is shared between versions at different frame rates, express it in milliseconds (or seconds) and let each version round to frames — or the 29.97 fps version will be about 17% faster than the 25 fps version if "12 frames" is copied literally.

## 2. The vocabulary of motion

Many of these terms come from classical character animation, where they were developed to make drawn objects feel alive; their names were popularised by animators' writing on the craft. In motion design they are tools, not obligations.

| Term | Meaning | Communicates | Risk |
|---|---|---|---|
| Ease-in (acceleration) | Starts slowly, speeds up | Mass overcoming inertia; departure | Slow starts feel sluggish in UI-like motion |
| Ease-out (deceleration) | Starts fast, slows to a stop | Arrival; responsiveness; settling | Too long a tail feels floaty |
| Ease-in-out | Slow–fast–slow | Smooth, deliberate, "considered" | Applied to everything, it becomes a uniform house style that feels generic |
| Hold | No motion | Rest; reading time; emphasis | Too short holds deny reading; too long feel dead |
| Overlap / follow-through | Parts of an object move at slightly different times; trailing parts continue after the main body stops | Organic, physical, flexible | Overdone, it feels rubbery |
| Stagger | Related elements start one after another | Reading order; hierarchy | Long staggers delay information |
| Anticipation | A small opposite move before the main move | Preparation; intent; weight | Inappropriate in precise or serious contexts; delays information |
| Overshoot | Passing the target slightly before returning | Energy; elasticity; playfulness | Unserious; can feel cheap in luxury, financial or medical contexts |
| Settle | Small diminishing oscillation or slow final approach to rest | Physical realism; completion | Long settles distract from content |

## 3. Position curves and velocity curves

Animation software typically shows motion in two graph forms:

- **Value (position) graph:** position on the vertical axis, time on the horizontal. The slope is speed. A straight line = constant speed; an S-shape = ease-in-out; a curve that flattens at the end = ease-out.
- **Speed (velocity) graph:** speed on the vertical axis, time on the horizontal. A flat line = constant speed; a hill = accelerate then decelerate; a peak early with a long tail = fast start, gentle stop.

### Why both matter

The value graph shows *where* the object is; the velocity graph shows *how it feels*. Two curves that look similar on the value graph can have very different velocity peaks. Experts look at the velocity graph to judge:

- **Peak speed:** a very high peak makes motion snappy or violent.
- **Peak position:** an early peak (most movement happens at the start) feels responsive; a late peak feels like acceleration toward impact.
- **Tail length:** long tails feel luxurious or floaty; short tails feel crisp or abrupt.

### What curve shapes tend to communicate `[Heuristic]`

| Curve character | Communicates | Fits |
|---|---|---|
| Early velocity peak, short tail (strong ease-out) | Responsive, confident, efficient | UI, claims, lower thirds, product text |
| Symmetrical ease-in-out with long ends | Calm, deliberate, smooth | Luxury, reflective documentary titles |
| Late peak (strong ease-in) then hard stop | Impact, weight, force | Stamps, slams, dramatic reveals |
| Constant speed (linear) | Mechanical, continuous, predictable | Conveyor belts, clock hands, data sweeps, credit rolls, tracking |
| Overshoot and settle | Elastic, playful, energetic | Children's content, playful brands, celebratory moments |

## 4. Linear motion is sometimes right

A common teaching overstatement is "never use linear motion; always ease." Easing makes objects feel physical because physical objects have inertia. But not all motion should feel like a physical object starting and stopping. Linear (constant-speed) motion is appropriate when:

- **The thing represented moves at constant speed:** a conveyor, a clock hand, water flowing through a filter at a steady rate, a satellite orbit at diagram scale.
- **The motion is continuous or looping:** a background texture drifting, a ticker, a loading indicator, a seamless loop where easing would create a visible "pulse" at the loop point.
- **Data sweeps:** a line chart drawing over time, where time is the x-axis — easing would distort the implied rate of time.
- **Predictable tracking:** credits, scrolling text, a map pan the viewer must follow — constant speed makes it easier to read and track.
- **Deliberately mechanical imagery:** robotic, industrial or retro-computing aesthetics.
- **Entering or exiting during a camera move:** linear motion of a layer tracked to a constant-speed camera move must match the camera's speed.

Even then, the *start and end* of a linear motion may be eased gently if the object appears from or stops at rest within the frame; a linear motion that begins or ends offscreen needs no easing.

## 5. Overshoot and bounce: when they help and hurt

| Context | Overshoot/bounce | Why |
|---|---|---|
| Children's education, playful consumer brands, celebrations | Often helps | Energy, delight, physical play |
| UI micro-interactions | Small amounts help | Feedback that an action registered |
| Financial reporting, investment products | Usually hurts | Bounce implies instability or frivolity; numbers that wobble undermine precision |
| Medical and public-health explanation | Usually hurts | Seriousness, trust; bouncing organs or pills feel trivialising |
| Serious documentary | Usually hurts | Signals entertainment over gravity |
| Luxury | Usually hurts | Luxury motion tends toward restraint, long smooth decelerations, stillness |

A value that overshoots in a chart (a bar briefly exceeding its final value) also misrepresents data momentarily — avoid in data graphics regardless of tone (see [Integration and Data Graphics](Integration-and-Data-Graphics.md)).

## 6. Motion sensitivity and reduced motion

Some viewers experience discomfort, dizziness or nausea from certain motion: large-scale zooms, parallax with strong depth, fast spinning, full-screen sliding, and constant background motion. Others find continuous motion distracting, which affects comprehension, including for some neurodivergent viewers and people with attention-related conditions.

**Practice** `[Practice]`:
- Animate only what carries information; keep backgrounds still or nearly still under text.
- Avoid large full-frame motion as decoration.
- Prefer fades and small translations over zooms and spins for information graphics.
- For interactive or web contexts, respect reduced-motion preferences where the delivery platform supports them; for linear video, consider whether a calmer version is warranted for some audiences (e.g., health information).
- Treat flashing and rapid high-contrast alternation as a safety issue, checked at QC against current guidance (see [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md)).

## 7. Frame-rate and motion-blur considerations

- **Animating "on ones" vs "on twos":** a new pose every frame (on ones) is smooth; every second frame (on twos) gives a stepped, hand-made or stylised look. Mixing them accidentally produces stutter.
- **Judder on slow, high-contrast moves:** at 23.976 or 25 fps, slow horizontal movement of sharp, high-contrast text or lines can appear to stutter (judder) — particularly on large displays. Mitigations: slightly faster or slower speed, motion blur, softer edges, or avoiding the move.
- **Motion blur on graphics:** graphics composited over live action usually need motion blur that matches the footage's shutter (e.g., 180-degree equivalent: blur over half the frame interval) or they look pasted on (see [Integration and Data Graphics](Integration-and-Data-Graphics.md)). Flat, deliberately graphic styles may skip blur intentionally.
- **Frame-rate conversion:** animations rendered at one rate and converted to another may stutter; render at the delivery rate.

## 8. Worked example 1 — The Arc lid-ring and claim text (hypothetical, Project B, 23.976 fps)

**Brief stance:** calm confidence; precise, not gadget-like.

**Lid-ring UI glow (if animated as an overlay on the macro):** in this project the real product's glow is filmed; motion design only adds the matching app UI on the phone screen. The *app's* progress arc must match the real ring's behaviour (approved product behaviour supplied by the client): a fill over about 18 frames (≈ 750 ms) with a strong ease-out.

| Option | Velocity character | Feel | Verdict |
|---|---|---|---|
| Linear fill, 18 frames | Constant speed, abrupt stop | Mechanical, like a loading bar | Rejected — reads as "waiting", not "achieved" |
| Ease-in-out, 18 frames | Slow start, slow end | Smooth but slightly sluggish to start | Acceptable |
| Strong ease-out, 18 frames | Fast start, long gentle settle | Responsive and calm; the drink registers immediately, then settles | **Chosen** — matches "responsive companion" |
| Overshoot and settle | Fills past target, returns | Playful, gamified | Rejected — brand is not a fitness game; also misrepresents the progress value momentarily |

**Claim text entry:** fade plus 20-pixel upward translation `[Illustrative]` over 10 frames (≈ 417 ms) with ease-out; no blur needed because translation is small. The line holds for the remainder of the beat; exit is a fade only.

**Verification:** compare against the real product footage side by side — does the app animation feel like the same object? Watch muted on a phone; ensure the fill completes before the claim text appears (show, then tell).

## 9. Worked example 2 — A process step (hypothetical, Project C "Clear Water", 29.97 fps)

**Beat:** cross-section of the filter: water enters the upper chamber, passes through the ceramic candle, collects below; then the candle is shown being removed for cleaning.

| Element | Motion choice | Rationale |
|---|---|---|
| Water level falling in the upper chamber | Linear, slow | Represents a steady physical rate; easing would suggest the rate changes |
| Particles caught at the candle surface | Small particles drift in linearly and stop at the surface with a short ease-out | Shows trapping; the stop must be legible |
| Clean water droplets below | Linear fall (stylised) | Constant-rate flow; looping without visible pulses |
| Candle removal (part motion) | Ease-in-out over about 24 frames (≈ 800 ms) | A hand-operated action; deliberate, calm |
| Labels ("ceramic candle", "trapped particles") | Fade in, no translation; staggered 10 frames after the part they label settles | Labels should not move while being read; stagger follows the viewer's attention |
| Camera (virtual) | Static | Viewers must compare levels; a moving virtual camera would add confusion |

**Accessibility:** no information carried only by colour — trapped particles are shown by shape and position as well as colour; labels have sufficient contrast; motion is limited to what carries meaning.

**Verification:** the advisor checks that the depicted flow and trapping are not misleading (e.g., the animation does not suggest viruses are trapped); a fresh viewer explains the mechanism in their own words.

## 10. Counterexample and repair — bounce in a medical explainer

**Hypothetical counterexample.** A hospital's patient-information video about preparing for a blood test uses a motion template: icons of a syringe, a clock and a glass of water pop in with large overshoot and wobble; text bounces into place; transitions spin. Patients in a feedback session describe it as "childish" and two say it made them more anxious ("the syringe bouncing at me"). One staff member notes that the spinning transitions made them dizzy.

**Diagnosis.**
- Overshoot and bounce signalled playfulness inconsistent with the medical contract and with patient anxiety.
- Animating the syringe drew attention to the most anxiety-provoking object.
- Spinning transitions triggered motion discomfort.

**Repair.**
1. Replace overshoot with gentle ease-out fades and small translations.
2. Present the syringe icon static and small, beside the instruction text, rather than animated toward the viewer.
3. Replace spinning transitions with straight cuts or short fades.
4. Keep motion only where it explains (a clock icon's hand moving linearly to show fasting time).

**Verification:** a second feedback session with patients; ask how the video made them feel and whether anything was uncomfortable. Success: no reports of childishness or dizziness; correct recall of preparation steps.

## 11. Micro-decisions

- Express motion specs in milliseconds when they must be shared across frame rates.
- Check the first and last two frames of every animation by frame-stepping: "pops" (a sudden jump at start or end) usually come from a mismatched keyframe or interpolation setting.
- Ensure an element is fully settled (no sub-pixel drift) before text on it must be read — slow sub-pixel motion makes text shimmer.
- Stagger related items by a consistent offset; inconsistent offsets read as accidental.
- Match exit style to entry but make it quieter (shorter, less movement).
- When graphics move with a camera move, match the camera's velocity curve, not a generic ease.

## 12. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| "It feels floaty" | Long ease-out tails; slow settles | Shorten tails; move velocity peak earlier |
| "It feels robotic" | Linear motion where physical motion was intended | Add easing; overlap on parts |
| "It feels cheap/childish" | Overshoot/bounce in serious context | Remove overshoot; restrained easing |
| "Text shimmers" | Sub-pixel drift during reading; thin strokes on interlaced or scaled output | Settle fully before reading; adjust stroke weight |
| "It stutters" | On-ones/on-twos mix; judder on slow high-contrast pans; wrong render rate | Consistent stepping; motion blur; correct render rate |
| "It makes me dizzy" | Large-scale motion, spins, zooms | Reduce scale of motion; replace with fades |

## 13. Verification

- Watch at full speed on the target device; then inspect velocity graphs for consistency with intent.
- Frame-step entries and exits for pops.
- Check motion against the genre contract and brand stance.
- Review for motion-sensitivity risks and run the flash/pattern QC gate where relevant.
- For data animations, confirm no momentary misrepresentation (overshoot, misleading easing on values).

## Dependencies

- Depends on: [Design System](Design-System.md).
- Companion: [Integration and Data Graphics](Integration-and-Data-Graphics.md).
- Interacts with: [Retiming and Virtual Motion](../CAMERA/Retiming-and-Virtual-Motion.md), [Typography System](../TEXT-ACCESSIBILITY/Typography-System.md), [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md).

## Confidence summary

Timing/spacing, easing vocabulary and curve reading are `[Practice]` in animation and motion design. Associations between curve shapes and perceived character are `[Heuristic]`; they hold widely but depend on context and culture. The appropriateness of linear motion in the listed cases is `[Practice]`. Motion-sensitivity guidance is `[Practice]`; specific flash thresholds are treated as `[Requirement]` only where verified at QC. Frame counts and pixel distances are `[Illustrative]`.
