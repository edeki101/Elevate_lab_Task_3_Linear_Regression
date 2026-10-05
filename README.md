# Elevate_lab_Task_3_Linear_Regression# Task 3: Linear Regression - AI & ML Internship

## 📋 Project Overview
This repository contains the implementation of **Simple and Multiple Linear Regression** using the Housing dataset as part of the AI & ML Internship tasks. The primary objective is to explore real estate data, preprocess features, train a linear regression model using `scikit-learn`, evaluate performance using standard error metrics, and interpret feature coefficients.

---

## 🛠️ Complete Workflow Followed
1. **Dataset Import & Selection:** Loaded the Housing dataset (`Housing.csv`) containing various property attributes and prices.
2. **Data Inspection:** Examined the dataset structure, data types, non-null counts, and summary statistics using Pandas (`.info()`, `.describe()`, `.head()`)[cite: 3].
3. **Exploratory Data Analysis (EDA):** Visualized feature distributions and correlation matrices via heatmaps to identify key price drivers and check for multicollinearity.
4. **Data Preprocessing:** Handled categorical variables by mapping binary columns (`yes`/`no` to `1`/`0`) and applying One-Hot Encoding to multi-class features (e.g., `furnishingstatus`).
5. **Data Splitting:** Split the cleaned dataset into an **80% training set** and a **20% testing set**[cite: 1].
6. **Model Training:** Fitted a **Multiple Linear Regression** model using `sklearn.linear_model`[cite: 1].
7. **Model Evaluation:** Evaluated model predictions on the test set using standard regression metrics:
   - **Mean Absolute Error (MAE)**[cite: 1]
   - **Mean Squared Error (MSE)**[cite: 1]
   - **$R^2$ Score (Coefficient of Determination)**[cite: 1]
8. **Visualization & Interpretation:** Plotted actual vs. predicted house values and analyzed the magnitude and direction of feature coefficients[cite: 1].

---

## 📊 Results & Performance Metrics
* **$R^2$ Score:** `[Insert your R^2 score here, e.g., 0.65]`
* **Mean Absolute Error (MAE):** `[Insert your MAE value here]`
* **Mean Squared Error (MSE):** `[Insert your MSE value here]`

*(Tip: You can add a screenshot of your Actual vs. Predicted scatter plot in your repo and link it here!)*

---

## ⚙️ Prerequisites & Dependencies
To run this project locally, ensure you have Python installed along with the required libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn


Interview Questions & Answers
1. What assumptions does linear regression make?
•	Linearity: The relationship between the independent variables and the dependent variable is linear.
•	Independence: The observations/residuals are independent of one another (no autocorrelation).
•	Homoscedasticity: The residuals have constant variance across all levels of the independent variables.
•	Normality: The error terms (residuals) are normally distributed.
•	No/Low Multicollinearity: The independent variables are not excessively correlated with each other.
2. How do you interpret the coefficients?
•	Each coefficient represents the expected change in the dependent variable (y) for a one-unit increase in that specific independent variable, assuming all other independent variables remain constant (ceteris paribus).
3. What is R2 score and its significance?
•	R2 (Coefficient of Determination) measures the proportion of variance in the dependent variable that can be explained by the independent variables.
•	Significance: It ranges from 0 to 1 (though it can be negative for models performing worse than a horizontal mean line). A score closer to 1 indicates that the model fits the data very well, meaning a large percentage of the variance is captured by your features.
4. When would you prefer MSE over MAE?
•	MSE (Mean Squared Error) squares the errors before averaging them, which heavily penalizes large errors and outliers.
•	You prefer MSE when large prediction errors are exceptionally costly or dangerous for your application. In contrast, MAE (Mean Absolute Error) treats all errors linearly and is preferred when your dataset contains significant outliers that you don't want to disproportionately skew your model.
5. How do you detect multicollinearity?
•	Correlation Matrix / Heatmap: Checking the Pearson correlation coefficients between predictor variables. Values exceeding 0.8 or 0.9 strongly suggest high multicollinearity.
•	Variance Inflation Factor (VIF): Calculating VIF for each feature. A VIF value above 5 or 10 indicates that the feature is highly collinear with other variables.
6. What is the difference between simple and multiple regression?
•	Simple Linear Regression: Involves only one independent variable to predict a single dependent variable (y=β0+β1x).
•	Multiple Linear Regression: Involves two or more independent variables to predict a single dependent variable (y=β0+β1x1+β2x2+⋯+βnxn).
7. Can linear regression be used for classification?
•	Standard linear regression outputs continuous numeric values, making it unsuited for discrete class labels. However, its modified form—Logistic Regression—applies the sigmoid function to map continuous values into probabilities between 0 and 1, making it a standard tool for binary classification.
8. What happens if you violate regression assumptions?
•	Violating regression assumptions compromises the reliability of your model. It can lead to biased coefficient estimates, inaccurate standard errors, misleading p-values (invalidating hypothesis tests and confidence intervals), and severely degraded predictive accuracy on unseen data.
 
--- Model Coefficients Interpretation ---
                        Feature   Coefficient
                      bathrooms  1.094445e+06
                airconditioning  7.914267e+05
                hotwaterheating  6.846499e+05
                       prefarea  6.298906e+05
   furnishingstatus_unfurnished -4.136451e+05
                        stories  4.074766e+05
                       basement  3.902512e+05
                       mainroad  3.679199e+05
                      guestroom  2.316100e+05
                        parking  2.248419e+05
furnishingstatus_semi-furnished -1.268818e+05
                       bedrooms  7.677870e+04
                           area  2.359688e+02

Intercept (eta_0$): 260032.36



