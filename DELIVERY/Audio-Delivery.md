# Audio Delivery: Loudness, Peaks, Layouts and Stems

**Purpose:** Teach how to deliver audio that complies with each destination's requirements — loudness targets and measurement methods, peak limits, channel layouts, stems and file formats — and why one loudness number never fits every destination.

**Applies to:** Final mixes and their deliverables for broadcast, streaming services, online platforms, cinema, events and archives.

**Prerequisites:** [Mix Strategy](../AUDIO/Mix-Strategy.md) (mix technique and measurement vocabulary).

**Owns:** Destination audio compliance. Mix technique is owned by [Mix Strategy](../AUDIO/Mix-Strategy.md); general export settings by [Quality Control and Export](Quality-Control-and-Export.md).

---

## 1. Destinations differ — by design

Loudness standards and specifications exist so that programmes play at consistent levels within a destination. Different destinations have chosen different targets and measurement methods because their listening contexts differ (living-room TV, cinema, phone, car). A mix "to −14 LUFS" for everything is a common mistake; so is assuming broadcast targets suit online platforms.

## 2. Verified and unverified reference figures

The figures below were checked on 2026-10-04 to the extent stated. **Always re-check the current specification of the actual destination and the contract before delivery.** Full source details are in [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md).

| Destination / document | Target and tolerance | Peak limit | Measurement notes | Verification status |
|---|---|---|---|---|
| EBU R 128 (2023 revision), European broadcast recommendation | Programme loudness −23.0 LUFS; where the target is not practically achievable (e.g., live programmes) a tolerance of ±1.0 LU is permitted; a ±0.2 LU tolerance is allowed in QC environments to account for measurement error | Maximum true peak −1 dBTP during production (lower may be needed for some distribution systems) | Whole-programme measurement, not dialogue-only; BS.1770 meter with gating, compliant with EBU Tech 3341 | `[Requirement]` — primary document read |
| ATSC A/85 (US broadcast recommended practice; referenced under the CALM Act) | −24 LKFS for content exchanged without metadata, with a commonly cited ±2 dB tolerance | Per broadcaster spec | Built on BS.1770; dialogue-anchored practice | `[Requirement]` as reported by secondary sources; primary document not read |
| Netflix sound mix specification (as published in its partner help centre) | −27 LKFS ±2 LU, dialogue-gated | True peak generally not exceeding −2 dBTP | Dialogue-gated measurement (BS.1770 with dialogue gating), measured on specified re-renders | `[Requirement]` for that destination as quoted from the partner help centre in search results; full page not read |
| AES TD1008 (recommendations for internet audio streaming and on-demand distribution) | Distribution loudness −18 LUFS for speech and "assorted" content; music normalised to no more than −16 LUFS | Maximum true peak not exceeding −1 dBTP at the codec input of lossy streams | A recommendation for distributors and services, not a platform specification | `[Practice]` (recommendation) as reported by secondary sources |
| Major online video platforms' playback normalisation | Some platforms turn down content louder than a reference (one widely reported reference is about −14 LUFS for a major video platform) | — | Based on third-party measurement and observation; platforms do not always publish official figures, and behaviour can change | **Unverified** — treat as observed behaviour, not a specification |

### What this table means in practice

