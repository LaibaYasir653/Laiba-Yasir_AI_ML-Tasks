
# Task 1: Iris Dataset Exploration 🌸

## 📌 Objective
The goal of this task is to perform an **exploratory data analysis (EDA)** on the famous Iris dataset.  
We aim to understand the dataset, visualize its structure, and extract meaningful patterns to support further modeling.

---

## 📂 Dataset Used
The **Iris dataset** contains **150 samples** of iris flowers with the following features:
- **Sepal Length (cm)**
- **Sepal Width (cm)**
- **Petal Length (cm)**
- **Petal Width (cm)**
- **Species** (Target variable: `setosa`, `versicolor`, `virginica`)

📊 **Source:** [Scikit-learn built-in dataset](https://scikit-learn.org/stable/datasets/toy_dataset.html#iris-plants-dataset)

---

## ⚙️ Steps Performed

### 1️⃣ Problem Statement & Goal
- Understand the distribution of features in the Iris dataset.
- Identify patterns, correlations, and potential separability between classes.

### 2️⃣ Data Loading & Preprocessing
- Loaded the dataset using **Scikit-learn**.
- Converted it into a Pandas DataFrame for easy manipulation.
- Checked for **missing values** and **data types**.
- Verified dataset balance across species.

### 3️⃣ Data Visualization & Exploration
- **Univariate Analysis:**
  - Histograms for each feature to see distribution.
  - Boxplots to detect outliers.
- **Bivariate Analysis:**
  - Pair plots (Seaborn) to visualize feature relationships.
  - Scatter plots with hue based on species.
- **Correlation Analysis:**
  - Heatmap to display feature correlations.

### 4️⃣ Model Training & Evaluation (Basic Check)
- Trained a **Logistic Regression** model to classify species.
- Achieved accuracy: **97%** on the test set.
- Generated a confusion matrix to evaluate misclassifications.

### 5️⃣ Results & Insights
- **Setosa** is clearly separable from other species based on petal measurements.
- **Versicolor** and **Virginica** overlap slightly in petal dimensions.
- Petal length & width are the most discriminative features.

---

## 🧠 Models Applied
- **Logistic Regression**: Simple baseline classification model.

---

## 📈 Key Results & Findings
| Metric        | Value |
|--------------|-------|
| Accuracy     | 97%   |
| Most Important Features | Petal Length, Petal Width |

---

## 📦 Requirements
To run the notebook, install the following Python libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## ▶️ How to Run
1. Clone this repository.
2. Open the Jupyter Notebook file (`Task1_Iris_Exploration.ipynb`).
3. Run all cells in order.

---

## 📜 Conclusion
The Iris dataset is well-balanced and easy to classify, especially with petal measurements.  
This EDA provides a strong foundation for testing other classification algorithms in future tasks.

---

✍ **Author:** Laiba Yasir  
📅 **Date:** August 2025
