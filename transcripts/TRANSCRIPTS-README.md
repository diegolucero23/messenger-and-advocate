# Transcripts Documentation

This directory contains the machine-readable transcripts for the *Latter Day Saints' Messenger and Advocate* (Oct 1844 – 1846).

## 🗂 Data Organization

The transcripts are organized by **Processing Batch Date**.
* **Current Batch:** `jan-5-2026`

Each file represents a single page of the newspaper and is named to correspond with the scan (e.g., `page_001.json`).

## 🧠 Topics & Themes
Volume 1, Issue 1 (Oct 15, 1844) establishes the foundational arguments of the publication. The transcripts in this directory cover:

### 1. The Authority Controversy
* **The Keys of David:** Disputes over whether Joseph Smith or the Twelve held the "keys of David" versus the "keys of Elijah".
* **The First Presidency:** Arguments citing D&C Section 14 and Section 85 to prove that the Twelve act *under* the direction of the Presidency and cannot succeed it.

### 2. Moral & Theological Disputes
* **Spiritual Wifery:** Detailed denunciations of plural marriage, referred to in the text as "whoredoms," "Corruptions of the Daughters of Zion," and the "Doctrine of the Nicolaitans".
* **Secret Combinations:** Allegations that the Twelve were operating via "secret chambers" and "secret priesthoods" unknown to the general body of the Church.
* **The "Salt" of the Earth:** Arguments that the Church in Nauvoo had "lost its savor" and was fit only to be "trodden under foot of men" (citing D&C 101).

### 3. Historical Events
* **The Pittsburgh Conference:** Minutes from October 14, 1844, presided over by Richard Savery, where resolutions were passed to sustain Sidney Rigdon and reject the Twelve.
* **The "Bull" of J.E. Page:** References to an attack published by Apostle John E. Page and his subsequent departure from Pittsburgh.

## 💻 Technical Structure (JSON Schema)

The transcripts are formatted as JSON objects to support **AI RAG (Retrieval-Augmented Generation)** pipelines. This allows LLMs to ingest the history without losing the context of where the information came from.

### JSON Field Definitions
* `publication`: Always "Latter Day Saints' Messenger and Advocate".
* `volume`: The volume number (e.g., "1").
* `issue`: The issue number (e.g., "1").
* `date`: The publication date (e.g., "October 15, 1844").
* `page`: The specific page number from the original folio.
* `source_file`: The name of the original scan file.
* `content`: The full markdown transcription of the text.

### Example Entry (from Vol 1, Issue 1, Page 16)

```json
{
  "metadata": {
    "volume": "1",
    "issue": "1",
    "page": "16",
    "date": "October 15, 1844",
    "source_file": "page_016.json"
  },
  "content": "# PROSPECTUS\n\n## FOR The Latter Day Saints' MESSENGER AND ADVOCATE.\n\nAs much doubt still remains on the public mind, as to the true doctrine of the church of Jesus Christ of Latter Day Saints; the subscriber proposes to publish a paper in the city of Pittsburgh..."
}
```

## 🔍 Verification Guidelines for Volunteers

When verifying `transcripts` against the `scans`:

*    **Do not correct "archaic" spelling**: If the original text says "shewing" instead of "showing," keep it as "shewing."

*    **Preserve Italics**: Use markdown (*text*) to preserve emphasis, as this often indicates scriptural quotation or editorial stress.

*    **Check Headers**: Ensure the Volume and Issue in the metadata matches the header on the page.

If you find discrepancies, please open an Issue in the main repository tagged transcription-error.