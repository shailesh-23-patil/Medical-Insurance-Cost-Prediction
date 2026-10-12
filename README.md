# Medical Insurance Cost Prediction

Repository: Medical-Insurance-Cost-Prediction

This project analyzes medical insurance charges and predicts how much a person might pay based on demographic and health-related attributes. It focuses on understanding the strongest drivers of insurance cost and testing several regression models.

## Project Goal

The main objective is to study how factors such as age, BMI, smoking status, sex, region, and family size affect medical insurance charges and build a machine-learning model to predict future insurance cost accurately.

## Dataset

- File: `insurance.csv`
- Target variable: `charges`
- Features include:
  - `age`
  - `sex`
  - `bmi`
  - `children`
  - `smoker`
  - `region`

## Data Cleaning and Preparation

The project performs a clean and structured preprocessing workflow:

- checked for missing values
- removed duplicate rows
- converted BMI into categories such as underweight, normal, overweight, and obese
- created dummy variables for categorical attributes
- added a smoker-by-obesity interaction feature to capture a meaningful business insight

This interaction is important because the dataset clearly suggests that smoking and obesity together drive much higher insurance costs than either factor alone.

## Exploratory Data Analysis

The notebook highlights several important patterns:

- smokers pay much higher medical costs than non-smokers
- age and BMI are strongly associated with higher charges
- the cost distribution is highly skewed
- smoking status is the strongest visible driver of premium level

## Feature Engineering and Selection

The project applies:

- BMI category creation
- one-hot encoding for categorical variables
- Pearson correlation analysis
- chi-square testing for binary features
- interaction term: `smoker_obese`

This allows the model to capture effects that a simple linear model would otherwise miss.

## Modeling Approach

The notebook compares several regression models:

- Linear Regression (baseline)
- Linear Regression with interaction term
- Random Forest Regressor
- Gradient Boosting Regressor

Models are evaluated with:

- R2 score
- Adjusted R2
- MAE
- RMSE
- 5-fold cross-validation

## Key Insights

- Smoking is the strongest predictor of high insurance charges.
- BMI and age also contribute strongly to the cost.
- The interaction between smoking and obesity increases expected premium significantly.
- Adding the interaction term improved the model compared with the baseline linear regression.
- Gradient boosting performed very well for this dataset, capturing non-linear relationships.

## Tech Stack

- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib
- SciPy
- scikit-learn
- Jupyter Notebook

## Files in This Project

- `insurance_fixed.ipynb` — full analysis and modeling notebook
- `insurance.csv` — dataset used for prediction

## How to Run

```bash
jupyter notebook insurance_fixed.ipynb
```

## Project Summary

This project is a strong regression case study showing how feature engineering, interaction terms, and tree-based models can improve prediction quality. It is particularly useful for demonstrating practical machine learning work in a business or analytics portfolio.
