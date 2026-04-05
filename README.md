# Yes Bank Stock Price Prediction (Machine Learning Project)

## 1. Project Overview

This project focuses on analyzing historical stock price data and building machine learning models to predict the closing price of Yes Bank stock. The objective is to understand price behavior, explore relationships between stock variables, and evaluate the predictive performance of different regression algorithms.

The project applies data preprocessing, exploratory data analysis (EDA), feature transformation, and multiple regression models to identify the most effective approach for stock price prediction.

---

## 2. Dataset Information

* Dataset: Yes Bank Historical Stock Data
* Total Records: 185
* Time Period Covered: July 2005 – November 2020
* Data Frequency: Monthly

### Dataset Columns

1. Date – Month and year of the record
2. Open – Opening price of the stock
3. High – Highest price during the period
4. Low – Lowest price during the period
5. Close – Closing price of the stock (Target Variable)

Key observations:

* The dataset contains **5 variables**.
* Price-related columns are numerical (float64).
* The Date column was converted to datetime format for better analysis.
* No missing values were found in the dataset.

---

## 3. Project Workflow

The project was executed in several stages:

1. Data Loading
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Handling Multicollinearity
6. Model Building
7. Model Evaluation
8. Final Conclusion

---

## 4. Data Preprocessing

Steps performed during preprocessing:

* Loaded the dataset using Python.
* Converted the Date column into datetime format.
* Verified data types for all variables.
* Checked for missing values and duplicates.
* Confirmed dataset completeness.

Result:
The dataset was clean and ready for analysis without requiring major cleaning operations.

---

## 5. Exploratory Data Analysis (EDA)

EDA was conducted to understand stock price behavior and relationships between variables.

Techniques used:

* Statistical summaries of variables
* Scatter plots to examine relationships with the Close price
* Trend analysis

Insights:

* Strong relationships were observed between Open, High, Low, and Close prices.
* Most variables showed strong correlation with the closing price.

---

## 6. Handling Multicollinearity

Since several features were highly correlated, multicollinearity could affect regression model performance.

To address this issue:

* A PowerTransformer using the Box-Cox method was applied.
* The transformation standardized the features and reduced skewness.

Benefits:

* Stabilized variance
* Improved feature distribution
* Reduced multicollinearity impact

---

## 7. Feature Engineering

Independent variables (X):

* Open
* High
* Low

Dependent variable (y):

* Close

The dataset was split into training and testing sets:

* Training Data: 80%
* Testing Data: 20%

---

## 8. Machine Learning Models Implemented

Four regression models were trained and evaluated:

1. Linear Regression
2. K-Nearest Neighbors (KNN) Regressor
3. Random Forest Regressor
4. Ridge Regression

### Hyperparameter Tuning

GridSearchCV with 5-fold cross-validation was used for:

* KNN (n_neighbors tuning)
* Random Forest (n_estimators, criterion, max_features)

This helped identify the best model configuration.

---

## 9. Model Evaluation

The models were evaluated using the **R² (R-Squared) metric**, which measures how well the predicted values match the actual values.

Visualization techniques were also used:

* Predicted vs Actual value plots

Key observations:

* Linear Regression captured general trends but missed sharp fluctuations.
* KNN captured local patterns and sharp movements effectively.
* Random Forest showed strong predictive performance and handled complex patterns.
* Ridge Regression improved stability compared to simple linear regression.

---

## 10. Key Results

* Random Forest delivered strong predictive performance.
* KNN effectively captured short-term fluctuations.
* Ridge Regression reduced overfitting compared to basic Linear Regression.

Overall, ensemble-based models demonstrated better capability in capturing complex stock price behavior.

---

## 11. Tools and Technologies Used

Programming Language:

* Python

Libraries:

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

Environment:

* Google Colab

---

## 12. Conclusion

This project demonstrates how machine learning techniques can be applied to financial data for predictive analysis. By analyzing historical stock prices and implementing multiple regression models, we were able to compare their predictive capabilities.

The study shows that advanced models such as Random Forest and KNN can capture complex stock price patterns more effectively than simple regression approaches.

Future improvements could include:

* Using larger financial datasets
* Incorporating additional financial indicators
* Applying advanced time-series models such as LSTM or ARIMA

---

## 13. Author

Project completed as part of a Machine Learning Capstone Project.

Author: Franko
