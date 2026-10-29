# 02 — Cell Types & Modes

A notebook is a list of **cells**. Each cell is either **code** or **markdown**.

## Two modes

| Mode | Visual cue | What you do |
|------|------------|-------------|
| **Command mode** | Blue bar on the left edge | Navigate, insert/delete cells, change cell type |
| **Edit mode** | Green bar on the left edge | Type code or text inside a cell |

- Press `Escape` → command mode
- Press `Enter` → edit mode

## Essential keyboard shortcuts

### Command mode (press `Esc` first)

| Shortcut | Action |
|----------|--------|
| `Shift + Enter` | Run cell, move to next |
| `Ctrl + Enter` | Run cell, stay in same cell |
| `Alt + Enter` | Run cell, insert new cell below |
| `A` | Insert cell above |
| `B` | Insert cell below |
| `D`, `D` | Delete current cell (press D twice) |
| `M` | Convert cell to Markdown |
| `Y` | Convert cell to Code |
| `Z` | Undo last cell operation |
| `Ctrl + Shift + H` | Show all keyboard shortcuts |

### Edit mode (inside a cell)

| Shortcut | Action |
|----------|--------|
| `Tab` | Autocomplete |
| `Shift + Tab` | Show function signature / docstring |
| `Ctrl + /` | Toggle comment on selected lines |
| `Ctrl + ]` | Indent |
| `Ctrl + [` | Outdent |

> **`Shift + Enter`** is the shortcut you'll use most. Learn it first.

## Code cells

Run Python and display output below the cell.

```python
import numpy as np

data = np.random.randn(1000)
mean = data.mean()
std = data.std()

print(f"Mean: {mean:.4f}")
print(f"Std:  {std:.4f}")
```

**Expected output:**
```
Mean: 0.0032
Std:  0.9987
```

## Markdown cells

Render formatted text. Use headers, bold, italic, lists, tables, LaTeX math, and images.

Example markdown:

```markdown
# Experiment Results

Testing learning rate **0.01** on the MNIST subset.

The loss curve is shown below:

$$E = mc^2$$

| Model | Accuracy |
|-------|----------|
| Linear | 0.72 |
| Neural Net | 0.94 |
```

To convert a cell to markdown: press `Esc`, then `M`.  
To convert back to code: press `Esc`, then `Y`.

## Variables persist between cells

All cells share the same **kernel** (a Python process running in the background). If you define a variable in one cell, it's available in the next:

**Cell 1:**
```python
x = 10
```

**Cell 2:**
```python
print(x * 2)  # Output: 20
```

---

**Next:** [03 Magic Commands](./03-magic-commands.md)
