# 🌱 NDVI-based Land Cover Classification | Summer Analytics 2025 Hackathon

Welcome to my submission for the **First Course Hackathon - Summer Analytics 2025**, hosted by the **Consulting & Analytics Club** in collaboration with **GeeksforGeeks**.

## 🚀 Overview

The goal of this hackathon was to build a **Multiclass Logistic Regression** model that classifies land cover types using **NDVI (Normalized Difference Vegetation Index)** time-series data. Each sample represents a location with 27 NDVI observations across time, alongside a labeled land cover type from six categories:

- **Water**
- **Impervious**
- **Farm**
- **Forest**
- **Grass**
- **Orchard**

### 🎯 Objective

Design a model that performs well even under **noisy** and **incomplete** data conditions — simulating real-world remote sensing challenges like cloud interference and imperfect labeling.

---

## 📚 What I Learned

### 🌍 Domain Knowledge
- Understood the significance of **NDVI** in analyzing vegetation health.
- Learned how land cover classification supports ecological monitoring and urban planning.

### 📈 Machine Learning Skills
- Implemented **Multiclass Logistic Regression** from scratch and using `scikit-learn`.
- Tackled **imbalanced classes** using class weights and stratified sampling.

### 🧹 Data Preprocessing & Feature Engineering
- **Imputation Techniques**: Used forward fill and mean strategies to handle missing NDVI values due to cloud cover.
- **Denoising**: Applied smoothing techniques like rolling averages to reduce the effect of noisy NDVI time points.
- **Feature Extraction**: Generated statistical summaries (mean, std, min, max, trend) to capture vegetation dynamics over time.

### 🧪 Evaluation
- Split the data strategically to mimic public/private leaderboard settings.
- Validated generalization using clean test data to avoid overfitting noisy training data.

---

## ⚙️ Project Structure

```bash
.
├── notebooks/
│   ├── EDA_and_Preprocessing.ipynb
│   └── Logistic_Regression_Model.ipynb
├── data/
│   ├── train.csv
│   ├── test.csv
│   └── sample_submission.csv
├── submission/
│   └── final_submission.csv
├── README.md
└── requirements.txt

