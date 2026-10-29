# 05 — Kernel & State

## What is the kernel?

The **kernel** is a separate Python process running in the background. When you run a cell:

1. The notebook UI sends the code to the kernel
2. The kernel executes it
3. The kernel sends the result back to the UI
4. All output appears below the cell

```text
Notebook UI  <-->  Kernel (Python process)
                        |
                        v
              Keeps variables in memory
                        |
                        v
              Runs cells in whatever order you click
                        |
                        v
              Dies when you restart it
```

## Variable persistence

All cells share the same kernel, so **variables persist between cells**.

**Cell 1:**
```python
learning_rate = 0.01
epochs = 10
```

**Cell 2 (runs later):**
```python
print(f"Training for {epochs} epochs at lr={learning_rate}")
# Output: Training for 10 epochs at lr=0.01
```

## Restarting the kernel

| Action | What happens |
|--------|--------------|
| **Restart** | Clears all variables; code stays in cells |
| **Restart & Run All** | Clears variables, then runs every cell top-to-bottom |
| **Re-run all cells** | Keeps variables, runs every cell again |

**When to restart:**
- After installing a new package with `!pip install`
- When you suspect hidden state is causing bugs
- Before sharing a notebook with someone else
- When memory usage is high

## State inspection

See what's currently in memory:

```python
# List all variables in the current namespace
%who

# List with types
%who_ls

# Detailed info
%whos
```

---

**Next:** [06 Notebooks vs Scripts](./06-notebooks-vs-scripts.md)
