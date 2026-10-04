# Image Texture and Post Relighting

**Purpose:** Teach local exposure and colour shaping — windows, tracking, keys, subject isolation and plausible relighting — with honest limits; and the texture tools (denoise, sharpening, grain, halation, bloom, diffusion, vignetting, optical softness, motion blur) with their order-of-operations trade-offs and interaction with compression.

**Applies to:** Finishing and grading for any project.

**Prerequisites:** [Color Management](Color-Management.md), [Correction and Shot Matching](Correction-and-Shot-Matching.md), [Creative Grading](Creative-Grading.md).

---

## 1. Local shaping

| Tool | What it does | Typical use | Limit |
|---|---|---|---|
| Shape masks ("windows") | Adjust inside/outside a soft geometric shape | Brighten a face, darken a background, add a gradient to a sky | Edges visible if too hard or if the mask doesn't follow movement |
| Tracking | Moves a mask with the subject or camera | Keep a face lift on a moving face | Fails with occlusion, fast motion, motion blur |
| Keys / qualifiers | Select by hue, saturation, luminance | Isolate skin, sky, a product colour | Noisy or compressed footage produces ragged keys; similar colours elsewhere get selected |
| Subject isolation (segmentation masks, often machine-learning assisted) | Automatic separation of people or objects | Separate subject from background for relighting or depth effects | Hair, fine edges, transparent and fast-moving parts fail; temporal flicker |
| Relighting tools (directional brightness shaping, sometimes with estimated depth or normals) | Simulate light direction changes | Strengthen a motivated key; add gentle falloff | Cannot create true shadows or speculars where geometry/light wasn't recorded |

### Plausible relighting

"Relighting" in post means reshaping brightness and colour to suggest a light direction or quality. Plausible relighting:

- **Follows existing motivation** (enhances the window side rather than inventing a new source).
- **Respects existing shadows** (a face lit from the left cannot convincingly be relit from the right — its nose shadow still falls the other way).
- **Uses soft, broad changes** rather than hard, specific light shapes.
- **Tracks reliably** and does not breathe or flicker.

### Limits — what post cannot reconstruct

| Limitation | Why |
|---|---|
| Clipped data | No information exists in fully clipped regions |
| Noise | Brightening shadows amplifies noise; denoise smooths detail |
| Low bit depth and heavy compression | Pushing tones produces banding and blocking |
| Hair edges and fine detail | Masks struggle; halos appear |
| Moving reflections | Speculars on moving objects and eyes are hard to track and modify |
| Missing shadows | A shadow that should exist (from a new "light") cannot be created convincingly without geometry |
| Lighting geometry | The size, direction and shape of the original light define the image; post can only nudge |

**Post cannot reliably reconstruct lighting geometry or truthful detail that was never recorded.** This is why lighting decisions on set matter (see [Reading and Designing Light](../LIGHTING/Reading-and-Designing-Light.md)).

## 2. Texture tools

| Tool | Purpose | Typical artefact when overused |
|---|---|---|
| Denoise (spatial, temporal) | Reduce sensor noise and compression noise | Waxy, plastic faces; smeared detail; temporal "swimming" |
| Sharpening | Increase perceived edge contrast | Crunchy edges; halos; emphasised noise; harsh skin |
| Grain (synthetic) | Add organic texture; mask banding and compression; unify cameras; film-associated look | Too coarse for the output size; grain removed or turned to mush by encoding; grain on graphics where it doesn't belong |
| Halation | Red/orange glow around bright edges, associated with film's light scattering | Glowing outlines everywhere; reads as an effect |
| Bloom / glow | Soft spread of highlights | Obscures information; lowers contrast; dreamy when unintended |
| Diffusion (soft-focus simulation) | Softens contrast and detail, especially highlights | Muddy image; loss of story detail |
| Vignetting | Darkens frame edges to focus attention | Obvious dark corners; shifts with reframing; conflicts with captions at the bottom |
| Optical softness / lens emulation | Mimics lens characteristics (edge softness, chromatic aberration, distortion) | Looks applied; inconsistent with actual lens |
| Motion blur (synthetic) | Adds blur to fast motion or graphics | Smears; artefacts at edges |

