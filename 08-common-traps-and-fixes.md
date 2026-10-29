# 08 — Common Traps & Fixes

Notebooks are powerful but have real pitfalls. Here are the three most common ones.

## Trap 1: Out-of-order execution

**The problem:** You run cell 5, then cell 2, then cell 7. The notebook works on your machine because variables exist in memory, but it breaks when someone runs it top-to-bottom.

**Example of the bug:**

Cell 1:
```python
x = 5
```

Cell 2:
```python
y = x + 10  # Works if you ran Cell 1 first
```

If you run Cell 2 before Cell 1, you get `NameError: name 'x' is not defined`.

**The fix:** Before sharing, use **Kernel > Restart & Run All**. This clears memory and runs every cell in order, proving the notebook is self-contained.

---

## Trap 2: Hidden state

**The problem:** You delete a cell, but the variable it created still exists in the kernel's memory. The notebook looks clean, but it depends on a "ghost cell."

**Example:**
1. Run a cell that defines `model = train_model()`
2. Delete that cell
3. Run a later cell that uses `model` — it still works because `model` is in memory

**The fix:** **Restart the kernel regularly**, especially after deleting cells. Use **Kernel > Restart & Run All** to verify everything works from scratch.

---

## Trap 3: Memory leaks

**The problem:** You load a 4 GB dataset, train a model, then load another dataset. Nothing gets freed automatically. Memory usage keeps climbing until the kernel crashes.

**Example:**
```python
# Cell 1
data = pd.read_csv("huge_dataset.csv")  # 4 GB

# Cell 2
model = train(data)

# Cell 3
data2 = pd.read_csv("another_dataset.csv")  # Another 4 GB — `data` still in memory!
```

**The fix:**
```python
import gc

del data          # Remove the reference
gc.collect()      # Force garbage collection
```

Or simply **restart the kernel** between major tasks.

---

## Quick checklist before sharing a notebook

- [ ] Kernel > Restart & Run All (no errors)
- [ ] All outputs visible and correct
- # No `!pip install` cells that haven't been run
- # No variables depending on deleted cells
- # File paths are relative (not `C:\Users\...\data.csv`)

---

**Next:** [09 Key Terms Glossary](./09-key-terms-glossary.md)
