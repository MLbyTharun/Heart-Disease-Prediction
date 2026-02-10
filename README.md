# ❤️ Heart Disease Prediction using Machine Learning

## 📌 Overview
This project focuses on predicting the presence of heart disease using clinical patient data.  
The dataset used in this competition was **pre-cleaned**, allowing the primary focus to be on **model selection, evaluation, and optimization**.

The objective was to maximize **ROC-AUC** on an **unseen Kaggle test dataset**.

---

## 📊 Dataset
- Source: Kaggle (Heart Disease Prediction Competition)
- Type: Pre-cleaned tabular clinical data
- Target Variable: Heart disease (binary classification)
- Evaluation Metric: **ROC-AUC**

> ⚠️ Dataset is not included in this repository due to Kaggle licensing rules.

---

## 🧠 Modeling Approach

### 1️⃣ Baseline Model — Logistic Regression
- Used as a strong baseline due to its simplicity and interpretability
- Performance on unseen test data:
  - **ROC-AUC: 0.88**

This established a reliable baseline before moving to more complex models.

---

### 2️⃣ Advanced Model — CatBoost Classifier
CatBoost was chosen due to its robustness on tabular data and strong handling of feature interactions.

#### Results:
- **Slightly tuned CatBoost**
  - ROC-AUC: **0.95336**
- **Well-tuned CatBoost (final model)**
  - ROC-AUC: **0.95349**

📌 **Current competition best score:** 0.95399  
➡️ Final model is **very close to the leaderboard top**.

---

### 3️⃣ Ensemble Experiments
The following ensemble strategies were explored:
- CatBoost + Logistic Regression
- CatBoost + XGBoost

📉 **Observation:**
- Neither ensemble outperformed the **solo CatBoost model**
- Added complexity did not translate to performance gains

This reinforced the strength of the single CatBoost model for this dataset.

---

## 📈 Model Performance Summary

| Model                         | ROC-AUC |
|------------------------------|---------|
| Logistic Regression           | 0.88    |
| CatBoost (tuned)              | 0.95336 |
| CatBoost (well-tuned, final)  | 0.95349 |
| Best Competition Score        | 0.95399 |

---

## 🧪 Why CatBoost Performed Exceptionally Well
CatBoost excelled in this problem due to:
- Strong handling of **tabular structured data**
- Built-in **regularization**, reducing overfitting
- Ability to model **complex feature interactions**
- Robust performance even with minimal preprocessing
- Stability on unseen test data

These characteristics made CatBoost more effective than both linear models and ensemble combinations in this competition.

---

## 🛠️ Tech Stack
- Python
- Pandas
- NumPy
- Scikit-learn
- CatBoost
- XGBoost
- Matplotlib / Seaborn
- Jupyter Notebook

---


## 🚀 Future Work
- Narrow gap with leaderboard top score
- Feature interaction analysis
- SHAP-based model interpretability
- Cross-validation strategies
- Experiment with stacking ensembles

---

## 👤 Author
**Tharun K**  
Aspiring Data Scientist | Machine Learning Enthusiast  

GitHub: https://github.com/MLbyTharun
