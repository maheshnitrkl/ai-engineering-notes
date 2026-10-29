# 01 — Setup & Launch

Three interfaces read and write the same `.ipynb` file format. Pick the one you prefer.

| Interface | Install command | Launch command | Best for |
|-----------|-----------------|----------------|----------|
| **JupyterLab** | `pip install jupyterlab` | `jupyter lab` | Full IDE experience — multiple tabs, file browser, terminal, extensions |
| **Jupyter Notebook** | `pip install notebook` | `jupyter notebook` | Simple, lightweight, one notebook at a time |
| **VS Code** | Install "Jupyter" extension from the marketplace | Open a `.ipynb` file in VS Code | Already in your editor, git integration, debugging |

## Step-by-step (local install)

```bash
# 1. Install JupyterLab
pip install jupyterlab

# 2. Launch it (opens in your browser)
jupyter lab
```

When you run `jupyter lab`, a new browser tab opens at `http://localhost:8888/lab`. You'll see a file browser on the left and can create new notebooks (`.ipynb`) from the launcher.

## Step-by-step (VS Code)

1. Install the **Jupyter** extension (by Microsoft) in VS Code.
2. Create a new file ending in `.ipynb` (e.g., `my-notebook.ipynb`).
3. VS Code will detect it and offer a "Select Kernel" button — choose your Python environment.
4. Code cells appear with a **Run** button above them.

## Verify it works

Create a new notebook and paste this into a code cell:

```python
print("Jupyter is working!")
```

Run it (Shift+Enter). You should see the output appear directly below the cell.

## What is an `.ipynb` file?

It's a **JSON file** that contains:
- Cells (code and markdown)
- Outputs (text, plots, HTML)
- Metadata (kernelspec, language info)

You can open it in any text editor to see the raw JSON, but you should edit it through JupyterLab, Jupyter Notebook, or VS Code.

---

**Next:** [02 Cell Types & Modes](./02-cell-types-and-modes.md)
