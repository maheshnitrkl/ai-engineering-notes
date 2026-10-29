# 07 — Google Colab

**Colab** is a free Jupyter notebook running in the cloud. No local installation required.

## How to use Colab

1. Go to [colab.research.google.com](https://colab.research.google.com)
2. Upload any `.ipynb` file from this course
3. Go to **Runtime > Change runtime type** > select **T4 GPU** (free)
4. Run cells normally

## Colab vs Local Jupyter

| Feature | Local Jupyter | Google Colab |
|---------|--------------|--------------|
| Setup required | Yes (`pip install jupyterlab`) | None |
| GPU | Only if you have one | Free T4 GPU available |
| File persistence | Yes (your local disk) | No — files disappear when session ends |
| Pre-installed libraries | You install them | numpy, pandas, matplotlib, torch, tensorflow, sklearn |
| Session timeout | Never | ~90 minutes of inactivity (free tier) |

## Colab-specific code

**Upload/download files:**
```python
from google.colab import files
uploaded = files.upload()  # Opens file picker
files.download("output.png")  # Downloads file to your computer
```

**Mount Google Drive for persistent storage:**
```python
from google.colab import drive
drive.mount('/content/drive')
# Files at /content/drive/MyDrive/ persist between sessions
```

**Check GPU availability:**
```python
import torch
print(f"CUDA available: {torch.cuda.is_available()}")
if torch.cuda.is_available():
    print(f"GPU: {torch.cuda.get_device_name(0)}")
```

---

**Next:** [08 Common Traps & Fixes](./08-common-traps-and-fixes.md)
