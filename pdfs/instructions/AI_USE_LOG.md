# AI-Use Log — DS5006 Team Project

**Team name:** _______________
**Members:** _______________

Keep this file in the root of your submission. Add an entry **each time** an AI tool
contributes something you keep (code, text, an idea, a fix). Log as you go — do not
reconstruct entries at the end. Any logged interaction may be discussed in the oral exam.

You do not need to log: spell-checkers, IDE autocomplete of single identifiers,
or searches whose results you did not use.

---

## Summary

| Tool (name + version/model) | Members who used it | Main purposes |
|---|---|---|
| e.g. ChatGPT (GPT-x) | A, C | debugging, plotting code |
| | | |

---

## Entries

Copy the block below for each entry. Number entries consecutively.

### Entry 001

- **Date:** YYYY-MM-DD
- **Member:** 
- **Tool:** 
- **Purpose:** (debugging / code generation / explaining a concept / refining a question / language editing / other)
- **Prompt:** Paste the prompt(s) verbatim. For long conversations, paste the key prompts
  and give a shared-chat link or an exported transcript file in `ai_transcripts/`.
- **Chat link / transcript file:** 
- **What we used:** What was kept from the output, and where it now lives
  (file + function, or report section).
- **What we changed:** How the output was modified before use.
- **How we verified it:** Tests run, results checked against expectations,
  documentation consulted, etc. "It ran" is not verification.

---

### Example (delete before submitting)

- **Date:** 2026-10-14
- **Member:** Member Two
- **Tool:** Claude
- **Purpose:** code generation
- **Prompt:** "Write a PyTorch function that appends k columns of i.i.d. standard
  normal noise to a feature matrix, using a fixed seed, and returns the new matrix."
- **Chat link / transcript file:** ai_transcripts/entry_001.txt
- **What we used:** The function body, now `add_noise_features()` in `code/data_utils.py`.
- **What we changed:** Switched from `torch.randn` to NumPy's `default_rng` so the
  noise is identical across the MLP and XGBoost pipelines; added a check that the
  original columns are unchanged.
- **How we verified it:** Unit test confirming output shape (n, d+k), that the first
  d columns equal the input, and that two calls with the same seed return identical
  noise; sample mean/std of the added columns ≈ 0/1 for n = 10,000.

---

## Declaration

We confirm that this log records all use of AI tools in this project, that every
member has read it, and that each of us can explain any work listed here.

| Member | Roll No. | Initials |
|---|---|---|
| | | |
| | | |
| | | |
| | | |
