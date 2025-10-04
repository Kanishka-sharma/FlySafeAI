# 🛡️ FLYSAFEAI — Drone Warning Level Prediction Using Machine Learning  

> 🚀 *Turning flight data into safety intelligence — one prediction at a time.*

---

## 📘 Overview  

**FLYSAFEAI** is a data-driven machine learning project that predicts **drone warning levels** based on telemetry and performance parameters.  
A high warning level indicates that the drone should be **grounded immediately** to prevent potential crashes or malfunctions.  

This project blends **statistical analysis**, **feature engineering**, and **machine learning** to develop interpretable and highly accurate models that ensure **drone flight safety**.

---

## 🎯 Objectives  

- Identify **key drone features** influencing flight risk.  
- Develop **probabilistic (Logistic Regression)** and **predictive (Random Forest)** models.  
- Enable **early risk detection** through real-time analytics.  
- Improve **drone operational safety** using AI insights.  

---

## 📊 Dataset Summary  

| Property | Description |
|-----------|-------------|
| **Records** | 5,725 |
| **Features** | 9 |
| **Target Variable** | (categorical levels: 0, 1, 2, 3) |
| **Source** | Simulated drone telemetry dataset |

**Feature List:**  
`['voltage_v', 'voltage_filtered_v', 'current_a', 'current_filtered_a', 'discharged_mah', 'remaining', 'scale', 'load', 'ram_usage']`

---

## 🧹 Data Preprocessing & EDA  

**Steps Performed:**
- Checked and handled missing values, duplicates, and outliers.  
- Explored data distributions and correlation patterns.  
- Visualized feature relationships with the warning variable.  

**Key Insights:**  
- `voltage_filtered_v` and `remaining` show the strongest correlation with warning levels.  
- Voltage instability and low remaining battery power are early indicators of flight risk.  


---

## 🔍 Feature Selection  

Used **Recursive Feature Elimination (RFE)** with Logistic Regression to identify the most impactful predictors.

**Selected Features:**
['voltage_v','voltage_filtered','current_a','current_filtered_ai','remaining']
> These parameters directly relate to the drone’s **battery health and electrical load**, which strongly influence its performance and risk level.

---

## ⚙️ Model Development  

### 🔸 Logistic Regression (Probabilistic Model)
- Captures the **likelihood** of each warning level.  
- Highlights **individual feature influence** on outcomes.  
- **Accuracy:** 98.7%

> Provides interpretability — useful for safety-critical decisions.

---

### 🔸 Random Forest (Predictive Model)
- Handles **non-linear relationships** and feature interactions.  
- Offers **feature importance ranking** and robust prediction.  
- **Accuracy:** 99.7%

> Excels in classification performance and generalization.

---

## 📈 Model Comparison  

| Model | Type | Accuracy | F1-Score | Strength |
|--------|------|-----------|-----------|-----------|
| Logistic Regression | Probabilistic | 98.7% | 0.98 | Interpretable & Explainable |
| Random Forest | Predictive | **99.7%** | **1.00** | Handles Complex Data & Imbalance |


---

## 💡 Insights & Impact  

- **Battery voltage stability** and **current regulation** are the most significant risk factors.  
- Machine learning enables **real-time monitoring** of drone health.  
- FLYSAFEAI demonstrates how **AI can prevent accidents** by providing **early warnings** before system failure.  

> 🧭 *From reactive maintenance to proactive safety — powered by data science.*

---

## 🧠 Why FLYSAFEAI Stands Out  

✅ **End-to-End AI Pipeline:** Raw data → EDA → Feature Selection → Modeling → Evaluation  
✅ **Dual Modeling Approach:** Logistic Regression (interpretability) + Random Forest (performance)  
✅ **Real-World Use Case:** Focused on **drone safety** — an emerging and relevant AI application  
✅ **High Accuracy + Explainability:** Balances trust and performance  
✅ **Clean, professional structure:** Recruiter-friendly and reproducible  

> 💬 *Unlike many academic projects, FLYSAFEAI demonstrates technical mastery **and** domain relevance — a combination employers value highly.*

---

## 🧰 Tech Stack  

| Category | Tools / Libraries |
|-----------|------------------|
| **Language** | Python |
| **Libraries** | pandas, numpy, seaborn, matplotlib, scikit-learn |
| **Models** | Logistic Regression, Random Forest |
| **Development Environment** | Jupyter Notebook |
| **Version Control** | Git & GitHub |

---

## 🔧 Future Enhancements  

- Apply **SMOTE** or **class weighting** for better minority-class handling.  
- Experiment with **XGBoost, LightGBM, or CatBoost**.  
- Integrate **real-time telemetry streaming** for live risk prediction.  
- Deploy an **interactive dashboard** using Streamlit or Dash for live visual analytics.  

---

## 🏁 Results Summary  

| Metric | Logistic Regression | Random Forest |
|--------|---------------------|---------------|
| Accuracy | 98.7% | **99.7%** |
| Precision | 0.98 | **0.99** |
| Recall | 0.97 | **1.00** |
| F1 Score | 0.98 | **1.00** |






 
