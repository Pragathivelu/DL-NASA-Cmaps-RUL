# 🚀 Remaining Useful Life (RUL) Prediction using GRU

## 📌 Project Overview

This project focuses on predicting the **Remaining Useful Life (RUL)** of turbofan engines using deep learning techniques. The model is trained on the NASA CMAPSS dataset and leverages a **GRU (Gated Recurrent Unit)** network to capture temporal dependencies in sensor data.

The goal is to enable **predictive maintenance**, reducing unexpected failures and optimizing maintenance schedules in industrial systems.

---

## 📊 Dataset

* Dataset: NASA CMAPSS (Turbofan Engine Degradation Simulation)
* dataset represents different operating conditions and fault modes
* Features:

  * 3 operational settings
  * 21 sensor measurements
  * Engine cycles (time-series)

---

## 🧠 Problem Statement

Predict the **Remaining Useful Life (RUL)** of an engine at any given cycle using historical sensor data.

This is a **regression problem**, where the output is a continuous value representing the number of cycles before failure.

---

## ⚙️ Pipeline

1. Data Loading
2. RUL Calculation
3. RUL Clipping (max threshold = 130)
4. Feature Selection
5. Train / Validation / Test Split (by engine unit)
6. Feature Scaling (MinMaxScaler)
7. Sequence Generation (time-series windows)
8. GRU Model Training
9. Model Evaluation

---

## 🏗️ Model Architecture

* GRU Layers: 3
* Units: 128 → 64 → 32
* Dropout: 0.2 – 0.3
* Optimizer: Adam
* Loss Function: Mean Squared Error (MSE)

---

## 📈 Evaluation Metrics

* RMSE (Root Mean Squared Error)
* MAE (Mean Absolute Error)

### ✅ Final Model Performance

* RMSE: ~11.96
* MAE: ~8.66

This indicates strong predictive performance for RUL estimation.

---

## 📊 Key Insights

* Time-series modeling significantly improves prediction accuracy
* GRU effectively captures temporal degradation patterns
* Model generalizes well across unseen engine units
* Proper sequence creation and unit-based splitting are critical

---

## 🔍 Advanced Techniques Used

* Early Stopping (to prevent overfitting)
* Learning Rate Scheduling (ReduceLROnPlateau)
* Sequence-based time-series modeling
* Unit-based data splitting to avoid data leakage

---

## 🛠️ Tech Stack

* Python
* TensorFlow / Keras
* NumPy, Pandas
* Scikit-learn
* Matplotlib / Seaborn

---

!
