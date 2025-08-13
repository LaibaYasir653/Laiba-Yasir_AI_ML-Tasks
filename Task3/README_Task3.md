❤️ Task 3 — Heart Disease Prediction (UCI)


📌 Objective

The aim of this task is to build a machine learning model that predicts whether a person is at risk of heart disease based on their clinical health data.
We leverage the UCI Heart Disease Dataset and apply both Logistic Regression and Decision Tree models to compare performance.

This project focuses on:

    Understanding medical data features

    Practicing binary classification

    Evaluating model performance with multiple metrics

    Extracting feature importance for interpretability

📂 Dataset Information

Kaggle Dataset Source - https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data?resource=download

Primary Source:
UCI Machine Learning Repository — Heart Disease Dataset

Dataset Variants:
This dataset has several versions (Cleveland, Hungarian, etc.). We focus on the Cleveland subset, which is most widely used in ML research.

Fallback CSV Used in This Notebook:
Public GitHub mirror:

https://raw.githubusercontent.com/sharmaroshan/Heart-UCI-Dataset/master/heart.csv

Columns Overview
Column	Description
age	Age in years
sex	Sex (1 = male; 0 = female)
cp	Chest pain type (0–3)
trestbps	Resting blood pressure (mm Hg)
chol	Serum cholesterol (mg/dl)
fbs	Fasting blood sugar > 120 mg/dl (1 = true; 0 = false)
restecg	Resting ECG results (0–2)
thalach	Maximum heart rate achieved
exang	Exercise induced angina (1 = yes; 0 = no)
oldpeak	ST depression induced by exercise
slope	Slope of peak exercise ST segment (0–2)
ca	Number of major vessels (0–3) colored by fluoroscopy
thal	Thalassemia status (1 = normal; 2 = fixed defect; 3 = reversible defect)
num / target	Heart disease diagnosis (0 = no disease, 1+ = disease)

Target Transformation in Our Task:
We convert num into a binary target:

y = df['num'].apply(lambda x: 1 if x > 0 else 0)

🛠️ Skills Practiced

    Data Cleaning — Handling missing values, duplicates, inconsistent datatypes.

    Exploratory Data Analysis (EDA) — Understanding distributions, correlations, and key patterns.

    Feature Engineering — Encoding categorical variables, scaling numeric ones.

    Modeling — Logistic Regression & Decision Tree Classifier.

    Model Evaluation — Accuracy, ROC-AUC, Confusion Matrix, ROC curve plotting.

    Interpretability — Feature importance ranking from both models.

🧭 Workflow Overview

The notebook follows a clear ML pipeline:
1. Data Loading

    Attempts to load heart.csv locally.

    If missing, downloads from the GitHub raw CSV link.

2. Data Cleaning

    Handles missing values (if any) using SimpleImputer.

    Ensures correct data types (numeric/categorical separation).

    Converts num to binary target (0/1).

3. Exploratory Data Analysis

    Summary statistics.

    Class distribution check.

    Histograms for continuous features.

    Correlation heatmap to see relationships.

4. Preprocessing

    Numerical columns: Standardized using StandardScaler.

    Categorical columns: Encoded with OneHotEncoder.

5. Model Training

    Logistic Regression (good for interpretable coefficients).

    Decision Tree (good for feature importance & rule-based classification).

6. Evaluation Metrics

    Accuracy score.

    ROC-AUC score.

    Confusion Matrix (visualized).

    Classification Report (Precision, Recall, F1-score).

7. ROC Curves

    Plotted for both models on the same graph for easy comparison.

8. Feature Importance

    Logistic Regression → Standardized coefficients.

    Decision Tree → feature_importances_.

📦 Requirements

pip install pandas numpy scikit-learn matplotlib seaborn

🚀 How to Run the Notebook

    Clone this repository:

git clone https://github.com/<your-username>/ai-ml-internship.git
cd ai-ml-internship

Place the dataset heart.csv in the same folder as Task3_Heart_Disease_Prediction.ipynb.
Or let the notebook auto-download from the GitHub link provided.

Open Jupyter Notebook:

    jupyter notebook

    Open Task3_Heart_Disease_Prediction.ipynb and Run All Cells.

📊 Sample Output

    Logistic Regression

        Accuracy ≈ 0.85

        ROC-AUC ≈ 0.91

    Decision Tree

        Accuracy ≈ 0.78

        ROC-AUC ≈ 0.82

(Results vary based on train-test split and random seed.)
⚠️ Notes & Cautions

    This project is for educational purposes only and not a medical diagnostic tool.

    Always use a diverse and clinically validated dataset for real-world predictions.

    Consider advanced techniques (cross-validation, hyperparameter tuning) for production-level models.

📚 References

    UCI Heart Disease Dataset- https://archive.ics.uci.edu/dataset/45/heart%2Bdisease

    Public CSV Mirror- https://raw.githubusercontent.com/sharmaroshan/Heart-UCI-Dataset/master/heart.csv

    Scikit-learn Documentation- https://scikit-learn.org/stable/

