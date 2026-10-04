# Sources and Limitations

**Purpose:** Record the external sources checked for this library, what each supports, how thoroughly it was verified, which items remain unverified, and the limits of the advice overall.

**Checked on:** 2026-10-04, using web search and page fetches available in the authoring environment. Summaries are in this library's own words.

---

## 1. Verified sources

"Verification level" states exactly what was checked:
- **Primary, read** — the authoritative document itself was opened and the cited clauses read.
- **Primary, excerpt** — the authoritative page was identified and the cited figures appeared in a direct excerpt (e.g., a search result quoting the page), but the full page was not read.
- **Secondary** — the figure was reported by a reputable secondary source; the primary document was not read.

| # | Title / organisation | Link | Verification level | Claims supported | Version / context | Used in |
|---|---|---|---|---|---|---|
| 1 | EBU R 128 — Loudness normalisation and permitted maximum level of audio signals (European Broadcasting Union) | https://tech.ebu.ch/docs/r/r128.pdf | Primary, read | Programme loudness target −23.0 LUFS; ±1.0 LU tolerance where the target is not practically achievable (e.g., live); ±0.2 LU tolerance in QC environments for measurement error; maximum true peak −1 dBTP in production (lower may be needed for some distribution systems); measurement with BS.1770-compliant meters including gating and EBU Tech 3341; whole-programme measurement; LUFS equivalent to LKFS | EBU R 128-2023 (version 5, November 2023) | [Audio Delivery](DELIVERY/Audio-Delivery.md), [Mix Strategy](AUDIO/Mix-Strategy.md) |
| 2 | Understanding Success Criterion 2.3.1: Three Flashes or Below Threshold (W3C WAI, WCAG 2.2) | https://www.w3.org/WAI/WCAG22/Understanding/three-flashes-or-below-threshold.html | Primary, read | Level A criterion wording; general and red flash thresholds; area condition (25% of a 10° visual field) | WCAG 2.2 | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md) |
| 3 | English (USA) Timed Text Style Guide (Netflix Partner Help Center) | https://partnerhelp.netflixstudios.com/hc/en-us/articles/217350977-English-USA-Timed-Text-Style-Guide | Primary, read (summarised by fetch tool) | 42 characters per line; maximum two lines; reading speed up to 20 cps (adult) and 17 cps (children's) | As published at check date; minimum/maximum durations and gaps were not found on the fetched page and are not stated in this library | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |
| 4 | Netflix Sound Mix Specifications & Best Practices (Netflix partner help) | https://backlothelp.netflix.com/hc/en-us/articles/360001794307-Netflix-Sound-Mix-Specifications-Best-Practices-v1-5 | Primary, excerpt | Average loudness −27 LKFS ±2 LU dialogue-gated; true peak generally not exceeding −2 dBTP | Page title indicates v1.5; check current version | [Audio Delivery](DELIVERY/Audio-Delivery.md) |
| 5 | ITU-R BT.1702 — Guidance for the reduction of photosensitive epileptic seizures caused by television (ITU) | https://www.itu.int/rec/R-REC-BT.1702 | Primary, excerpt (title and in-force version from ITU listing in search results) | Existence, title and current version BT.1702-3 (approved November 2023) | Content not reproduced | [Quality Control and Export](DELIVERY/Quality-Control-and-Export.md) |
| 6 | ACES 2.0 release (Academy of Motion Picture Arts and Sciences; OpenColorIO) | https://press.oscars.org/news/academy-motion-picture-arts-and-sciences-launches-next-chapter-aces-academy-software ; https://opencolorio.readthedocs.io/en/main/releases/ocio_2_4.html | Primary, excerpt + secondary (trade press) | ACES 2.0 released April 2025 with new output transforms including improved gamut mapping; OpenColorIO 2.4 implements ACES 2.0 configurations | Application-specific behaviour not verified | [Color Management](COLOR/Color-Management.md) |
| 7 | ATSC A/85 recommended practice (reported) | e.g., https://www.tvtechnology.com/opinions/lkfs-amp-the-calm-act | Secondary | −24 LKFS target for content exchanged without metadata, commonly cited ±2 dB tolerance; built on BS.1770; relationship to the US CALM Act | Primary ATSC document not read | [Audio Delivery](DELIVERY/Audio-Delivery.md) |
| 8 | AES TD1008 — Recommendations for loudness of internet audio streaming and on-demand distribution (reported) | e.g., https://productionadvice.co.uk/td1008/ | Secondary | −18 LUFS distribution loudness for speech and assorted content; music normalised to no more than −16 LUFS; maximum true peak −1 dBTP at codec input of lossy streams | Primary AES document not read | [Audio Delivery](DELIVERY/Audio-Delivery.md) |
| 9 | BBC subtitle guidelines (reported) | Reported by e.g. https://clevercast.com/bbc-subtitling-guidelines | Secondary (the BBC page could not be fetched from the authoring environment) | Presentation rate around 160–180 words per minute, with editorial variation | Verify against the current BBC guidelines before claiming compliance | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |
| 10 | FCC closed captioning quality standards, 47 CFR 79.1(j) (reported) | e.g., https://www.dwt.com/insights/2014/02/fcc-adopts-closed-caption-quality-standards | Secondary | Four quality categories: accuracy, synchronicity, completeness, placement; accuracy includes lyrics of music in the audio track | Applies to covered US television programming; regulation text not read | [Captions and Accessibility](TEXT-ACCESSIBILITY/Captions-and-Accessibility.md) |

