# 🌍 Earthquake Risk Prediction using Machine Learning

This project focuses on analyzing earthquake data and predicting risk levels using machine learning. Instead of attempting exact earthquake prediction (which is highly uncertain), the system classifies earthquakes into **low-risk** and **high-risk** categories based on their magnitude.

---

## 🚀 Project Overview

* **Dataset:** USGS Earthquake Data
* **Problem Type:** Classification
* **Goal:** Identify high-magnitude earthquakes (≥ 5)

The project demonstrates how machine learning can be applied to real-world geospatial data for risk analysis.

---

## ⚙️ Workflow

1. Data loading and cleaning
2. Feature selection (latitude, longitude, depth, time-based features)
3. Feature engineering (year, month, day extraction)
4. Handling missing values
5. Train-test split and scaling
6. Model training and evaluation
7. Visualization (graphs + interactive map)

---

## 🧠 Models Used

* Random Forest
* Support Vector Machine (SVM)
* XGBoost

All models were trained and compared to identify the most effective approach.

---

## ⚠️ Challenge: Imbalanced Data

The dataset contained:

* A large number of low-magnitude earthquakes
* Very few high-magnitude earthquakes

This caused models to achieve high accuracy but perform poorly on important cases.

---

## ✅ Solution

To address this, class imbalance was handled using:

* **Class weighting (`scale_pos_weight`) in XGBoost**

This significantly improved the model’s ability to detect high-magnitude earthquakes.

---

## 📊 Results

- Accuracy: ~97%  
- Recall (High Magnitude): Improved after handling imbalance  
- The model is now more effective at identifying critical earthquake events  

High accuracy alone was misleading due to class imbalance, so recall was improved to better detect critical earthquake events.

---

## 📈 Visualizations

* Magnitude distribution
* Confusion matrix
* Feature relationships
* 🌍 Interactive map using Folium to visualize earthquake locations and risk levels

---

## 🗺️ Map Features

* Marker size based on magnitude
* Color-coded risk levels (high vs low)
* Interactive popups
* Clean and readable light-themed map

---

## 🧩 Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn
* Folium

---

## 🎯 Key Takeaways

* High accuracy alone is not enough — recall is crucial for critical cases
* Handling class imbalance is essential in real-world datasets
* Visualization improves understanding of geospatial patterns

---

## 📌 Future Improvements

* Use larger historical datasets
* Apply deep learning models (e.g., LSTM)
* Build a real-time earthquake monitoring system

---

## 👨‍💻 Author

Mohammed Saqib
