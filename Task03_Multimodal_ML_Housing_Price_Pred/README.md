# 🏠 Task 3: Multimodal ML – Housing Price Prediction

## 📝 Project Overview
This project implements a **Multimodal Machine Learning** model to predict housing prices. Unlike traditional models that only use tabular data, this approach combines **structured numerical data** (area, bedrooms, etc.) with **unstructured image data** (house photos) to improve prediction accuracy.

---

## 🚀 Technical Implementation

### 1. Architecture: Feature Fusion
The model consists of two parallel branches that are merged before the final prediction:
- **CNN Branch (Images):** Uses Convolutional Neural Networks (`Conv2D`, `MaxPooling2D`) to extract spatial features from house images.
- **MLP Branch (Tabular):** A Fully Connected Neural Network to process numerical features like square footage and room counts.
- **Fusion Layer:** Uses `concatenate` to join features from both branches, followed by dense layers for regression.

### 2. Key Techniques
- **Multimodal Learning:** Integration of different data types (Vision + Tabular).
- **CNN Feature Extraction:** Automatically learning visual patterns of houses.
- **Regression Modeling:** Predicting a continuous value (Price).

---

## 🛠️ Tech Stack
- **Framework:** TensorFlow / Keras
- **Libraries:** `NumPy`, `Pandas`, `Matplotlib`, `Scikit-learn`
- **Environment:** Google Colab (T4 GPU)

---

## 📊 Evaluation Metrics
The model was evaluated using standard regression metrics:
- **MAE (Mean Absolute Error):** Measures the average magnitude of errors.
- **RMSE (Root Mean Squared Error):** penalizes larger errors more heavily.

**Current Results:**
- **MAE:** 251,938.73
- **RMSE:** 282,771.02
*(Note: Values based on the provided experimental dataset)*

---

## 👨‍💻 Submission Details
- **Student Name:** Muhammad Yahya
- **Role:** AI/ML Engineering Intern
- **Date:** April 28, 2026
