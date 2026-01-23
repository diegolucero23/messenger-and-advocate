# Latter Day Saints' Messenger and Advocate (1844-1847)

> **Historical Transcriptions Project**
> *A complete, structured, and searchable digitization of Sidney Rigdon's Pittsburgh publication following the 1844 Succession Crisis.*

## 📜 About The Project

This repository serves as the digital archive for the *Latter Day Saints' Messenger and Advocate*, a historically critical newspaper published in Pittsburgh, Pennsylvania, beginning October 15, 1844.

While the history of the "Utah Period" of the Church of Jesus Christ of Latter-day Saints is well-documented, the perspective of the **Rigdonite Succession** has often been obscured by poor quality scans and lack of indexable text. This project remedies that by providing accurate OCR and Markdown transcriptions of the 24-issue run (384 pages).

### Historical Significance
This publication documents the immediate aftermath of the martyrdom of Joseph and Hyrum Smith. It represents the primary platform used by **Sidney Rigdon** (the only surviving member of the First Presidency at the time) to challenge the authority of Brigham Young and the Quorum of the Twelve.

**Key Historical Threads preserved in these transcripts:**
* **The Schism:** Rigdon's assertion that the Twelve were a "travelling, presiding High Council" intended to labor abroad, not to usurp the Presidency in Zion.
* **Polygamy Controversies:** Explicit, contemporary allegations against the Twelve regarding "Spiritual Wifery," which Rigdon denounces as the "doctrine of the Nicolaitans" and a "secret work of darkness".
* **Nauvoo "Corruptions":** First-hand accounts (letters from Samuel L. and John A. Forgeus) describing the social and theological state of Nauvoo in late 1844, including the "secret chambers" and the alleged "beating of the people".
* **Ecclesiastical Reorganization:** Minutes from the Pittsburgh Conference (Oct 1844) detailing the excommunication of the Twelve by the Rigdonite body and the affirmation of the "original platform" of the Church.

## 📂 Repository Structure

The data is organized into "sets" based on the date of processing to allow for version control and OCR improvements.

```text
messenger-and-advocate/
├── scans/
│   └── jan-5-2026/       # Original high-res PNG scans (e.g., page_001.png)
├── transcripts/
│   └── jan-5-2026/       # JSON structured transcripts with rich metadata
├── scripts/              # Tools used for OCR and text parsing
└── README.md
```

## 🤝 Call for Volunteers (Verification)

**Current Status**: *Verification Phase (Jan 2026)*

I have created a complete transcription set (`jan-5-2026`). These texts are currently being verified against the original images to ensure every theological argument and historical name is preserved accurately.

**How to Help**: We are looking for volunteers to read the text in `transcripts/` and compare it against the `scans/`. Particular attention should be paid to:

* **Scriptural Citations**: The text frequently cites specific sections of the 1844 *Book of Doctrine and Covenants* (e.g., Section 101, Section 104). These numbers must be accurate.

* **Proper Names**: Ensure names like *B. Winchester*, *James M. Greig*, *Samuel L. Forgeus*, and *Eliza R. Snow* (if appearing) are spelled correctly.

## 🛠 Usage & Data Format

The transcripts are not just raw text; they are structured data designed for modern usage.

* **Format**: JSON objects containing Markdown text.

* **Metadata**: Each entry includes the publication date, page number, issue, and volume.

* **Application**: This structure is optimized for AI RAG (Retrieval-Augmented Generation) systems, allowing LLMs to cite specific historical snippets without hallucination.

See the [Transcripts README](https://github.com/diegolucero23/messenger-and-advocate/transcripts/README.md) for detailed documentation on the data schema.

## 📝 License

Distributed under the MIT License. See LICENSE for more information.

## 👤 Author

**Diego Lucero**

* GitHub: [@diegolucero23](https://github.com/diegolucero23)