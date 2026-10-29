# 09 — Key Terms Glossary

| Term | What people say | What it actually means |
|------|----------------|------------------------|
| **Kernel** | "The thing running my code" | A separate Python process that executes cells and keeps variables in memory. All cells in a notebook share the same kernel. |
| **Cell** | "A code block" | An independently runnable unit in a notebook. Either code (Python) or markdown (formatted text). |
| **Magic command** | "Jupyter tricks" | Special commands prefixed with `%` (line magic) or `%%` (cell magic) that control the notebook environment. Examples: `%timeit`, `%%time`, `%matplotlib inline`. |
| **`.ipynb`** | "Notebook file" | A JSON file containing cells, outputs, and metadata. Stands for **IPython Notebook**. Can be opened in JupyterLab, Jupyter Notebook, or VS Code. |
| **Command mode** | "Navigation mode" | Cell-level navigation (blue sidebar). Press `Esc` to enter. Use `A`, `B`, `D D`, `M`, `Y`, `Shift+Enter`. |
| **Edit mode** | "Typing mode" | Cell content editing (green sidebar). Press `Enter` to enter. Use `Tab`, `Shift+Tab`, `Ctrl+/`. |
| **Inline output** | "Output below the cell" | Results (text, plots, tables) displayed directly underneath the code cell that produced them. |
| **Restart & Run All** | "Reset everything" | Clears the kernel's memory and runs every cell top-to-bottom. Used to verify reproducibility. |

---

**Next:** [10 Practice Exercises](./10-practice-exercises.md)
