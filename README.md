# 🐱🐶 Cat vs Dog Image Classifier — CNN & MobileNetV2

![Python](https://img.shields.io/badge/Python-3.9+-blue?style=flat-square&logo=python)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=flat-square&logo=tensorflow)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red?style=flat-square&logo=keras)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=flat-square&logo=opencv)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

A complete binary image classification system built using Deep Learning on 10,000 real images. Two models are trained and compared a Custom CNN built from scratch and MobileNetV2 Transfer Learning.

---

## 🎯 Features

- ✅ Custom CNN built from scratch (3 Conv Blocks)
- ✅ MobileNetV2 Transfer Learning + Fine-Tuning
- ✅ Data Augmentation pipeline (flip, rotate, zoom, contrast)
- ✅ Batch Normalization & Dropout to prevent overfitting
- ✅ Full evaluation — ROC Curve, Confusion Matrix, AUC
- ✅ predict_single() — classify any new image instantly
- ✅ Auto train/val/test split (70% / 15% / 15%)

---

## 📊 Results

| Model | Test Accuracy | AUC Score |
|---|---|---|
| Custom CNN | ~88–92% | ~0.94 |
| MobileNetV2 | ~96–98% | ~0.99 |

---

## 🗂️ Dataset Structure

```
dogs-vs-cats/
├── cat/     ← 5,000 cat images
└── dogs/    ← 5,000 dog images
```

Download dataset: [Kaggle — Dogs vs Cats](https://www.kaggle.com/c/dogs-vs-cats)

---

## 🛠️ Tech Stack

- Python 3.9+
- TensorFlow 2.x
- Keras
- OpenCV
- Scikit-learn
- Matplotlib
- NumPy
- Pillow

---

## ⚡ Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/engineerzainabbas/cat-vs-dog-classifier.git
cd cat-vs-dog-classifier
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add your dataset
Place your dataset folder in the same directory as the notebook:
```
cat-vs-dog-classifier/
├── cat_vs_dog_local.ipynb
├── requirements.txt
└── dogs-vs-cats/
    ├── cat/
    └── dogs/
```

### 4. Run the notebook
Open `cat_vs_dog_local.ipynb` in Jupyter Notebook and run all cells.

### 5. Predict on any image
```python
predict_single('dogs-vs-cats/cat/cat.1.jpg')
predict_single('dogs-vs-cats/dogs/dog.1.jpg')
predict_single('path/to/your/image.jpg')
```

---

## 📂 Project Structure

```
cat-vs-dog-classifier/
│
├── cat_vs_dog_local.ipynb     ← Main notebook
├── requirements.txt            ← Dependencies
├── README.md                   ← This file
└── results/                    ← Output charts
    ├── sample_images.png
    ├── augmentation_examples.png
    ├── confusion_matrices.png
    ├── roc_curve.png
    ├── model_comparison.png
    └── sample_predictions.png
```

---

## 🔬 Model Architectures

### Custom CNN
```
Input (128×128×3)
→ Conv2D(32) + BatchNorm + MaxPool + Dropout
→ Conv2D(64) + BatchNorm + MaxPool + Dropout
→ Conv2D(128) + BatchNorm + MaxPool + Dropout
→ GlobalAveragePooling
→ Dense(256) + Dropout
→ Dense(1, sigmoid)
```

### MobileNetV2 Transfer Learning
```
MobileNetV2 (pretrained ImageNet, frozen)
→ GlobalAveragePooling
→ Dense(128) + Dropout
→ Dense(1, sigmoid)
--- Fine-tuning: last 30 layers unfrozen ---
```

---

## ⚙️ Training Configuration

| Parameter | Value |
|---|---|
| Image Size | 128×128 |
| Batch Size | 16 |
| Optimizer | Adam |
| Loss | Binary Crossentropy |
| Epochs | 50 (Early Stopping) |
| Augmentation | Flip, Rotate, Zoom, Contrast |

---

## 🏭 Real-World Applications

- 🐾 **Pet recognition** systems
- 🔬 **Medical imaging** classification
- 🏭 **Manufacturing** defect detection
- 🛒 **E-commerce** product categorization
- 🔒 **Security** camera systems

---

## 💼 Need a Custom Solution?

If you need a custom image classification system built for your specific dataset or use case:

- 🎯 Custom model training on your images
- 🚀 Deployment as web application (Streamlit/Flask)
- 📊 Multi-class classification
- 🔧 Integration with your existing system

📧 engineerzainabbas@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/engineerzainabbas/)

---

## 👤 Author

**Zain Abbas**
- 🎓 Computer Engineering
- 💼 AI & Machine Learning Engineer
- 🔗 [LinkedIn](https://www.linkedin.com/in/engineerzainabbas/)
- 📧 engineerzainabbas@gmail.com

---

## 📄 License

This project is licensed under the MIT License.
