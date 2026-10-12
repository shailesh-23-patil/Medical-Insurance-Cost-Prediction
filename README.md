# Medical Insurance Cost Prediction

A machine learning project that analyzes medical insurance charges, identifies factors associated with healthcare costs, and builds regression models to estimate insurance expenses based on demographic and lifestyle-related attributes.

## Project Goal

The objective is to understand how age, BMI, smoking status, sex, region, and number of children relate to medical insurance charges. The project applies exploratory data analysis, feature engineering, and regression modeling to predict insurance costs.

## Dataset

- **Dataset:** `insurance.csv`
- **Target variable:** `charges`
- **Features:**
  - `age`
  - `sex`
  - `bmi`
  - `children`
  - `smoker`
  - `region`

## Data Cleaning and Preparation

The project includes the following preprocessing steps:

- Checks for missing values.
- Identifies and removes duplicate records where appropriate.
- Examines numerical and categorical features.
- Creates BMI categories for exploratory analysis.
- Encodes categorical variables for machine learning.
- Investigates an interaction between smoking status and obesity.

These steps help prepare the data for analysis and modeling.

## Exploratory Data Analysis (EDA)

The notebook explores relationships between insurance charges and different attributes:

- Differences in charges between smokers and non-smokers.
- Relationship between age and insurance costs.
- Effect of BMI on medical insurance charges.
- Differences in costs across regions and sexes.
- Influence of the number of children on insurance expenses.
- Distribution and skewness of insurance charges.

Visualizations help identify patterns and potential relationships within the dataset.

## Feature Engineering and Selection

The project investigates several techniques to improve the modeling workflow:

- BMI category creation.
- One-hot encoding for categorical variables.
- Pearson correlation analysis.
- Chi-square testing where appropriate for categorical features.
- An interaction feature, `smoker_obese`, to investigate whether smoking and obesity together are associated with insurance costs.

Feature engineering can help models capture relationships that may not be represented adequately by basic input features.

## Machine Learning Approach

The project compares multiple regression algorithms.

### Models

- Linear Regression — baseline model.
- Linear Regression with an interaction term.
- Random Forest Regressor.
- Gradient Boosting Regressor.

### Evaluation Metrics

- R² Score
- Adjusted R²
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- 5-fold cross-validation

These metrics help compare prediction accuracy and model performance.

## Key Areas of Analysis

The project investigates the following patterns:

- Smoking status and its association with insurance charges.
- The relationship between age, BMI, and insurance expenses.
- Whether interaction features improve predictions.
- Differences between linear and tree-based regression models.
- The ability of models to estimate costs on unseen data.

Actual findings and model evaluation results are available in the Jupyter Notebook.

## Technology Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-learn
- Jupyter Notebook

## Project Structure

```text
Medical-Insurance-Cost-Prediction/
├── insurance.csv
├── insurance_fixed.ipynb
└── README.md
```

## How to Run

### 1. Install the required libraries

Make sure Python and Jupyter Notebook are installed. Then run:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn jupyter
```

### 2. Open the project directory

Navigate to the folder containing the dataset and notebook.

### 3. Launch the notebook

```bash
jupyter notebook insurance_fixed.ipynb
```

### 4. Execute the notebook

Run the cells sequentially to reproduce the data analysis, preprocessing, model training, and evaluation.

## Project Objectives

- Analyze medical insurance cost data.
- Identify factors associated with insurance charges.
- Apply data cleaning and feature engineering.
- Compare regression algorithms.
- Evaluate predictive performance using multiple metrics.
- Demonstrate practical machine learning and data analysis skills.

## Conclusion

Medical Insurance Cost Prediction is a practical regression project demonstrating exploratory data analysis, feature engineering, preprocessing, model comparison, and predictive evaluation. It is suitable for a student machine learning portfolio and for demonstrating applied data science skills.

## Disclaimer

This project is intended for educational and analytical purposes. Predictions are estimates based on the available dataset and should not be treated as actual insurance quotations or financial advice.

---

**Author:** Shailesh Patil

**Project Type:** Machine Learning — Regression