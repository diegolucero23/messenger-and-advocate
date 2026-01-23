# Transcripts Documentation

This directory contains the transcribed newspaper issues for the *Latter Day Saints' Messenger and Advocate* (Oct 1844 – 1846).

## 🗂 Data Organization

The transcripts are organized by "batch date" to track OCR improvements over time.
* **Current Batch:** `jan-5-2026`

## 🧠 Topics Covered
These documents cover a wide range of theological and historical controversies from the 1844 succession crisis, including:
* Brigham Young and the Quorum of the 12
* Spiritual Wifery vs. Monogamy
* The Law of the Church
* The excommunication of Sidney Rigdon
* Investigations into the alleged crimes of the Twelve
* Adultery and Secret Priesthoods
* The Cochranites influence
* William Smith's testimony

## 💻 Technical Structure (JSON + Markdown)

Unlike standard text files, these transcripts are recorded in a structured markdown embedded within **JSON format**. This design choice ensures the data is machine-readable and ready for high-level applications.

### Why this format?
1.  **Searchability:** Search engines (Google, DuckDuckGo) can easily parse structured metadata.
2.  **AI & RAG Readiness:** Academic research increasingly relies on AI Large Language Models (LLMs). By providing structured JSON, we enable **RAG (Retrieval-Augmented Generation)** pipelines to ingest this history. This allows an AI to answer questions about the text while accurately citing the specific *Volume*, *Issue*, and *Page*, significantly reducing "hallucinations."

### Data Schema
Each transcript file contains objects with the following properties:

```json
{
  "publication": "Latter Day Saints' Messenger and Advocate",
  "volume": "1",
  "issue": "1",
  "date": "October 15, 1844",
  "page": "1",
  "content": "# Header\n\nThis is the markdown transcription of the text..."
}
```

## 🔍 Verification

We are currently verifying the data in the `jan-5-2026` folder. If you find discrepancies between the JSON content and the source scans, please submit an issue in the main repository.