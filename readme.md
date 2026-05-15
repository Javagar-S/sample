<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00b09b,100:96c93d&height=200&section=header&text=CropGuard&fontSize=40&fontColor=ffffff"/>
</p>

<div align="center">

# 🌱 CropGuard | AI-Powered Crop Disease Detection

**Deep learning-based web application for real-time plant disease diagnosis and agricultural insights.**

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue?style=for-the-badge&logo=python)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange?style=for-the-badge&logo=tensorflow)](https://www.tensorflow.org/)
[![Flask](https://img.shields.io/badge/Flask-WebApp-black?style=for-the-badge&logo=flask)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)]()

</div>

---

## 🚀 Live Demo
> *(Add after deployment)*  
🌐 https://your-app-link.com  

---

## 📖 Overview

**CropGuard** is an end-to-end deep learning system that detects crop diseases from leaf images using a fine-tuned **EfficientNetB0** model.

It combines:
- Image classification  
- Test-Time Augmentation (TTA)  
- Confidence-based filtering  
- Real-time weather context  

to deliver **accurate and reliable agricultural diagnostics**.

---

## 📸 Screenshots

<div align="center">

### 🏠 Home Page
<img src="https://github.com/Javagar-S/crop-disease-prediction-ml/blob/main/images/home%20page.png?raw=true" width="80%">

### 📊 Prediction Result
<img src="https://github.com/Javagar-S/crop-disease-prediction-ml/blob/main/images/result%20page.png?raw=true" width="80%">

### 📄 Diagnostic Report
<img src="https://github.com/Javagar-S/crop-disease-prediction-ml/blob/main/images/report.png?raw=true" width="80%">

</div>

---

## ✨ Key Features

- 🧠 **Deep Learning Model** – EfficientNetB0 fine-tuned for plant disease detection  
- 🔍 **Test-Time Augmentation (TTA)** – Improves prediction stability  
- 🚫 **Confidence Filtering** – Rejects low-quality or irrelevant images  
- 🌦️ **Weather Integration** – Adds environmental context (temperature & humidity)  
- 🎙️ **Voice Assistance** – Reads diagnosis using Web Speech API  
- 📄 **Report Generation** – Clean, printable disease reports  

---

## 🏗️ Model Architecture

- **Base Model:** EfficientNetB0 (ImageNet pretrained)  
- **Custom Layers:**
  - GlobalAveragePooling2D  
  - BatchNormalization  
  - Dense (256, ReLU)  
  - Dropout (0.2, 0.3)  
  - Softmax (15 classes)

### Training Strategy
- Phase 1: Train classification head  
- Phase 2: Fine-tune top layers of base model (`lr = 1e-5`)  

---

## 📊 Performance Highlights

- 📈 Dataset: ~20,600 images (PlantVillage)  
- 🎯 Classes: 15  
- ⚖️ Class imbalance handled using `class_weight`  
- 🔍 TTA improves prediction consistency  
- ✅ Confidence threshold: **75%+**

---

## 🛠️ Tech Stack

### Machine Learning
- TensorFlow / Keras  
- NumPy, Scikit-learn  

### Backend
- Flask  
- Werkzeug  

### Frontend
- HTML, CSS, JavaScript  
- Bootstrap 5  

---

## 📂 Project Structure

```text
crop-disease-prediction-ml/
│
├── data/
├── models/
├── src/
├── web/
├── config.py
├── split_dataset.py
├── requirements.txt
└── README.md
