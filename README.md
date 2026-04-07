<h1 align="center">🧠 CIFAR-10 Image Classification</h1>

<p align="center">
  Deep Learning project comparing custom CNN vs ResNet50 for image classification 🚀
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Deep Learning-CNN-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Transfer Learning-ResNet50-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Dataset-CIFAR--10-orange?style=for-the-badge" />
</p>

---

## 🎯 Project Overview

<p align="center">
This project focuses on image classification using the CIFAR-10 dataset by comparing a custom-built CNN model (<b>SimCNN</b>) with a pretrained <b>ResNet50</b> architecture.
</p>

<p align="center">
The objective is to evaluate performance, training efficiency, and generalization capability across different architectures and hyperparameter configurations.
</p>

---

## 🎓 Project Context

<p align="center">
This project was developed as part of a <b>Deep Learning course</b> during my Master’s in Data Science at NYIT, demonstrating practical implementation of CNNs and transfer learning techniques.
</p>

---

## 🧾 Dataset

<p align="center">

| Attribute           | Details |
|--------------------|--------|
| Dataset            | CIFAR-10 |
| Type               | Image Classification |
| Classes            | 10 categories |
| Image Size         | 32 × 32 pixels |
| Training Samples   | 50,000 |
| Test Samples       | 10,000 |

</p>

---

## 🔧 Models & Architectures

### 🔹 SimCNN (Custom CNN)

- 3 Convolution + MaxPooling layers  
- Fully connected dense layers  
- Dropout for regularization  
- Optimizer: Adam  

📊 **Performance**
- Accuracy: **68.75%**
- Loss: **0.9260**

---

### 🔹 ResNet50 (Pretrained - ImageNet)

#### ✅ Default Configuration (ResNet50-01)
- Batch Size: 32  
- Epochs: 25  

📊 **Performance**
- Accuracy: **95.93%**
- Loss: **0.1683**

---

#### ⚙️ Custom Configuration (ResNet50-02)
- Batch Size: 64  
- Epochs: 30  

📊 **Performance**
- Accuracy: **94.67%**
- Loss: **0.2565**

---

## 📊 Model Comparison

<p align="center">

| Model         | Batch Size | Epochs | Accuracy | Loss   |
|--------------|------------|--------|----------|--------|
| SimCNN       | 32         | 25     | 68.75%   | 0.9260 |
| ResNet50-01  | 32         | 25     | **95.93%** | 0.1683 |
| ResNet50-02  | 64         | 30     | 94.67%   | 0.2565 |

</p>

---

## 📌 Key Insights

<ul align="center">
<li>ResNet50 significantly outperforms the custom CNN</li>
<li>Transfer learning improves generalization on small datasets</li>
<li>Increasing batch size improves training speed but not accuracy</li>
<li>Custom CNN struggles with complex feature extraction</li>
</ul>

---

## ⚙️ Hyperparameter Justification

- **Batch Size = 64** → Faster training, stable gradients  
- **Epochs = 30** → Better feature learning  
- **Learning Rate = 0.005** → Stable convergence  
- **Steps/Epoch ≈ 782** → Ensures full dataset coverage  

---

## 🧱 Architecture

<p align="center">
<b>Image → CNN / ResNet50 → Feature Extraction → Classification → Output</b>
</p>

---

## 📂 Project Structure

```bash
cifar10-image-classification/
│
├── SimCNN.ipynb
├── ResNet50_01.ipynb
├── ResNet50_02.ipynb
├── dataset/
└── README.md
