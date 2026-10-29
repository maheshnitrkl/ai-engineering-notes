# Jupyter Notebooks — Study Notes

**Source:** `ai-engineering-from-scratch` → Phase 0, Lesson 05 — Jupyter Notebooks  
**Type:** Build  
**Language:** Python  
**Estimated time:** ~30 minutes

> Notebooks are the lab bench of AI engineering. You prototype here, then move what works into production.

---

## 📚 Table of Contents

| Section | What's inside |
|---------|---------------|
| [01 Setup & Launch](./01-setup-and-launch.md) | Install JupyterLab / Jupyter Notebook / VS Code, start the server |
| [02 Cell Types & Modes](./02-cell-types-and-modes.md) | Code vs markdown cells, command vs edit mode, keyboard shortcuts |
| [03 Magic Commands](./03-magic-commands.md) | `%timeit`, `%%time`, `%matplotlib inline`, `!pip`, `%env` |
| [04 Rich Output & Display](./04-rich-output-and-display.md) | Inline plots, HTML tables, images, `display()` |
| [05 Kernel & State](./05-kernel-and-state.md) | How the kernel works, variable persistence, restarts |
| [06 Notebooks vs Scripts](./06-notebooks-vs-scripts.md) | When to use which, the "explore in notebooks, ship in scripts" rule |
| [07 Google Colab](./07-google-colab.md) | Free cloud notebooks with GPU, differences from local Jupyter |
| [08 Common Traps & Fixes](./08-common-traps-and-fixes.md) | Out-of-order execution, hidden state, memory leaks |
| [09 Key Terms Glossary](./09-key-terms-glossary.md) | Kernel, cell, magic command, `.ipynb` |
| [10 Practice Exercises](./10-practice-exercises.md) | Hands-on exercises with copy-paste code |
| [Quiz Review](./quiz-review.md) | Review of the lesson's quiz questions and answers |
| [Cheat Sheet](./cheat-sheet.md) | One-page quick reference |

---

## 🎯 Learning Objectives

By the end of these notes, you should be able to:

1. Install and launch JupyterLab, Jupyter Notebook, or VS Code with the Jupyter extension
2. Use magic commands (`%timeit`, `%%time`, `%matplotlib inline`) to benchmark and visualize inline
3. Distinguish when to use notebooks vs scripts and apply the "explore in notebooks, ship in scripts" workflow
4. Identify and avoid common notebook traps: out-of-order execution, hidden state, and memory leaks

---

## 🗂️ Folder Structure

```text
jupyter_notes/
├── README.md                    # This file — overview and navigation
├── cheat-sheet.md               # One-page quick reference
├── quiz-review.md               # Quiz questions & answers
├── 01-setup-and-launch.md       # Installation and startup
├── 02-cell-types-and-modes.md   # Cells, modes, shortcuts
├── 03-magic-commands.md         # Jupyter magics
├── 04-rich-output-and-display.md # Plots, tables, images
├── 05-kernel-and-state.md       # Kernel internals
├── 06-notebooks-vs-scripts.md   # Workflow guidance
├── 07-google-colab.md           # Colab cloud notebooks
├── 08-common-traps-and-fixes.md # Pitfalls and how to avoid them
├── 09-key-terms-glossary.md     # Terminology
└── 10-practice-exercises.md     # Hands-on exercises
```

---

## ⚠️ Important Note

These notes are **separate from your learning directory** (`ai-engineering-from-scratch`). Nothing in this folder touches your course repo. You can edit, delete, or experiment here freely.

Start with [01 Setup & Launch](./01-setup-and-launch.md) if you're new to Jupyter, or jump to the [Cheat Sheet](./cheat-sheet.md) for a quick reference.
