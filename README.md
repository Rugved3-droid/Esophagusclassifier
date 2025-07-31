
# 🧠 Esophagus Disease Classifier — YOLOv8n-Cls

This project features a trained YOLOv8n classification model that detects:

- **Normal Esophagus**
- **Esophagitis**
- **Barrett’s Esophagus**

The model is designed for image-based classification using endoscopic visuals to support early diagnosis.

---

## 📦 Model Details

- **Architecture**: YOLOv8n (classification mode)
- **Framework**: Ultralytics YOLOv8 + PyTorch
- **Input Size**: 224×224 pixels
- **Number of Classes**: 3 (`normal`, `esophagitis`, `barretts`)
- **Model Weights File**: `best.pt`

---

## ✅ Validation Performance

| Metric            | Score    |
|-------------------|----------|
| **Top-1 Accuracy** | 85.1%    |
| **Top-5 Accuracy** | 100%     |
| **Epochs Trained** | 10       |

> ⚠️ Model performance may vary on live or low-resolution inputs (e.g. webcams).

---

## 🔍 How to Use

```python
from ultralytics import YOLO

# Load model
model = YOLO('best.pt')

# Predict on an image
results = model('your_image.jpg')
results.print()
