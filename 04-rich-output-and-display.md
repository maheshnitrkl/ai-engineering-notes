# 04 — Rich Output & Display

Notebooks auto-display the **last expression** in a cell. You don't need `print()` for the final value.

## Auto-display example

```python
import pandas as pd

df = pd.DataFrame({
    "model": ["Linear", "Random Forest", "Neural Net"],
    "accuracy": [0.72, 0.89, 0.94],
    "training_time": [0.1, 2.3, 45.6]
})

df  # Renders as a formatted HTML table, not a text dump
```

**Output:** A nicely formatted HTML table with alternating row colors and sortable columns (in JupyterLab).

---

## Inline plots

With `%matplotlib inline` enabled, `plt.show()` renders inside the notebook.

```python
%matplotlib inline
import matplotlib.pyplot as plt

plt.figure(figsize=(8, 4))
plt.plot([1, 2, 3, 4], [1, 4, 2, 3])
plt.title("Training Loss Over Epochs")
plt.xlabel("Epoch")
plt.ylabel("Loss")
plt.grid(True, alpha=0.3)
plt.show()
```

**Output:** The chart appears directly below the cell.

---

## Displaying images

Use `IPython.display` to show images inline.

```python
from IPython.display import Image, display

# From a local file
display(Image(filename="architecture.png", width=600))

# From a URL
display(Image(url="https://example.com/diagram.png"))
```

---

## Rich display objects

You can display HTML, Markdown, LaTeX, audio, video, and more:

```python
from IPython.display import HTML, Markdown, Latex, Audio

HTML("<div style='color:red;'>Warning: high loss detected</div>")
Markdown("## Section Header\nThis is **bold** and this is *italic*.")
Latex(r"\int_{0}^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2}")
```

---

## Why this matters for AI

You see the **data, the plot, and the code together** in one place. This rapid feedback loop is why notebooks dominate AI research and prototyping.

---

**Next:** [05 Kernel & State](./05-kernel-and-state.md)
