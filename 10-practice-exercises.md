# 10 — Practice Exercises

These are based on the exercises from the actual lesson. Copy the code blocks into your notebook and run them.

## Exercise 1: Benchmark list comprehension vs NumPy

**Goal:** Use `%timeit` to compare two ways of creating an array of 100,000 random numbers.

```python
import numpy as np
import random

# Method 1: List comprehension + list
%timeit [random.random() for _ in range(100000)]

# Method 2: NumPy
%timeit np.random.randn(100000)
```

**What to observe:** NumPy should be significantly faster. Record both timings in a markdown cell below the code.

---

## Exercise 2: Load CSV, display dataframe, plot chart

**Goal:** Create a notebook with both markdown and code cells that loads data, shows it, and visualizes it. Then verify with Restart & Run All.

```python
%matplotlib inline
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np

# Create sample data (no external CSV needed)
np.random.seed(42)
df = pd.DataFrame({
    "epoch": range(1, 21),
    "loss": np.exp(-np.linspace(0, 3, 20)) + np.random.normal(0, 0.02, 20),
    "accuracy": 1 - np.exp(-np.linspace(0, 3, 20)) + np.random.normal(0, 0.02, 20)
})

# Display the dataframe (rich HTML output)
df.head()

# Plot loss curve
plt.figure(figsize=(10, 4))
plt.plot(df["epoch"], df["loss"], marker="o", label="Loss")
plt.plot(df["epoch"], 1 - df["accuracy"], marker="s", label="Error rate")
plt.xlabel("Epoch")
plt.ylabel("Value")
plt.title("Training Metrics")
plt.legend()
plt.grid(True, alpha=0.3)
plt.show()
```

**Verification steps:**
1. Run all cells top-to-bottom
2. Use **Kernel > Restart & Run All**
3. Confirm no errors and the plot appears

---

## Exercise 3: Colab with GPU (optional)

**Goal:** Run code with a free GPU in Google Colab.

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Create a new notebook
3. Paste this code:

```python
import torch

print(f"PyTorch version: {torch.__version__}")
print(f"CUDA available: {torch.cuda.is_available()}")

if torch.cuda.is_available():
    print(f"GPU: {torch.cuda.get_device_name(0)}")
    
    # Quick GPU test
    x = torch.randn(1000, 1000).cuda()
    y = torch.randn(1000, 1000).cuda()
    z = x @ y
    print(f"Matrix multiply on GPU: shape={z.shape}")
else:
    print("Running on CPU — still works for this test")
```

4. Go to **Runtime > Change runtime type > T4 GPU**
5. Run the cell

---

**Next:** [Quiz Review](./quiz-review.md) or [Cheat Sheet](./cheat-sheet.md)
