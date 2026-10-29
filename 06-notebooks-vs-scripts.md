# 06 — Notebooks vs Scripts

## When to use which

| Use notebooks for | Use scripts (`.py`) for |
|-------------------|-------------------------|
| Exploring a dataset | Training pipelines |
| Prototyping a model | Reusable utilities |
| Visualizing results | Anything with `if __name__ == "__main__":` |
| Explaining your work | Code that runs on a schedule |
| Quick experiments | Production code |
| Course exercises | Packages and libraries |

## The golden rule

> **Explore in notebooks, ship in scripts.**

## Common AI workflow

1. **Explore data** in a notebook — load CSVs, check distributions, plot charts
2. **Prototype the model** in the notebook — try architectures, tune hyperparameters
3. **Move working code** to `.py` files — data loaders, model definitions, training loops
4. **Import those `.py` files** back into the notebook for further experiments

```text
Notebook (exploration)
    ↓  (code that works)
.py script (production)
    ↓  (import back)
Notebook (further experiments using the script)
```

## Why not use notebooks for everything?

- **Version control is harder** — `.ipynb` files are JSON and diff poorly in Git
- **Hidden state** — variables from out-of-order cells can break reproducibility
- **No `if __name__ == "__main__":`** — notebooks don't have a clean entry point
- **Harder to test** — you can't easily `import` a notebook and unit-test its functions

---

**Next:** [07 Google Colab](./07-google-colab.md)
