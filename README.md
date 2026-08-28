# titanic-survival-prediction
# 🚢 Titanic Survival Prediction Pipeline

<p align="center">
  <img src="https://img.shields.io/badge/Model-Random%20Forest-blueviolet?style=flat-square&logo=python" alt="Model">
  <img src="https://img.shields.io/badge/Accuracy-80.22%25-success?style=flat-square" alt="Accuracy">
  <img src="https://img.shields.io/badge/Task-Binary%25Classification-orange?style=flat-square" alt="Task">
</p>

---

## 🏗️ Mimari Akış Şeması (Pipeline Diagram)

```text
[ Raw Data: train.csv ]
         │
         ▼
[ 1. Data Preprocessing & Cleaning ] 
         ├── Missing Values (Age -> Median, Cabin Drop/Transform)
         └── Outlier Capping (IQR Method on Fare)
         │
         ▼
[ 2. Feature Engineering ]
         ├── FamilySize = SibSp + Parch + 1
         ├── IsAlone & Title Extraction (from Name)
         └── Encoding (Label & One-Hot Encoding)
         │
         ▼
[ 3. Modeling & Classification ]
         ├── Baseline (~63.0%)
         ├── Decision Tree (74.63%)
         ├── Logistic Regression (79.85%)
         └── Random Forest [Champion] (80.22%)
         │
         ▼
[ 4. Evaluation & Insights ]
         ├── Confusion Matrix (False Positive / False Negative Analysis)
         └── Feature Importance (Sex & Fare Dominance)
