# Localization: Language, Script and Meaning

**Purpose:** Teach how to carry meaning faithfully across languages and scripts in captions, subtitles, on-screen text and narration — translation versus adaptation, script behaviour (with Hindi/Devanagari as the detailed case), names, numbers, terminology, cultural connotation and review.

**Applies to:** Any piece with more than one language version, subtitled testimony, bilingual graphics, or speakers who code-switch.

**Prerequisites:** [Typography System](Typography-System.md), [Captions and Accessibility](Captions-and-Accessibility.md).

**Owns:** Script-specific behaviour, translation/adaptation practice and linguistic review. The **workflow** of producing language versions (version matrix, re-timing narration, approvals, delivery) is owned by [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md).

---

## 1. Four different operations

| Operation | What it does | Where it fits | Risk |
|---|---|---|---|
| Translation | Renders meaning from one language into another as faithfully as possible | Testimony subtitles, factual narration, legal or safety text | Literalism that distorts idiom or tone |
| Adaptation | Rewrites for length, rhythm, tone and cultural fit within approved meaning | On-screen copy, narration that must fit picture, calls to action | Drift from approved meaning |
| Transcreation | Re-creates the intent (often of persuasive copy) with new wording, possibly new imagery | Taglines, advertising concepts | Becomes a different message; needs fresh approval |
| Transliteration | Writes words of one language in another script without translating | Names, brand names, technical terms used as loanwords | Inconsistent spellings; unfamiliar to some readers |

Most localization combines them: testimony is translated, labels are adapted, the tagline may be transcreated, and names are transliterated consistently.

## 2. Faithful meaning versus literal words

A literal translation can be inaccurate. A free translation can add meaning. The goal is **equivalent meaning and effect for the viewer**, constrained by the genre contract: testimony demands closer fidelity than advertising copy.

**Hypothetical example (Project A):** Asha says in Hindi, "इंतज़ार करते-करते आँखें पथरा गईं।"

| Rendering | Text | Assessment |
|---|---|---|
| Literal | "While waiting and waiting, the eyes turned to stone." | Grammatically faithful, but the idiom is opaque or oddly poetic to English readers |
| Faithful | "I waited until I couldn't wait any more." | Conveys the meaning (exhausted, endless waiting) in natural English |
| Over-free | "It felt like forever and I was furious." | Adds anger she did not express |

**Choice:** the faithful rendering. For testimony, a bilingual reviewer confirms it, and where the line carries story weight, Asha (or a trusted bilingual person close to the context) is asked whether the English version represents what she meant.

### Things that do not translate one-to-one

- **Politeness and intimacy forms:** Hindi distinguishes आप (formal "you"), तुम (familiar) and तू (very intimate or rude). English "you" loses the distinction. When the form carries meaning — a shift from आप to तुम signalling a change in relationship — the subtitle may need to carry it another way (word choice, a name, tone), or accept the loss knowingly.
- **Gendered grammar:** Hindi verbs and adjectives agree with the gender of the subject: "मैं थक गई थी" (a woman: "I was tired") versus "मैं थक गया था" (a man). Translating *into* Hindi requires knowing the speaker's or narrator's gender; machine translation commonly defaults to masculine forms.
- **Code-switching:** many Hindi speakers mix English words ("night shift", "drip", "BP"). Subtitles into English simply include them; Hindi captions must decide how to write them (Devanagari transliteration like "नाइट शिफ़्ट" or Latin script) — and apply the decision consistently.
- **Humour, irony and understatement:** Asha's "चाय भी तो खाना है" ("Tea counts as food too") is a joke whose effect depends on tone; the subtitle must keep it short and land at the laugh.

## 3. Devanagari in practice

