# Jupyter Notebooks — Cheat Sheet

## Launch
```bash
pip install jupyterlab
jupyter lab
```

## Keyboard shortcuts

| Action | Shortcut |
|--------|----------|
| Run cell, move to next | `Shift + Enter` |
| Run cell, stay | `Ctrl + Enter` |
| Run cell, insert below | `Alt + Enter` |
| Insert cell above | `A` (command mode) |
| Insert cell below | `B` (command mode) |
| Delete cell | `D`, `D` (command mode) |
| To markdown | `M` (command mode) |
| To code | `Y` (command mode) |
| Undo cell | `Z` (command mode) |
| All shortcuts | `Ctrl + Shift + H` |
| Autocomplete | `Tab` (edit mode) |
| Function signature | `Shift + Tab` (edit mode) |
| Toggle comment | `Ctrl + /` (edit mode) |

*Press `Esc` for command mode, `Enter` for edit mode.*

## Magic commands

| Magic | What it does |
|-------|--------------|
| `%timeit` | Benchmark a line (many runs, average) |
| `%%time` | Time a whole cell (one run, wall time) |
| `%matplotlib inline` | Show plots inside the notebook |
| `!pip install pkg` | Install a package from shell |
| `%env VAR` | Show/set environment variable |
| `%who` | List variables in memory |

## Common traps & fixes

| Trap | Fix |
|------|-----|
| Out-of-order execution | Kernel > Restart & Run All |
| Hidden state (ghost variables) | Restart kernel regularly |
| Memory leaks | `del var; gc.collect()` or restart kernel |

## Notebooks vs Scripts

- **Notebooks:** Exploration, prototyping, visualization, teaching
- **Scripts (`.py`):** Production, pipelines, reusable utilities, scheduled tasks
- **Rule:** Explore in notebooks, ship in scripts

## File format

- `.ipynb` = JSON file with cells, outputs, metadata
- All interfaces (JupyterLab, Jupyter Notebook, VS Code) use the same format
