# Contributing to the Messenger and Advocate Project

First off, thank you for considering contributing! This project relies on volunteers to ensure the history of the 1844 succession crisis is preserved accurately.

We welcome contributors of all skill levels. You do not need to be a coder to help—you just need sharp eyes and attention to detail.

## 🚦 The Workflow: How to Verify a Page

We use a "Claim System" to prevent two people from working on the same page at the same time.

### Step 1: Find a Task
Go to the **[Issues Tab]** in this repository. Look for issues tagged `verification-needed`.
* **Action:** When you find a page you want to work on, leave a comment on that Issue saying: *"I am working on this."*

### Step 2: Prepare Your Workspace
If you are new to GitHub, here is the safest way to work:

1.  **Fork** this repository (click the "Fork" button in the top right).
2.  **Clone** your fork to your computer (or use the GitHub Web Editor by pressing `.` on your keyboard while viewing the repo).
3.  **Create a Branch**: Name it something specific, like `verify-vol1-issue1`.
    ```bash
    git checkout -b verify-vol1-issue1
    ```

### Step 3: Verify and Edit
1.  Open the Scan (image) and the Transcript (JSON) side-by-side.
2.  Follow the rules in the [Style Guide](./STYLE_GUIDE.md).
3.  **Critically:** Ensure you do not break the JSON syntax (watch out for unescaped quotes!).

### Step 4: Submit Your Work
1.  **Commit** your changes:
    ```bash
    git commit -m "Verified Vol 1, Issue 1, Page 15"
    ```
2.  **Push** to your fork:
    ```bash
    git push origin verify-vol1-issue1
    ```
3.  **Open a Pull Request (PR):**
    * Go to the main repository.
    * Click "Compare & Pull Request."
    * In the description, link the Issue you claimed (e.g., *"Closes #123"*).

---

## 🐞 Reporting Errors
If you find a historical inconsistency or a major file error but don't feel comfortable fixing it yourself:
1.  Open a **New Issue**.
2.  Tag it with `transcription-error` or `question`.
3.  Describe the problem (e.g., *"On Page 4, the text says 'Joseph' but the scan looks like 'Hyrum'."*).

## 💬 Community & Etiquette
* **Be Respectful:** We are dealing with sensitive historical and religious topics. Keep discussions focused on the text accuracy, not theological debate.
* **Ask Questions:** There are no stupid questions. If you can't read a word, ask in the Discussions tab!