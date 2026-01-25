# Transcription Style Guide & Volunteer Protocol

**Project:** Latter Day Saints' Messenger and Advocate (1844-1847)
**Status:** Active Verification Phase
**Maintainer:** @diegolucero23

---

## 🏁 1. The Core Philosophy: "Diplomatic Transcription"

Welcome to the project! Our goal is **not** to edit, improve, or modernize these newspapers. Our goal is to create a **digital twin** of the original 1844 documents.

We follow the principle of **Diplomatic Transcription**:
> **"Type what you see. If it is in the image, it goes in the text. If it is NOT in the image, it does not go in the text."**

We want future historians to see exactly what Sidney Rigdon wrote—including his unique spelling, the printer's mistakes, and the archaic language of the time. We are archivists, not editors.

---

## 📝 2. Spelling, Grammar, and Typos

This is the most critical section. You will constantly face a choice: *"Is this a mistake I should fix, or history I should preserve?"*

### A. Archaic Spelling (⛔ DO NOT FIX)
The English language in the 1840s was different. You will see spellings that look "wrong" to modern eyes. **You must preserve these exactly as they appear.**

* **Common Examples to KEEP:**
    * `shewing` (instead of *showing*)
    * `connexion` (instead of *connection*)
    * `publick` (instead of *public*)
    * `defence`, `offence`, `pretence` (using 'c' instead of 's')
    * `labour`, `honour`, `favour` (British/Archaic 'u')
    * `surprize`, `enterprize` (using 'z')

### B. Printer's Errors (⛔ DO NOT FIX)
Typesetters in 1844 often made mistakes—flipping letters, misspelling names, or missing punctuation. **We preserve these errors.** This allows researchers to cite the specific version of the text.
* **Scan:** "The prophit said..."
* **Transcription:** "The prophit said..." (Do NOT change to "prophet").
* **Scan:** "Josehp Smith"
* **Transcription:** "Josehp Smith" (Do NOT change to "Joseph").

*Tip: If a typo makes a word confusing, you may add `[sic]` immediately after it, but prefer to just type it as is.*

### C. OCR & Scanning Errors (✅ FIX THESE)
This is the main purpose of your verification. The computer software (OCR) frequently misreads letters. **You must correct these.**

* **Scan:** "the church of Christ" -> **OCR:** "tbe cburch of Cbrist"
    * **Action:** **FIX** to "the church of Christ".
* **Scan:** "burn" -> **OCR:** "bum"
    * **Action:** **FIX** to "burn".
* **Common OCR Scrambles:**
    * `rn` becoming `m` (e.g., `corn` -> `com`)
    * `cl` becoming `d` (e.g., `clear` -> `dear`)
    * `h` becoming `b`
    * `li` becoming `h`

### D. Hyphenation at Line Breaks (✅ FIX THESE)
Newspapers often break words across lines with a hyphen to justify the column. For digital searchability, we must **rejoin** these words.

* **Scan:**
    > ...the revel-
    > ation of...
* **Transcription:** "...the revelation of..." (Remove the hyphen and the newline).
* **Exception:** If the word is *always* hyphenated (e.g., "well-being", "self-defence"), keep the hyphen.

---

## ⌨️ 3. Formatting & Markdown Standards

We use standard Markdown to represent the visual hierarchy of the page.

### Headers
* **H1 (`#`):** Use ONLY for the main Newspaper Title on Page 1.
* **H2 (`##`):** Use for Major Article Headlines (e.g., `TO THE PUBLIC`, `COMMUNICATIONS`).
* **H3 (`###`):** Use for sub-headers, letter salutations, or distinct section breaks within an article.

### Emphasis
* **Italics:** If the text is italicized in the scan, wrap it in single asterisks.
    * Input: `*The Book of Mormon*`
    * *Note: This is very common for scriptural citations.*
* **Bold:** If the text is bold (often used in small headers), wrap it in double asterisks.
    * Input: `**SECTION 101.**`
* **ALL CAPS:** If the text is in ALL CAPS, type it in ALL CAPS.

