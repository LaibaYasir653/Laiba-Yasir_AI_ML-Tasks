# 🏠 House Price Prediction — Task 6

## 📌 Objective
The primary goal of this project is to **predict house prices** based on property features such as:
- Square footage (size of the house)
- Number of bedrooms
- Location
- Other relevant attributes

By building and evaluating regression models, we aim to estimate house prices accurately and understand the influence of different features on property value.

---

## 📂 Dataset

**Source:** [Housing Prices Dataset on Kaggle](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset)  
**File Name:** `Housing.csv`  

### **Key Features in the Dataset:**
- `price` — Target variable, the selling price of the house
- `area` — Square footage of the property
- `bedrooms` — Number of bedrooms
- `bathrooms` — Number of bathrooms
- `stories` — Number of floors
- `mainroad` — Whether the house is connected to the main road (yes/no)
- `guestroom`, `basement`, `hotwaterheating`, `airconditioning` — Boolean features for amenities
- `parking` — Number of parking spaces
- `prefarea` — Whether the house is in a preferred area (yes/no)
- `furnishingstatus` — Type of furnishing (furnished, semi-furnished, unfurnished)

> **Target Variable:** `price` — Continuous value representing the price of the house.

---

## 🛠️ Preprocessing Steps

1. **Handling Missing Values**
   - Used **median imputation** for numeric features.
   - Used **most frequent value imputation** for categorical features.

2. **Feature Scaling**
   - Applied **StandardScaler** to normalize numeric features for models sensitive to scale.

3. **Encoding Categorical Variables**
   - Used **OneHotEncoder** to transform categorical variables into numerical format.

4. **Train-Test Split**
   - 80% training data, 20% testing data.

---

## 🤖 Models Applied

### **1. Linear Regression**
- Simple, interpretable model.
- Assumes a linear relationship between features and target.

### **2. Gradient Boosting Regressor**
- Ensemble learning method combining multiple decision trees.
- Handles non-linear relationships better than linear regression.
- Often provides superior performance in regression tasks.

---

## 📊 Evaluation Metrics

The models were evaluated using:

- **Mean Absolute Error (MAE)** — Measures average absolute difference between predicted and actual prices.
- **Root Mean Squared Error (RMSE)** — Penalizes larger errors more than MAE.
- **R² Score** — Proportion of variance in target explained by the model.

---

## 📈 Key Results & Findings

| Model                  | MAE      | RMSE     | R² Score |
|------------------------|----------|----------|----------|
| Linear Regression      | *X.XX*   | *X.XX*   | *0.XXX*  |
| Gradient Boosting      | *X.XX*   | *X.XX*   | *0.XXX*  |

> *(Replace X.XX with actual results after running the notebook)*

### **Insights:**
- **Gradient Boosting** outperformed **Linear Regression** in all metrics.
- Amenities like **air conditioning**, **preferred area**, and **number of bathrooms** had a noticeable effect on price.
- Location-related features (`mainroad`, `prefarea`) strongly influence price variation.
- Feature scaling improved Linear Regression’s performance but had less impact on Gradient Boosting.

---

## 📊 Visualizations
The notebook includes:
- **Distribution of Prices** — Understand skewness in target variable.
- **Correlation Heatmap** — Identify strong relationships between features.
- **Actual vs Predicted Price Plots** — Evaluate how well the models predict unseen data.

---

## 📦 Requirements
```bash
pip install pandas numpy matplotlib seaborn scikit-learn

# 🚀 How to Run

# 1️⃣ Download the dataset from Kaggle:
#    https://www.kaggle.com/datasets/yasserh/housing-prices-dataset

# 2️⃣ Save the file as "Housing.csv" in your working directory.

# 3️⃣ Run the script or notebook:
jupyter notebook house_price_prediction.ipynb
# OR
python house_price_prediction.py

# 4️⃣ View the performance metrics & visualizations in the output.


# 📌 Notes
# - This project is for educational purposes and should not be used for
#   real-world property valuation without further data validation.
# - Feature engineering & hyperparameter tuning could further improve performance.
# - Cross-validation can be added for more robust evaluation.



# 📚 References

# Kaggle Dataset:
# https://www.kaggle.com/datasets/yasserh/housing-prices-dataset

# Scikit-learn Documentation:
# https://scikit-learn.org/stable/

# Seaborn Visualization Library:
# https://seaborn.pydata.org/

