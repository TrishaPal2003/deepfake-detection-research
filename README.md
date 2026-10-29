---
license: mit
task_categories:
- image-classification
language:
- en
tags:
- deepfake
- face-swap
- detection
- computer-vision
- insightface
size_categories:
- 10K<n<100K
---

# DeepGuard Deepfake Dataset

A paired deepfake dataset for training and benchmarking deepfake detection models.
Generated as part of the DeepGuard AI Project (2026).

![Total Downloads](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fhuggingface.co%2Fapi%2Fdatasets%2FSowaiba01%2FDeepfake%3Fexpand%3DdownloadsAllTime&query=%24.downloadsAllTime&label=Total%20Downloads&color=success&style=for-the-badge)

**📥 2,301+ all-time downloads**
## Dataset Statistics
- **Fake images:** 5426 (face-swapped using InsightFace inswapper_128)
- **Real images:** 5426 (original paired faces)
- **Total:** 10852 images
- **Format:** JPEG, high quality (95%)
- **Generation method:** InsightFace inswapper_128 (ONNX runtime)

## Why This Dataset is Unique
- **Paired structure:** Every fake has a matching real image of the same target person
- **Modern method:** inswapper_128 powers most 2024-2026 real-world deepfake apps
- **Traceable metadata:** Source identity, target face, and method per image
- **Open access:** No sign-up required, instant `load_dataset()` access


## Quick Start
```python
from datasets import load_dataset
ds = load_dataset('Sowaiba01/Deepfake')
```

## Detection Model
Trained EfficientNet-B4 detection model also available:
```python
from huggingface_hub import hf_hub_download
model_path = hf_hub_download('Sowaiba01/deepguard-ai', 'efficientnet_b4_deepguard.pth')
```
Validation accuracy: **91.54%** on 140K Real & Fake Faces dataset.

## Citation
```
@dataset{deepguard2026,
  author = {Arshad, Sowaiba},
  title  = {DeepGuard Deepfake Dataset},
  year   = {2026},
  url    = {https://huggingface.co/datasets/Sowaiba01/Deepfake}
}
```
