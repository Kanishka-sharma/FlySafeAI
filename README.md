# 🛡️ FLYSAFEAI — Drone Warning Level Prediction Using Machine Learning

> 🚀 *Turning flight data into safety intelligence by solving real-world data challenges.*

---

## 📘 Overview

**FLYSAFEAI** is a data-driven project that predicts drone warning levels to prevent equipment failure and ensure operational safety. A high warning level indicates that a drone must be grounded immediately.

This project demonstrates a complete, end-to-end machine learning workflow, from initial data analysis to final model evaluation. A key challenge was a **severe class imbalance** in the dataset, where critical (but rare) warning signals were easily missed by standard models. This analysis showcases how using the **SMOTE (Synthetic Minority Over-sampling Technique)** can transform a misleadingly "accurate" model into a genuinely effective and reliable safety tool.

---

## 🎯 Project Highlights

-   **Problem Solving:** Identified and solved a critical class imbalance problem, a common challenge in real-world datasets.
-   **Model Improvement:** Dramatically improved model performance on minority classes, boosting the Random Forest F1-score from a failing grade to a perfect **1.00**.
-   **Comparative Analysis:** Evaluated both a probabilistic model (Logistic Regression) for interpretability and an ensemble model (Random Forest) for predictive power.
-   **Feature Engineering:** Used **Recursive Feature Elimination (RFE)** to identify the most critical predictors of drone failure.

---

## ⚙️ The Challenge: Severe Class Imbalance

Initial models achieved high accuracy (~99%), but this was misleading. The models were simply predicting the majority class while completely failing to identify the rare, critical warning levels, resulting in F1-scores of **0.00** for those classes.

### The Solution: Applying SMOTE

By applying SMOTE to the training data, we generated synthetic samples of the minority classes. This created a balanced dataset, allowing the models to learn the patterns of rare events effectively.

---

## 📈 Final Model Performance (After SMOTE)

The results after balancing the data show a massive improvement, with the Random Forest model achieving a perfect score on the test set.

| Model               | Type          | Accuracy | Weighted F1-Score | Key Strength                            |
| ------------------- | ------------- | -------- | ----------------- | --------------------------------------- |
| Logistic Regression | Probabilistic | 96%      | 0.97              | Good recall & high interpretability     |
| **Random Forest** | **Predictive** | **100%** | **1.00** | **Perfect classification & robustness** |


### Key Predictive Features

The Random Forest model identified **`voltage_filtered_v`** and **`remaining`** battery as the most significant predictors of a potential failure.

---
##  M️odel Validation

To ensure the model's near-perfect score wasn't a fluke from a single `train_test_split`, I performed rigorous **k-fold cross-validation**. This process repeatedly tests the model on different subsets of the data to verify its stability and predictive power.

The results confirmed the model's exceptional robustness:

| Metric                          | Value      |
| ------------------------------- | ---------- |
| **Validation Folds** | 20         |
| **Average Weighted F1-Score** | **0.9975** |
| **Standard Deviation** | **0.0041** |

A high average score with a very low standard deviation proves that the model is **consistently accurate and reliable**, solidifying its readiness for a real-world application.

## 🧰 Tech Stack

| Category                | Tools / Libraries                                  |
| ----------------------- | -------------------------------------------------- |
| **Language** | Python                                             |
| **Core Libraries** | pandas, numpy, scikit-learn                        |
| **Data Imbalance** | `imblearn` (for SMOTE)                             |
| **Visualisation** | seaborn, matplotlib                                |
| **Development** | Jupyter Notebook                                   |
| **Version Control** | Git & GitHub                                       |

---

## 🔧 Future Enhancements

-   **Hyperparameter Tuning:** Use `GridSearchCV` or `RandomizedSearchCV` to further optimize the Random Forest model.
-   **Explore Other Models:** Experiment with gradient boosting models like XGBoost or LightGBM, which often perform well on tabular data.
-   **Deployment:** Wrap the final model in a simple API using Flask or FastAPI and create an interactive web app with Streamlit to predict drone warnings in real-time.
