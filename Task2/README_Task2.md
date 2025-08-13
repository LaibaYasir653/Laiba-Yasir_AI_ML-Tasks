📊 Task 2: Predict Future Stock Prices (Short-Term)
📝 Objective

The aim of this task is to predict the next day's closing stock price using historical data from Yahoo Finance.
We will use time series regression modeling to forecast short-term price movement and visualize the predictions.
📂 Dataset

The stock market data is retrieved directly from Yahoo Finance using the yfinance Python library.
This dataset contains:

    Open: Price at market open

    High: Highest price during the day

    Low: Lowest price during the day

    Volume: Total number of shares traded

    Close: Price at market close (target variable)

Data Source: Yahoo Finance
Python Library: yfinance
🛠️ Skills Demonstrated

    Fetching stock market data via API (yfinance)

    Preprocessing and handling time series data

    Applying Linear Regression and Random Forest Regression models

    Splitting training and testing datasets

    Model evaluation using R² score and Mean Absolute Error

    Plotting actual vs predicted closing prices

📌 Workflow Overview

Below is the step-by-step process followed in the notebook:
1️⃣ Import Libraries

Essential Python libraries for data fetching, processing, modeling, and visualization were imported, including:

    pandas for data handling

    numpy for numerical operations

    matplotlib & seaborn for plotting

    sklearn for machine learning

    yfinance for fetching stock data

2️⃣ Fetch Historical Data

    Selected a stock (e.g., Apple - AAPL).

    Fetched 1 year of historical data using yfinance.download().

    Extracted relevant features: Open, High, Low, Volume.

    The Close column was used as the target variable.

3️⃣ Feature Selection

    Independent Variables (X):

        Open

        High

        Low

        Volume

    Dependent Variable (y):

        Close (next day's predicted closing price)

4️⃣ Data Splitting

    80% Training data

    20% Testing data

    Used train_test_split() from sklearn to split data while preserving the sequence of time series.

5️⃣ Model 1: Linear Regression (LR)

    A simple and interpretable regression model.

    Fits a straight-line relationship between features and target.

    Quick to train, useful for identifying trends.

Advantages:

    Easy to implement and interpret.

    Works well with linear relationships.

Limitations:

    Poor performance on non-linear data.

    Sensitive to outliers.

6️⃣ Model 2: Random Forest Regression (RFG)

    An ensemble model combining multiple decision trees.

    Captures non-linear patterns and interactions between features.

Advantages:

    Works well with complex relationships.

    Resistant to overfitting.

    Handles outliers better than LR.

Limitations:

    Less interpretable than Linear Regression.

    Computationally more expensive.

7️⃣ Model Evaluation

Both models were evaluated using:

    R² Score (Coefficient of Determination)
    Measures how well the predictions match the actual values.

    Mean Absolute Error (MAE)
    Average absolute difference between predicted and actual prices.

📌 In our results, Random Forest Regression outperformed Linear Regression, showing higher R² and lower MAE.
8️⃣ Visualization

    Plotted actual vs predicted closing prices for both models.

    This visual comparison clearly showed Random Forest predictions aligning more closely with real stock prices.

📊 Results Summary
Model	R² Score	MAE
Linear Regression	Lower	Higher
Random Forest Regression	Higher	Lower

✅ Random Forest Regression is better suited for this task due to stock market data's non-linear nature.
📌 Key Insights

    Data from Yahoo Finance can be fetched easily for modeling.

    Random Forest Regression generally gives better accuracy than Linear Regression for stock predictions.

    Feature importance analysis from RFG helps identify which factors most influence stock price changes.

🚀 How to Run

    Install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn yfinance

Open the Jupyter Notebook:

    jupyter notebook Task2_Stock_Prediction.ipynb

    Select your desired stock ticker symbol (e.g., "AAPL", "TSLA") in the data fetching section.

    Run all cells to:

        Fetch historical stock data

        Train models

        View predictions and performance metrics

📌 References

    Yahoo Finance API: https://finance.yahoo.com/

    yfinance Python Library: https://pypi.org/project/yfinance/

    Scikit-learn Documentation: https://scikit-learn.org/