- **Broadcast:** mix and measure to the broadcaster's specification (often based on EBU R 128 or ATSC A/85), including their tolerances, peak limits and any loudness range or dialogue requirements.
- **Streaming services with published specs:** follow their documents exactly, including measurement method (dialogue-gated vs full programme) and which re-renders are measured.
- **Online platforms without published specs:** mix for the content's dynamic intent at a moderate loudness, keep true peaks safe for lossy encoding, and check how the platform's normalisation changes the result (see [Mix Strategy](../AUDIO/Mix-Strategy.md#7-platform-normalisation-as-a-creative-constraint)).
- **Cinema:** mixed in calibrated rooms at reference playback levels; loudness practices differ from broadcast; follow the distributor's and exhibitor's requirements.
- **Events and projection:** consider the venue's system; deliver a version suitable for the room, and test.

## 3. Measurement methods matter

| Method | Measures | Used by |
|---|---|---|
| Full-programme integrated loudness (gated) | All content | EBU R 128 and many broadcast specs |
| Dialogue-gated loudness | Only passages detected as dialogue | Some streaming and broadcast specs; dialogue-anchored practice |
| True peak | Inter-sample peaks | Most specs |
| Loudness range (LRA) | Macro-dynamics | Some specs (as guidance or limit) |
| Short-term / momentary maxima | Sudden loud moments | Some specs (e.g., for commercials or loudness jumps) |

A mix can comply with a full-programme target and fail a dialogue-gated one, or vice versa — a dynamic film with quiet dialogue and loud action may measure differently by the two methods. Measure with the method the destination specifies.

## 4. Channel layouts and stems

### 4.1 Layouts

| Layout | Use | Considerations |
|---|---|---|
| Mono | Some archives, radio, specific accessibility outputs | Rare for video |
| Stereo (2.0) | Online, social, most corporate | Check mono fold-down |
| 5.1 surround | Broadcast, streaming, cinema | Channel order must match the spec (orders differ between conventions); LFE handling; downmix behaviour |
| 7.1 and immersive/object-based formats | Cinema, premium streaming | Specialist workflows; required re-renders (e.g., 5.1 and 2.0) and their compliance |

### 4.2 Stems

Stems are sub-mixes that sum to the full mix:

| Stem | Contents | Why |
|---|---|---|
| Dialogue (D) | All dialogue and narration | Localization (dubbing); re-mixes |
| Music (M) | All music | Licence changes; re-edits |
| Effects (E) | Sound effects, Foley, ambience | Re-mixes |
| M&E | Music and effects without dialogue (often with production effects that were on dialogue tracks rebuilt or included) | International versions |
| Dialogue-free / textless variants | Per spec | Adaptation |

Deliver stems only within a specified delivery context; their exact definition (e.g., whether production effects are in D or E, whether narration is separate) varies by destination.

## 5. File and format decisions

| Item | Typical professional delivery (verify per spec) |
|---|---|
| Sample rate | 48 kHz for video |
| Bit depth | 24-bit for masters |
| File format | Broadcast WAV (multichannel or multiple mono files per spec), or audio embedded in the master video file |
| Track layout | Documented in a track sheet: which channel/track carries what |
| Sync | Start timecode, 2-pop or sync marks where required |
| Metadata | Programme loudness, dialogue normalisation values where required by the system |

**Distribution encodes:** lossy codecs (e.g., AAC) can raise peaks and change tone at low bitrates. Measure true peak on the encoded file where the destination encodes from your file, and leave headroom accordingly.

## 6. Worked example 1 — Explainer delivered to several destinations (hypothetical, Project C)

**Destinations:** the public-health channel's website (online player), a regional broadcaster that will air the Hindi version (spec supplied: hypothetical document based on EBU R 128 with −23 LUFS and −1 dBTP), and community screenings.

| Deliverable | Target | Rationale |
|---|---|---|
| Broadcast master (Hindi) | Per broadcaster's document (e.g., −23 LUFS integrated, ≤ −1 dBTP), stereo, 48 kHz/24-bit, with the channel layout and track sheet the broadcaster specifies | Compliance |
| Web masters (Hindi, English) | A moderate integrated loudness chosen for speech-led content on phones (e.g., in the region of the AES TD1008 speech recommendation, −18 LUFS, with true peak ≤ −1 dBTP) | Intelligible on small speakers; safe for encoding; avoids being turned down heavily or up excessively |
| Screening copy | Web master, checked in a representative room; level set on the PA during setup | Room-dependent |
| M&E | No target loudness; matched to the full mix's balance | Future localization |

**Process:** one mix session; separate masters rendered and measured individually; true peak measured after a test encode for the web versions.

**Verification:** meter readings recorded per deliverable (integrated, true peak, LRA if requested); listening on a phone and a TV; broadcaster QC report reviewed.

## 7. Worked example 2 — A brand campaign's audio deliverables (hypothetical, Project B)

| Deliverable | Notes |
|---|---|
| Social and pre-roll masters | Stereo; moderate loudness consistent with dynamic intent; true peak ≤ −1 dBTP after test encode; checked after platform normalisation by level-matching against reference content |
| Product-page player | Same as social, checked in the actual page player (some web players do not normalise) |
| Possible TV placement (future) | Not mixed to broadcast spec now; stems (D, M, E) and M&E delivered so a broadcast-compliant version can be produced if the media plan changes |
| Stems | D (VO and founder dialogue), M (Track B edit), E (product sounds, Foley, ambience) |

## 8. Counterexample and repair — the "−14 everywhere" mix

**Hypothetical counterexample.** A documentary is mixed to about −14 LUFS integrated with heavy limiting "because that's the online standard" and then delivered unchanged to a broadcaster whose spec requires −23 LUFS (EBU R 128-based). The file fails QC. The editor lowers the gain by 9 dB to pass — compliance achieved — but the heavy limiting remains: the documentary sounds flat and fatiguing on air, with dialogue and music crushed together.

**Diagnosis:** a single loudness number applied to all destinations; dynamics destroyed by limiting that the broadcast target never required.

**Repair:**
1. Return to the pre-limited mix.
2. Mix for the broadcast destination with appropriate dynamics; measure per spec.
3. For online, derive a separate master with a moderate loudness and safe true peaks, checked after platform normalisation.
4. Document both masters in the version matrix (see [Versioning and Localization](Versioning-and-Localization.md)).

**Verification:** broadcaster QC passes; level-matched comparison shows the new broadcast mix has more natural dynamics; the online master behaves well after normalisation.

## 9. Micro-decisions

- Ask for the destination's audio specification at the brief stage, not at export.
- Record meter type, settings and readings in the QC sheet for each deliverable.
- Measure the actual delivered file, not the session.
- Keep the mix session organised as D/M/E buses so stems are trivial to render.
- After loudness adjustments, listen again — compliance changes can expose noise or change balance.

## 10. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| QC failure on loudness | Wrong target or measurement method | Re-measure per spec; adjust the mix, not only gain |
| QC failure on true peak | Limiter not true-peak aware; encoding raised peaks | True-peak limiting; headroom |
| Dialogue too quiet on air | Full-programme target met but dialogue low | Dialogue-anchored balance; check dialogue-gated reading if specified |
| Channel swapped in surround | Wrong channel order | Follow spec order; check with test tones |
| Stems don't sum to mix | Processing on the master bus not reflected in stems | Process stems consistently; verify null test |

## 11. Verification

- Compliant meter readings on the delivered files for every audio deliverable.
- Listening checks on representative systems.
- Track sheets and channel orders verified with test signals or careful listening.
- Stems verified by summing to the full mix (null test where possible).

## Dependencies

- Depends on: [Mix Strategy](../AUDIO/Mix-Strategy.md).
- Companion: [Quality Control and Export](Quality-Control-and-Export.md), [Versioning and Localization](Versioning-and-Localization.md).
- Sources: [Sources and Limitations](../SOURCES-AND-LIMITATIONS.md).

## Confidence summary

EBU R 128-2023 figures are `[Requirement]` from the primary document. ATSC A/85, Netflix and AES TD1008 figures are reported with their verification level as stated. Online platform normalisation references are explicitly **unverified** observations. Layout and stem practices are `[Practice]`. Example targets for hypothetical deliverables are `[Illustrative]`.