## 2. Items used but not verified (and how that affects use)

| Item | Status | Effect on usage |
|---|---|---|
| Online video platform playback normalisation (e.g., a reference around −14 LUFS on a major platform) | Third-party observation (e.g., https://productionadvice.co.uk/stats-for-nerds/); not an official specification | Treated as observed behaviour; mix for dynamic intent and check after normalisation rather than targeting the number |
| Ofcom flashing-image guidance specifics | Reported via secondary sources only | Do not claim UK broadcast compliance without reading the current Ofcom guidance and the broadcaster's specification |
| ITU-R BS.1770 and EBU Tech 3341 details | Referenced by EBU R 128 (verified); the documents themselves were not read | Window lengths (400 ms, 3 s) and gating are stated as widely documented facts; consult the standards for implementation |
| Display standards (BT.709, BT.1886, BT.2020, BT.2100, SMPTE ST 2084, sRGB) | Stable, widely documented; not fetched for this library | Used for concepts only; destination specifications decide which apply |
| Platform dimensions, safe zones, durations, caption formats, ad specs | Deliberately not stated | Must be checked per destination at delivery time |
| Drone, filming-permit and data-protection rules; EU AI Act transparency obligations; India's DPDP Act; GDPR | Mentioned only as examples of applicable regimes; obligations not verified | Consult current law and counsel; nothing here is legal advice |
| Generative AI product capabilities, terms, retention and pricing | Deliberately not described per product | Check current terms of any named service before use |
| Juxtaposition (Kuleshov-type) research | Summarised generally as mixed findings; no specific study cited | Treated as a `[Heuristic]` |
| Camera log curves' exposure targets | Deliberately not given | Use manufacturer documentation for the curve in use |

## 3. Limits of the advice

1. **No real material was analysed.** Every observation about footage, sound, levels or colour is hypothetical and labelled. The library does not claim to have seen continuity defects, measured peaks or inspected waveforms of any real project.
2. **Craft heuristics are not laws.** They are labelled `[Heuristic]` and come with boundary conditions. Taste remains open to reasonable disagreement.
3. **Small viewer tests indicate, not prove.** Fresh-viewer checks reveal clarity problems for those viewers; they do not establish audience-wide effects or commercial outcomes.
4. **Time-sensitive specifications change.** Even verified figures must be re-checked against the current destination document before delivery.
5. **Language examples.** Hindi sentences are illustrative and should be reviewed by a fluent speaker before reuse in production.
6. **Legal and ethical guidance is practical, not legal advice.** Laws, contracts and commissioners' codes govern actual obligations.
7. **Software-independent by design.** Where tools are mentioned, they are described by capability; menu names and features vary by application and version.
8. **What this library cannot do:** reveal any artist's private cognition, guarantee engagement or sales, remove subjective disagreement, or recover information that was never captured.

## 4. How to re-verify

For each `[Requirement]` used in a real delivery:
1. Identify the authority (standards body, platform specification page, accessibility guideline, broadcaster delivery document, manufacturer documentation).
2. Open the current version; note its date and version.
3. Record the clause or figure, the date checked and the deliverable it applies to in the project's delivery profile (see [Worksheets and Logs](TEMPLATES/Worksheets-and-Logs.md#29-delivery-profile)).
