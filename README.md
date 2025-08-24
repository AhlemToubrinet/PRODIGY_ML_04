# PRODIGY_ML_04: Hand Gesture Recognition using CNN

## ✋ Project Overview

This project implements a **Convolutional Neural Network (CNN)** model to classify different **hand gestures** using the [LeapGestRecog dataset](https://www.kaggle.com/gti-upm/leapgestrecog). It was developed as part of the **Prodigy InfoTech machine learning internship**, demonstrating how deep learning can be applied for gesture-based human-computer interaction.

The model processes grayscale images of hand gestures and classifies them into one of five gesture classes, enabling the foundation for intuitive gesture-controlled systems.

---

## 💡 Features

- **Data Handling**:
  - Data collected from 10 subjects performing 10 different gestures
  - Subset of 5 gesture classes used for classification
  - Dataset organized into folders, renamed and structured for training

- **Data Preprocessing**:
  - Image loading using OpenCV
  - Grayscale conversion
  - Resizing to 100x100 for memory efficiency
  - Label encoding and normalization

- **Model Architecture**:
  - Convolutional layers with ReLU activation
  - Batch Normalization & MaxPooling
  - Dropout regularization
  - Dense layers with softmax output for multi-class classification

- **Training Strategy**:
  - Early stopping to prevent overfitting
  - Training-validation split (80/20)
  - Performance metrics tracking (accuracy, loss)

- **Evaluation & Visualization**:
  - Test set evaluation
  - Accuracy and loss curves

---

## 📁 Dataset

The dataset used is the [LeapGestRecog dataset](https://www.kaggle.com/gti-upm/leapgestrecog), which contains:

- 10 gesture classes captured from 10 users
- Each gesture performed multiple times
- Subset used in this project:  
  - `01_l`  
  - `02_thumb`  
  - `03_index`  
  - `04_ok`  
  - `05_c`

Each class is stored in a dedicated folder for training.

---

## 🧠 Model Summary

```text
Conv2D (32 filters, 3x3) → ReLU → BatchNorm → MaxPooling → Dropout  
Conv2D (64 filters, 3x3) → ReLU → BatchNorm → MaxPooling → Dropout  
Flatten → Dense(128) → ReLU → Dropout → Dense(5) → Softmax 
```

---

## 🚀 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/PRODIGY_ML_04.git
   cd PRODIGY_ML_04
2. **Create and activate a virtual environment (recommended)**:
   ```bash
   python -m venv venv
   # On Windows:
   venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
4. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook Hand_Gesture_Recognition.ipynb

