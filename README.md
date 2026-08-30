# ANN Project — Iris Flower Classification using Artificial Neural Network

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Keras](https://img.shields.io/badge/Keras-ANN-red?logo=keras&logoColor=white)](https://keras.io/)
[![Accuracy](https://img.shields.io/badge/Accuracy-~100%25-brightgreen)](#results)

> A complete implementation of an **Artificial Neural Network (ANN)** for classifying Iris flower species using TensorFlow/Keras. The model achieves near-perfect accuracy on the classic Iris dataset.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Workflow](#training-workflow)
- [Results](#results)
- [File Structure](#file-structure)
- [Requirements](#requirements)
- [How to Run](#how-to-run)


---

## 🔍 Overview

This project demonstrates how to build, train, and evaluate a **multi-layer Artificial Neural Network** to solve a multi-class classification problem. The **Iris dataset** — one of the most well-known datasets in machine learning — serves as the benchmark. The goal is to classify a flower into one of three species based on four physical measurements.

---

## 📊 Dataset

**Source:** [Iris.csv](https://raw.githubusercontent.com/umang9369/ANN-Project/main/Iris.csv) (included in this repository)

The Iris dataset contains **150 samples** with **6 columns**:

| Column | Description |
|---|---|
| `Id` | Sample identifier |
| `SepalLengthCm` | Sepal length in centimetres |
| `SepalWidthCm` | Sepal width in centimetres |
| `PetalLengthCm` | Petal length in centimetres |
| `PetalWidthCm` | Petal width in centimetres |
| `Species` | Target class (Iris-setosa / Iris-versicolor / Iris-virginica) |

### Dataset Preview

![Dataset Preview — first 5 rows of the Iris CSV showing sepal/petal measurements and species labels](images/iris_dataset_preview.png)

**Class Distribution:** 50 samples per species (perfectly balanced).

---

## 🧠 Model Architecture

The network is a **fully connected feed-forward ANN** with the following structure:

```
Input Layer  →  4 neurons  (SepalLength, SepalWidth, PetalLength, PetalWidth)
Hidden Layer 1  →  Dense(64, activation='relu')
Hidden Layer 2  →  Dense(32, activation='relu')
Output Layer  →  Dense(3, activation='softmax')
```

| Layer | Units | Activation |
|---|---|---|
| Input | 4 | — |
| Hidden 1 | 64 | ReLU |
| Hidden 2 | 32 | ReLU |
| Output | 3 | Softmax |

- **Loss Function:** Categorical Cross-Entropy  
- **Optimizer:** Adam  
- **Metrics:** Accuracy  

---

## ⚙️ Training Workflow

1. **Load & Explore** — Read `Iris.csv`, inspect shape and class balance.
2. **Preprocessing** — Encode species labels with `LabelEncoder` + `to_categorical`; apply `StandardScaler` to features.
3. **Train/Test Split** — 80% training / 20% testing.
4. **Model Build** — Define sequential ANN using `keras.Sequential`.
5. **Training** — Fit model for **100 epochs** with validation split.
6. **Evaluation** — Plot accuracy/loss curves; compute final test accuracy.

---

## 📈 Results

The model converges rapidly and achieves **~100% accuracy** on the test set within ≈15 epochs.

### Accuracy Curve (Training vs. Validation)

![Model accuracy curve showing training (blue) and validation (orange) accuracy over 100 epochs — both reaching ~100%](images/accuracy_curve.png)

> **Blue line:** Training accuracy · **Orange line:** Validation accuracy  
> Both curves converge near **1.0 (100%)** from epoch ≈ 15 onwards, demonstrating excellent generalisation with no overfitting.

### Performance Summary

| Metric | Value |
|---|---|
| Test Accuracy | ≈ 100% |
| Epochs to converge | ~15 |
| Total training epochs | 100 |
| Dataset size | 150 samples |
| Train/Test split | 80% / 20% |

---

## 🗂️ File Structure

```
ANN-Project/
│
├── Iris.csv                 # Dataset (150 samples, 6 columns)
├── Untitled1.ipynb          # Main Jupyter Notebook (ANN implementation)
└── README.md                # Project documentation (this file)
```

> **Note:** You must create an `images/` folder in the repository and upload `accuracy_curve.png` and `iris_dataset_preview.png` for the images above to render correctly on GitHub.

---

## 🔧 Requirements

Install all dependencies with:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow keras jupyter
```

| Library | Purpose |
|---|---|
| `numpy` | Numerical computation |
| `pandas` | Data loading & manipulation |
| `matplotlib` | Plotting accuracy/loss curves |
| `scikit-learn` | Preprocessing, train-test split |
| `tensorflow` / `keras` | Building & training the ANN |
| `jupyter` | Running the notebook |

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/umang9369/ANN-Project.git
cd ANN-Project
```

### 2. Install dependencies

```bash
pip install numpy pandas matplotlib scikit-learn tensorflow keras
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook Untitled1.ipynb
```

### 4. Run all cells

Inside the notebook, go to **Kernel → Restart & Run All** to reproduce the full training pipeline and output plots.

---
<p align="center">
  Made with ❤️ by <a href="https://github.com/umang9369">umang9369</a>
</p>
