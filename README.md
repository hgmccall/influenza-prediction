# influenza-prediction
Machine learning project that predicts influenza-like illness (ILI) rates using CDC surveillance data, feature engineering, and regression models including Random Forest and XGBoost.
# Influenza-Like Illness (ILI) Prediction Using Machine Learning

A machine learning project that analyzes historical influenza-like illness (ILI) surveillance data and compares multiple predictive models to forecast ILI rates.

---

## Overview

This project explores influenza-like illness (ILI) trends using surveillance data collected across multiple California regions from 2001 to 2020.

The analysis examines historical flu activity, provider reporting patterns, and patient counts to predict Percent ILI using multiple regression models. The project includes data preprocessing, exploratory data analysis, feature engineering, model training, evaluation, and cross-validation.

Three machine learning models were developed and compared:

- Linear Regression
- Random Forest Regression
- XGBoost Regression

---

## Objectives

The primary goals of this project were to:

- Analyze historical influenza-like illness trends
- Identify factors associated with Percent ILI
- Compare traditional statistical methods and machine learning models
- Evaluate predictive performance using regression metrics
- Assess model stability using cross-validation
- Gain experience with ensemble learning techniques

---

## Dataset

Influenza-Like Illness Surveillance Dataset

Dataset Characteristics:

- 5,946 observations
- Data collected from 2001–2020
- Six reporting regions
- Weekly surveillance records

Included Features:

- Region
- Season
- Date
- Total ILI Cases
- Total Patients Seen
- Percent ILI
- Number of Providers Reporting

Target Variable:

- Percent_ILI

---

## Data Cleaning & Preprocessing

Several preprocessing steps were performed to prepare the data for analysis and modeling.

### Missing Value Handling

The dataset contained missing values in the Percent_ILI column.

Missing values were replaced with:

```text
0
```

to represent periods where no influenza-like illness activity was reported.

### Date Conversion

The weekending column was converted into a datetime format.

Additional features were extracted:

- Year
- Month
- Week Number

These features provided temporal information for modeling.

### Categorical Encoding

The region variable was converted into machine-readable numerical features using one-hot encoding.

Two approaches were used:

- One-hot encoding with drop_first=True for Linear Regression
- Full one-hot encoding for tree-based models

---

## Technologies Used

### Programming Language

- Python

### Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost

### Machine Learning Models

- Linear Regression
- Random Forest Regressor
- XGBoost Regressor

### Development Environment

- Jupyter Notebook

---

## Exploratory Data Analysis

Several visualizations were created to better understand the dataset.

### Correlation Heatmap

A heatmap was used to visualize relationships among:

- Total ILI Cases
- Total Patients Seen
- Percent ILI
- Provider Reporting Counts

### Flu Trends Over Time

A time-series plot was used to track changes in influenza-like illness activity across the study period.

### Regional Analysis

A bar chart compared Percent ILI across reporting regions to identify geographic variation.

---

## Modeling Approach

### Train-Test Split

The dataset was divided into:

- 80% Training Data
- 20% Testing Data

This allowed model performance to be evaluated on unseen data.

### Feature Selection

Predictor variables included:

- Total ILI
- Total Patients Seen
- Number of Providers Reporting
- Region
- Year

Target variable:

- Percent ILI

### Feature Scaling

Standardization was applied to Linear Regression inputs using StandardScaler.

Tree-based models did not require feature scaling.

---

## Model Performance

### Linear Regression

Results:

- MSE: 3.27
- R²: 0.32

The linear model explained approximately 32% of the variance in influenza activity.

---

### Random Forest Regression

Results:

- MSE: 0.13
- R²: 0.97

The Random Forest model significantly improved predictive performance by capturing nonlinear relationships in the data.

---

### XGBoost Regression

Results:

- MSE: 0.07
- R²: 0.99

XGBoost achieved the strongest predictive performance among all tested models.

---

## Cross-Validation Results

Five-fold cross-validation was performed to evaluate model generalizability.

Results:

| Model | Average R² |
|---------|---------|
| Linear Regression | 0.29 |
| Random Forest | 0.96 |
| XGBoost | 0.96 |

The ensemble models demonstrated strong and consistent predictive capability across multiple validation folds.

---

## Visualizations

The project includes:

- Correlation heatmaps
- Time-series flu trend analysis
- Regional ILI comparisons
- Actual vs Predicted scatter plots
- XGBoost learning curves
- Random Forest feature importance analysis
- XGBoost feature importance analysis
- Model comparison charts

---

## Key Findings

### Ensemble Models Outperformed Linear Regression

Random Forest and XGBoost dramatically outperformed Linear Regression, suggesting that nonlinear relationships exist between the predictors and influenza activity.

### XGBoost Delivered the Best Performance

XGBoost achieved the highest predictive accuracy with an R² score of approximately 0.99 and the lowest Mean Squared Error.

### Reporting and Case Counts Were Highly Predictive

Variables such as Total ILI Cases, Total Patients Seen, and Provider Reporting Counts were among the most influential predictors.

### Cross-Validation Confirmed Model Stability

Random Forest and XGBoost maintained strong performance across multiple validation folds, reducing concerns about overfitting.

---

## Future Improvements

Potential enhancements include:

- Hyperparameter tuning using GridSearchCV
- Forecasting future flu seasons
- Integration of weather and population data
- Time-series forecasting models
- Interactive dashboards using Power BI or Tableau
- Public health surveillance visualization tools

---

## Author

Hailey McCall

LinkedIn: www.linkedin.com/in/hailey-mccall

GitHub: https://github.com/haileymccall