### Film-associated cues versus photochemical equivalence

Grain, halation, gate weave, specific highlight roll-offs and colour responses are cues many viewers associate with film. Digital tools can simulate these cues convincingly. That is not the same as photochemical equivalence: a simulated look is a design choice that evokes film, not proof of film origin. Avoid claims like "authentic film look" in factual contexts where the origin of footage matters.

## 3. Order of operations

Texture operations interact; their order changes results. A reasoned default `[Heuristic]`:

1. **Denoise early** (on the source, in a suitable space), before strong contrast increases amplify noise and before sharpening.
2. **Primary and secondary grading** (correction and look).
3. **Local relighting.**
4. **Optical effects** (halation, bloom, diffusion) on the graded image, because they depend on final highlight brightness.
5. **Grain late**, so it sits on top of the image like a medium, and is not denoised or sharpened.
6. **Sharpening** carefully and usually minimally, after resizing to output resolution if possible (sharpening before downscaling behaves differently).
7. **Output transform** — though some tools apply grain and optical effects in display space after it; consistency matters more than the exact position.

**Why uniform recipes fail:** cameras differ in noise structure and sharpness; shots differ in exposure; the same denoise strength that cleans a well-exposed day interior destroys detail in a night shot, while being insufficient for an underexposed phone clip. Set texture per camera and per scene, then check sequences for consistency.

## 4. Compression and resizing interaction

Final delivery formats compress heavily. Consequences:

- **Fine grain may be removed** by encoders (they treat it as noise) or turned into blocky, swimming patterns. Grain size and strength should be checked on the final encoded file at the delivery resolution.
- **Sharpening halos are emphasised** by compression.
- **Gradients (skies, vignettes, dark backgrounds) band** in 8-bit delivery; a little grain or dithering can mask banding, if it survives encoding.
- **Resizing** (e.g., UHD source to HD delivery, or 16:9 crop to 9:16) changes apparent sharpness and grain size; texture decisions must be checked after the final resize.

## 5. Matching texture versus deliberate contrast

| Goal | Approach | Example |
|---|---|---|
| Match cameras | Denoise the noisier source, soften the sharper source, add a common grain | Project A's phone B-cam matched to the mirrorless A-cam |
| Deliberate textural contrast | Give different worlds different textures | Archival photos keep their scan grain; present-day footage is cleaner; a memory sequence is softer |
| Unified "world" texture | Same grain and softness across all material, including graphics where appropriate | A brand film with a consistent filmic texture |

## 6. Detecting texture problems

| Problem | What to look for | Correction |
|---|---|---|
| Waxy faces | Skin without pores or fine texture; plastic look | Reduce denoise/skin smoothing; add fine grain |
| Crunchy edges | Bright halos along edges; brittle hair | Reduce sharpening; sharpen after resize |
| Oversaturated shadows | Coloured noise in dark areas | Reduce shadow saturation; chroma denoise |
| Unstable masks | Edges that crawl, breathe or lag | Improve track; softer edges; smaller adjustments |
| Crushed story detail | Important objects lost in shadow | Lift selectively; adjust contrast |
| Grain too fine or coarse for output | Grain invisible after encoding, or blotchy | Adjust size/strength; test on encoded file |
| Bloom obscuring information | Text, product details or faces lost in glow | Reduce or mask bloom |

## 7. Worked example 1 — Texture matching a phone to a mirrorless camera (hypothetical, Project A)

**Observed (hypothetical):** the phone B-cam has smoothed skin (in-phone noise reduction), sharpening halos on edges, compression blocking in dark corners; the A-cam has fine luminance noise and natural skin texture.

