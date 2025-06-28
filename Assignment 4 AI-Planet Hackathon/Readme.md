# 🧠 Nutrition Health Survey — Age Prediction 🔬  
**Summer Analytics 2025 | IIT Guwahati x Consulting & Analytics Club**

![Analytics](https://img.shields.io/badge/Challenge-SummerAnalytics2025-purple)
![Python](https://img.shields.io/badge/Python-3.11-blue)
![F1 Score](https://img.shields.io/badge/Evaluation-F1--Score-green)

> Predict if a person is a **Senior (65+) or Adult (<65)** using real medical & lifestyle data — powered by NHANES dataset + your ML superpowers!

---

## 📊 About the Project

The **National Health and Nutrition Examination Survey (NHANES)** is a gold-standard health study by the CDC.  
This challenge uses a **trimmed subset** from NHANES to help participants explore:

- Classification
- Feature Engineering
- Imbalanced data handling
- Model Evaluation via F1-score

You'll work with **6,287 rows of rich health data**, and the goal is to predict whether a person belongs to:

- `0` → **Adult**  
- `1` → **Senior** (Age 65 and above)

---

## 🚀 Challenge Hosted By
👨‍💻 **Consulting & Analytics Club, IIT Guwahati**  
📅 **Summer Analytics 2025**

Compete for leaderboard spots using the **F1 score**, with an extra spotlight on your **Feature Engineering and EDA creativity** in case of tie-breaks!

---

## 📦 Dataset Files

| File | Description |
|------|-------------|
| `train.csv` | 2,016 rows with input features + `age_group` target |
| `test.csv` | 312 rows (no target) — submit predictions here |
| `sample_submission.csv` | Format: two columns — `SEQN`, `age_group` (0 or 1) |

---

## 🎯 Target Variable

- `age_group = 0` → Adult  
- `age_group = 1` → Senior (65+ years)

---

## 🧬 Features

| Column | Description |
|--------|-------------|
| `SEQN` | Sequence ID |
| `RIAGENDR` | Gender (1 = Male, 2 = Female) |
| `PAQ605` | Weekly physical activity (1 = Yes, 2 = No, 9 = Don't know) |
| `BMXBMI` | Body Mass Index |
| `LBXGLU` | Glucose level |
| `DIQ010` | Diabetes diagnosis (1 = Yes, 2 = No, 3 = Borderline, 9 = Don't know) |
| `LBXGLT` | Oral glucose tolerance |
| `LBXIN` | Insulin level |

> ⚠️ **NaNs are present!** You must impute/mask/engineer carefully. Your F1 score depends on it.

---

## 📈 Evaluation Metric

Your model is scored based on **F1 Score** (focus on correctly identifying both classes under imbalance).

| Term | Meaning |
|------|---------|
| TP | True Positive |
| FP | False Positive |
| TN | True Negative |
| FN | False Negative |

> Partial evaluation: **Public leaderboard = 50% test data**, final **Private leaderboard = remaining 50%**.

---

## ⚡ Workflow

1. 📥 Download training data
2. 🔧 Preprocess (EDA + Impute + Engineer)
3. 🤖 Train ML model (LogReg, RandomForest, LGBM, etc.)
4. 📤 Predict on `test.csv`
5. ✅ Format submission (like `sample_submission.csv`)
6. 🔼 Submit & climb the leaderboard!

---

## 🧪 Tips to Boost F1 Score

- Handle class imbalance (use weights or upsampling)
- Engineer smart features (like BMI thresholds, activity-diabetes combos)
- Try threshold tuning, not just raw `.predict()`
- Consider tree-based models if linear ones plateau
- **Avoid overfitting to public leaderboard**

---

## ⚠️ Notes

- Only `0` and `1` are valid predictions
- Final leaderboard = only if you mark your **final submission**
- Data modified slightly by organizers for this hackathon
- Feature engineering creativity might break tie-scores!

---

## 🙌 Acknowledgement

Data is originally from **CDC NHANES**  
Challenge designed for learning by the **C&A Club, IIT Guwahati**

---

## 📚 License & Disclaimer

This dataset is modified and provided for **educational purposes** only.  
We do not own or claim rights to the original NHANES data.

---

> 🏁 Ready to dive into data and decode the secrets of aging?  
Let’s predict the future — literally! 🚀