### Layout
* **Columns:** Ignore column breaks. Treat the newspaper page as one continuous stream of text. Read Column 1 (top to bottom), then Column 2, then Column 3.
* **Paragraphs:** Add a single blank line between paragraphs.
* **Separators:** If there is a distinct horizontal line separating articles, use the Markdown horizontal rule: `---`.

---

## 📄 4. Handling Scriptural Citations

This publication heavily cites the Bible and the Doctrine and Covenants. Rigdon was inconsistent in how he abbreviated these. **Copy his inconsistency.**

* If he writes: `D. & C.`, you type `D. & C.`
* If he writes: `Book of Cov.`, you type `Book of Cov.`
* If he writes: `Book of Doctrine and Covenants`, you type the full phrase.

**Do not normalize citations.** (e.g., Do not change `Sec. 101` to `Section 101`).

---

## ❓ 5. Illegible, Damaged, or Missing Text

The original paper may be torn, stained, faded, or cut off.

* **Uncertainty:** If you are mostly sure but the ink is smeared, place the word in brackets with a question mark.
    * Example: `The [persecution?] was severe.`
* **Unreadable:** If a word is completely unreadable, use the tag `[illegible]`.
    * Example: `The [illegible] of the Twelve.`
* **Missing Page Corners:** If the paper is physically torn away, use `[missing text]`.

---

## 🤖 6. The JSON Wrapper (Technical Rules)

Every transcription file is a JSON object. It is vital that you **maintain valid JSON syntax**.

### The Structure
```json
{
  "metadata": {
    "publication": "Latter Day Saints' Messenger and Advocate",
    "volume": "1",
    "issue": "1",
    "page": "15",
    "date": "October 15, 1844",
    "source_file": "page_015.png"
  },
  "content": "MARKDOWN GOES HERE"
}
```

### The "Escaping" Rule (CRITICAL)

Because the entire transcript is inside a JSON string (the `"content"` field), you cannot simply use double quotes `"` inside your text, or it will break the file.

- **The Rule:** You must "escape" double quotes by putting a backslash `\` before them.

- **Bad Syntax:** `"content": "He said "Hello"."` (Computer crashes).

- **Good Syntax:** `"content": "He said \"Hello\"."` (Computer is happy).

Note: You do NOT need to escape single quotes/apostrophes (e.g., `Saints'` is fine).

## 🚫 7. What to Ignore

- **Modern Watermarks:** Do not transcribe "Digitized by...", "Google", "LatterDayTruth.org", or any URL stamps added by modern archives.

- **Handwritten Marginalia:** Unless it seems to be a correction by the original editor, ignore scribbles, doodles, or owner signatures (e.g., "John Smith's Copy") in the margins.

## ✅ 8. The Verification Checklist

Before you submit your file or mark a page as "Done," run through this mental checklist:

1. [ ] **Metadata:** Do the Volume, Issue, and Page Number in the JSON match the header on the image?

2. [ ] **De-Hyphenation:** Did I rejoin all words broken at the end of lines? (e.g., `judge-ment` -> `judgement`)?

3. [ ] **Archaic Spelling:** Did I resist the urge to fix `shewing` or `connexion`?

4. [ ] **OCR Cleanup:** Did I catch the nonsense words (e.g., `tbe`, `bum`, `corn`->`com`)?

5. [ ] **Quotes:** Did I backslash-escape all double quotes (`\"`) inside the JSON content?

## 🆘 Example Comparison

**Original Image Source:**

> *volume 1. pittsburgh, oct 15. no 1.*
> 
> ...for the judg- ment of God is up- on the nations. As stated in the *Book of Cov.* sec 101. the "wicked" shall [ink blot] perish.

**Correct Transcription:**

```json
{
  "metadata": {
     "volume": "1",
     "issue": "1",
     "date": "October 15, 1844",
     "page": "1"
  },
  "content": "...for the judgment of God is upon the nations. As stated in the *Book of Cov.* sec 101. the \"wicked\" shall [illegible] perish."
}
```