The type-system implications (no letter-spacing, leading, font support) are in [Typography System](Typography-System.md#51-devanagari-hindi-essentials-for-the-type-system). This section covers language-level behaviour that affects captions, graphics and review.

### 3.1 Encoding and shaping

Devanagari text is stored as Unicode code points and *shaped* by the rendering engine into visible glyphs: consonant clusters joined with a virama (्) form conjuncts; vowel signs attach to consonants; the short-i sign (ि) is stored after its consonant but drawn before it. Tools that do not apply shaping display broken text. **Test every tool in the chain** — caption editor, graphics application, encoder burn-in, the destination player — with real text containing conjuncts and above/below marks.

### 3.2 Characters, clusters and counting

What a reader perceives as one letter (an *akshara*, e.g., क्षि) may be several code points. Consequences:

- **Character limits per line** designed for Latin text do not transfer; a "42-character" limit counted in code points is misleading for Devanagari. Use the destination's Hindi guide, or define limits by tested on-screen width and reading tests.
- **Animations, line breaks and highlighting** must operate on grapheme clusters, never splitting a conjunct or separating a matra from its consonant.

### 3.3 Line breaking and punctuation

- Break lines at spaces between words; Hindi is not normally hyphenated in captions.
- Do not break before the full stop or danda.
- The traditional sentence end mark is the danda (।); modern Hindi media use either the danda or the Latin full stop. Choose one in the style guide; use it consistently.
- Question and exclamation marks are used as in English.

### 3.4 Nukta and spelling variants

Some sounds borrowed from Persian/Arabic or English are written with a nukta dot (e.g., ज़, फ़). Usage varies between writers and publications; the style guide should decide (e.g., "फ़िल्टर" with nukta or "फिल्टर" without) and apply it consistently, including in names where the person's preference governs.

### 3.5 Numerals

Decide between Devanagari digits (०–९) and international digits (0–9). Many contemporary Hindi media use international digits; some formal or traditional contexts use Devanagari digits. The audience and client preference decide; consistency is mandatory, including in charts and captions.

## 4. Text expansion and contraction

Translated text changes length. The amount varies by language pair, register and content; Hindi narration can run longer or shorter than English depending on terminology and phrasing, and spoken duration does not track written length exactly. **Do not plan on a fixed percentage**; plan room, then test with the actual translation:

- Graphics: design boxes and layouts with headroom for longer text, and rules for what happens if text still does not fit (adapt wording, not shrink beyond tested limits).
- Narration: time the translated script read aloud at the intended pace before animating to it (see [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md)).
- Captions: reading load changes; re-time rather than reuse source timings.

## 5. Names, numbers, units and terminology

| Item | Practice |
|---|---|
| People's names | Spell as the person prefers in each script; record both spellings in a glossary |
| Place names | Use established spellings; check local conventions |
| Product and brand names | Usually kept in Latin script, or transliterated per brand guidelines |
| Numbers and units | Convert units only when the audience needs it and the source supports it; keep precision honest (do not convert "about 3 litres" into "3.17 litres") |
| Currency and dates | Use local formats in each version; check approval for any converted value |
| Technical vocabulary | Build a glossary with the advisor: which terms are translated, transliterated or left in English |

### Terminology example (hypothetical, Project C)

The filter's ceramic element is called a "candle" in English. A literal Hindi translation, "मोमबत्ती", means a *wax* candle — viewers would be confused or misled. Households that own such filters commonly call it "कैंडल" (transliterated) or describe it as "फ़िल्टर की कैंडल". The glossary records: **candle → "कैंडल" (on first use: "फ़िल्टर कैंडल")**, approved by the advisor and tested with two Hindi-speaking viewers.

## 6. Cultural connotation and stereotypes

Words, colours, gestures, foods, clothing, music and settings carry connotations that differ between audiences. Localization should check:

- Whether an example, joke or image means the same thing to the new audience.
- Whether depictions reinforce stereotypes (about regions, castes, religions, genders, classes); a version for a new audience may surface assumptions invisible in the source.
- Whether colour symbolism in graphics (e.g., an accent colour) has unintended associations in context.

The aim is accurate and respectful communication, not erasing specificity: Project A is about a specific place and person, and its localization should not "generalise" her.

## 7. Right-to-left and other scripts

Where the version set includes right-to-left languages (Arabic, Urdu, Hebrew) or other complex scripts (Bengali, Tamil, Thai), the same principles apply with script-specific rules: RTL alignment and mirrored layouts, bidirectional handling of numbers and Latin words inside RTL text, joined letterforms that forbid letter-spacing, and fonts with complete script support. Bring in a fluent reviewer for each script; do not rely on visual inspection by non-readers.

## 8. Linguistic review workflow

| Stage | Who | Checks |
|---|---|---|
| 1. Translation / adaptation | Qualified translator briefed with the glossary, speaker genders, tone and contract | Meaning, register, terminology |
| 2. Linguistic review | A second fluent reviewer | Accuracy, naturalness, consistency, spelling, typography of the language |
| 3. In-context review | Reviewer watching the picture with text/VO | Timing, line breaks, readability, fit with image, lip sync where relevant |
| 4. Subject/speaker review (testimony) | The speaker or a trusted bilingual person | "Is this what you meant?" |
| 5. Subject-matter review | Advisor (factual content) | Technical and factual accuracy in each language |
| 6. Final QC on encoded files | QC operator who reads the language, or a reviewer | Rendering, shaping, missing glyphs, placement |

Machine translation can draft; it cannot replace stages 2–6. See [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md) for approval gates when AI drafts translations or transcripts.

## 9. Worked example 1 — Testimony subtitles (hypothetical, Project A, Hindi → English)

**Material:** six minutes of Hindi speech with code-switching, humour and one idiom.

| Decision | Choice | Rationale |
|---|---|---|
| Fidelity level | Faithful, close to speech; condensed only where reading rate requires | Documentary testimony |
| Code-switched English words | Kept as spoken ("night shift", "drip") | Faithful; natural in English |
| Idiom (eyes turned to stone) | Faithful rendering | See Section 2 |
| Joke ("tea counts") | Short, timed to the laugh | Humour depends on timing |
| Politeness forms | Asha uses आप with a senior doctor and तुम with Sunita; subtitles convey through names/titles ("Doctor", "Sunita") rather than forms | English lacks the distinction |
| Uncertain words | Two words indistinct under the fan noise; subtitle uses "[indistinct]" rather than a guess | No fabricated testimony |
| Review | Bilingual reviewer; Asha reviews the three story-carrying subtitles | Representation |

**Verification:** a bilingual viewer watches with subtitles and reports any line where the English changes the meaning or tone. An English-only viewer summarises Asha's character; the summary should match the bilingual viewer's.

## 10. Worked example 2 — Bilingual labels and narration (hypothetical, Project C, English ↔ Hindi)

| Element | English | Hindi | Notes |
|---|---|---|---|
| Step label | "Step 2: Brush" | "स्टेप 2: ब्रश करें" or "चरण 2: ब्रश करें" | Style guide decision: the channel's audience research suggests "स्टेप" is more widely understood in this context than the formal "चरण"; chosen "स्टेप" with international digits |
| Warning | "No soap" | "साबुन नहीं" | Short, unambiguous; icon reinforces |
| Term | "candle" | "कैंडल" | Glossary; avoids "मोमबत्ती" |
| Narration | Female narrator in both languages | Hindi script uses feminine first-person forms where the narrator refers to herself | Translator briefed on narrator gender |
| Chart unit | "colonies per 100 mL" | "प्रति 100 mL कॉलोनी" or a simpler label with a spoken explanation | Advisor approval; simpler wording tested with viewers |

**Timing check:** the Hindi narration for the mechanism section is read aloud at the intended pace and timed before animation; labels are held longer in the Hindi version where the narration is longer.

## 11. Counterexample and repair — machine translation in the narration

**Hypothetical counterexample.** To save time, Project C's English script is machine-translated into Hindi and sent directly to the narrator. In the recording, the narrator (a woman) reads first-person lines in masculine forms ("मैंने पहले गलत तरीके से साफ़ किया था, फिर मैं समझ गया" — masculine "समझ गया"), the "candle" becomes "मोमबत्ती" throughout, and "Do not use soap" becomes a construction the advisor flags as ambiguous. The narrator corrects some forms on the fly, inconsistently.

**Diagnosis:** no glossary, no speaker-gender brief, no linguistic review before recording.

**Repair:**
1. A translator revises the script using the glossary and the narrator's gender; a second reviewer checks.
2. The advisor approves technical terms and the safety instruction wording.
3. The narration is re-recorded (cheaper than repairing an inconsistent take).
4. Captions are generated from the approved script and re-timed to the new recording.

**Verification:** a Hindi-speaking reviewer listens to the full narration with the script; a small group of target viewers confirms the term "कैंडल" is understood and the safety instruction is unambiguous.

## 12. Micro-decisions

- Give translators the picture, not just the script; context resolves ambiguity.
- Brief translators with speaker genders, relationships and tone.
- Maintain one glossary per project across captions, graphics, narration and descriptions.
- Keep source and translated text versioned together, so a source change triggers a translation change.
- Use the person's preferred spelling of their name in every script; ask them.

## 13. Failure signatures and corrections

| Symptom | Likely cause | Correction |
|---|---|---|
| Native viewers find subtitles "odd" | Literal translation | Faithful adaptation; review |
| Inconsistent terms | No glossary | Glossary; consistency pass |
| Wrong gender forms | Translator not briefed; machine translation | Brief; review; re-record if needed |
| Broken Devanagari | Shaping failure in a tool | Test tool chain; change tool or font |
| Text doesn't fit | Expansion not planned | Adapt wording; layout headroom |
| Meaning drift in testimony | Free translation | Speaker review; closer fidelity |

## 14. Verification

- Bilingual review for meaning; in-context review on picture; speaker review for testimony; advisor review for technical content.
- Rendering checks on the final encoded file and destination player for each script.
- Fresh-viewer comprehension in each language.

## Dependencies

- Depends on: [Typography System](Typography-System.md), [Captions and Accessibility](Captions-and-Accessibility.md), [Interview Craft](../STORY/Interview-Craft.md).
- Workflow and delivery: [Versioning and Localization](../DELIVERY/Versioning-and-Localization.md).
- AI drafts: [Assistance and Control](../AI-WORKFLOWS/Assistance-and-Control.md).

## Confidence summary

The distinction between translation, adaptation, transcreation and transliteration, the review workflow and the grapheme-cluster rule are `[Practice]`. Devanagari shaping behaviour, gender agreement and politeness forms are linguistic facts. Choices such as nukta usage, digit style and loanword spelling are `[Preference]` decided per style guide. Hindi example sentences are illustrative and should be reviewed by a fluent speaker before reuse in production.