**Steps:**
1. On the phone footage: gentle softening to reduce halos; no further denoise (it's already over-processed); a small chroma denoise in dark areas to reduce colour blotches.
2. On the A-cam: light temporal denoise only on night scenes, keeping skin texture.
3. Across both: a fine, low-strength grain, sized to be visible on a 1920×1080 encoded file but not distracting; it unifies texture and masks the phone's compression blocking.
4. Test: encode a 20-second A/B section at the delivery settings and check on a phone and a large display.

**Verification:** fresh viewers do not notice a camera change at A/B cuts; skin looks natural on both.

## 8. Worked example 2 — Strengthening motivated light (hypothetical, Project D)

**Situation:** in Nisha's single (take 5, chosen for performance), the hidden supplementary source was slightly too far forward, so her face is evenly lit and the table lamp's direction reads weakly.

**Approach:**
1. A soft, tracked shape over the lamp side of her face, brightening slightly (a fraction of a stop) and warming toward the lamp's colour.
2. A second soft shape darkening the far side slightly, increasing modelling.
3. No attempt to create a new shadow; the existing faint nose shadow already falls correctly for the lamp's side.
4. Track checked through her head movements; edges kept very soft so no mask boundary is visible.

**Limit acknowledged:** when she turns away from the lamp, the shapes would contradict the real light; the adjustment is keyframed off for that section.

**Verification:** full-speed playback; frame-step through head turns for mask "breathing"; compare with the master shot's lamp direction.

## 9. Counterexample and repair — the beauty pass that removed a person

**Hypothetical counterexample.** For the Arc brand film, a finishing artist applies strong skin smoothing to Dev's interview "to look premium". Dev's face becomes waxy; pores, fine lines and stubble disappear; under motion the smoothing flickers as the face turns. Dev's colleagues say it "doesn't look like them"; viewers sense something synthetic, undermining the authenticity of the founder story.

**Diagnosis:** beauty smoothing beyond plausibility; temporal instability; contradiction with the film's authenticity.

**Repair:**
1. Remove the global smoothing.
2. If any retouching is needed (a temporary blemish, with Dev's agreement), use small, local, tracked fixes that preserve texture.
3. Add matching fine grain so skin and background share texture.

**Verification:** Dev approves; a fresh viewer comparing before and after prefers the natural version for trustworthiness.

## 10. Micro-decisions

- Check texture at 100% and at the smallest viewing size.
- Apply grain to the image, not to graphics overlays, unless the design calls for unified texture.
- Keep vignettes subtle and check them with captions and lower thirds.
- Denoise per camera and exposure; save settings as per-camera presets, then adjust per shot.
- Use temporal denoise cautiously on fast motion (smearing).
- After any reframe for vertical, re-check vignettes and local masks.

## 11. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Plastic skin | Over-denoise or smoothing | Reduce; add grain |
| Halos | Over-sharpening; sharpening before resize | Reduce; sharpen at output |
| Visible mask edges | Hard edges; poor tracking | Soften; re-track; smaller changes |
| Banding in skies | 8-bit delivery; heavy grade | Dither/grain; gentler grade |
| Texture vanishes after upload | Encoder removed grain | Adjust grain; test with destination encoder |
| Bloom hides detail | Too strong | Reduce; mask |

## 12. Verification

- In motion: masks and tracking at full speed.
- After resizing and encoding: texture survival and artefacts.
- Across scene cuts: consistency of texture.
- With story intact: no story detail lost to darkness, bloom or smoothing.

## Dependencies

- Depends on: [Color Management](Color-Management.md), [Correction and Shot Matching](Correction-and-Shot-Matching.md), [Creative Grading](Creative-Grading.md), [Reading and Designing Light](../LIGHTING/Reading-and-Designing-Light.md).
- Feeds: [Quality Control and Export](../DELIVERY/Quality-Control-and-Export.md), [Repair and Finishing](../VFX/Repair-and-Finishing.md).

## Confidence summary

Local shaping tools, their limits and texture-compression interactions are `[Practice]`. Order of operations is a `[Heuristic]`; tools and pipelines differ. Statements about film-associated cues are `[Practice]`; "equivalence" claims are deliberately rejected. Examples are `[Illustrative]`.
