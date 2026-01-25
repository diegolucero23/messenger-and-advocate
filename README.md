# Latter Day Saints' Messenger and Advocate (1844-1847)

> **Historical Transcriptions Project**
>
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

The repository is organized to separate raw image data from structured text, while providing clear documentation for contributors in the root directory.

```text
messenger-and-advocate/
├── scans/
│   └── jan-5-2026/       # Original high-res PNG scans (e.g., page_001.png)
├── transcripts/
│   └── jan-5-2026/       # JSON structured transcripts with rich metadata
├── .gitignore            # System file ignoring node_modules, .env, etc.
├── CODE_OF_CONDUCT.md    # Standards for community interaction & historical neutrality
├── CONTRIBUTING.md       # Step-by-step instructions for volunteers
├── LICENSE               # MIT License
├── README.md             # Project overview (this file)
├── ROADMAP.md            # Current project status, milestones, and timeline
└── STYLE_GUIDE.md        # Strict rules for spelling, formatting, and JSON syntax
```

## 🤝 How to Contribute (Volunteer Portal)

**Current Status**: *Verification Phase (Jan 2026)*

We are currently verifying the raw OCR text against the original images. This is a manual process requiring human review to ensure historical fidelity.

**If you wish to help, please read the following documents in order:**

1.  **[CONTRIBUTING.md](./CONTRIBUTING.md)**: This is your "Start Here" guide. It explains the workflow (Claiming an Issue -> Forking -> Pull Request).
2.  **[STYLE_GUIDE.md](./STYLE_GUIDE.md)**: This is the most important document for accuracy. It explains how to handle archaic spelling (e.g., *shewing* vs *showing*), OCR errors, and JSON formatting.
3.  **[ROADMAP.md](./ROADMAP.md)**: Check this file to see which Volumes and Issues are currently open for verification.
4.  **[CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md)**: Please review our community standards regarding historical neutrality and respectful communication.

### What we are checking for:
* **Scriptural Citations**: The text frequently cites specific sections of the 1844 *Book of Doctrine and Covenants* (e.g., Section 101, Section 104). These numbers must be accurate.
* **Proper Names**: Ensure names like *B. Winchester*, *James M. Greig*, *Samuel L. Forgeus*, and *Eliza R. Snow* are spelled exactly as they appear in the image.
* **Archaic Spelling**: We use **Diplomatic Transcription**. If the original text says "connexion," we do not change it to "connection."

## 🛠 Usage & Data Format

The transcripts are not just raw text; they are structured data designed for modern usage.

* **Format**: JSON objects containing Markdown text.
* **Metadata**: Each entry includes the publication date, page number, issue, and volume.
* **Application**: This structure is optimized for AI RAG (Retrieval-Augmented Generation) systems, allowing LLMs to cite specific historical snippets without hallucination.

See the [Transcripts README](./transcripts/README.md) for detailed documentation on the data schema.

## 📝 License

Distributed under the MIT License. See [LICENSE](./LICENSE) for more information.

## 👤 Author

**Diego Lucero**

* GitHub: [@diegolucero23](https://github.com/diegolucero23)