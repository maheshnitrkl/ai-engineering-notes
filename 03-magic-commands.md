# 03 — Magic Commands

Magic commands are **Jupyter-specific**, not Python. They start with:

- `%` — **line magic** (affects one line)
- `%%` — **cell magic** (affects the whole cell)

---

## `%timeit` — Microbenchmarking

Runs the code many times and reports the average. Best for small, fast operations.

```python
import numpy as np

%timeit np.random.randn(10000)
```

**Typical output:**
```
45.2 µs ± 1.3 µs per loop (mean ± std. dev. of 7 runs, 10000 loops each)
```

**When to use:** Comparing two ways of doing the same small task (e.g., list comprehension vs. NumPy).

---

## `%%time` — Wall clock timing

Runs the cell once and reports total elapsed time. Best for longer operations like model training.

```python
%%time
# Simulate a training loop
import time
time.sleep(2)
print("Done")
```

**Typical output:**
```
Done
Wall time: 2.01 s
```

**Difference from `%timeit`:**
- `%timeit` → many runs, statistical average (microbenchmarks)
- `%%time` → single run, wall time (training runs, scripts)

---

## `%matplotlib inline` — Inline plots

Makes plots render directly inside the notebook, below the code cell.

```python
%matplotlib inline

import matplotlib.pyplot as plt

plt.figure(figsize=(8, 4))
plt.plot([1, 2, 3, 4], [1, 4, 2, 3])
plt.title("Inline Plot")
plt.show()
```

The plot appears immediately under the cell. Without this, plots may open in a separate window or not appear at all.

---

## `!pip install` — Install packages without leaving the notebook

The `!` prefix runs any shell command.

```python
!pip install scikit-learn
```

You can also `!ls`, `!pwd`, `!curl`, etc.

> **Tip:** After installing, you may need to restart the kernel for the new package to be importable.

---

## `%env` — Check environment variables

```python
%env CUDA_VISIBLE_DEVICES
```

To set an environment variable inside the notebook:

```python
%env CUDA_VISIBLE_DEVICES=0
```

---

## Quick reference table

| Magic | Type | Purpose | Example |
|-------|------|---------|---------|
| `%timeit` | Line | Benchmark small code snippets | `%timeit sum(range(1000))` |
| `%%time` | Cell | Time a whole cell once | `%%time` then training code |
| `%matplotlib inline` | Line | Render plots inline | `%matplotlib inline` |
| `!pip install` | Shell | Install Python packages | `!pip install pandas` |
| `%env` | Line | Show/set env vars | `%env CUDA_VISIBLE_DEVICES` |

---

**Next:** [04 Rich Output & Display](./04-rich-output-and-display.md)
