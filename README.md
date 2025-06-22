# Medical Insurance Cost Analysis & Regression Modeling

This project investigates the financial impact of various demographic and lifestyle factors on annual medical insurance charges. Using statistical analysis and linear modeling, we extract actionable insights and build predictive frameworks to better understand the drivers of healthcare costs.

---

## Project Contents

- **`Medical Insurance Data Analysis.ipynb`**  
  An in-depth Jupyter Notebook containing the full workflow — from preprocessing and exploration to statistical testing and modeling.

- **`insurance.csv`**  
  The lightly modified dataset used throughout this project. The original dataset was extended with simulated missing values and noise to better reflect real-world data quality and increase analytical depth. 
  - Original dataset Link: [U.S. Health Insurance Dataset (Kaggle)](https://www.kaggle.com/datasets/teertha/ushealthinsurancedataset)

---

## Dataset Overview

The dataset includes 1,365 records, each of which captures the profile of an insurance policyholder and includes:

- `age`: Age of the individual  
- `sex`: Gender  
- `bmi`: Body Mass Index  
- `children`: Number of dependents  
- `smoker`: Smoking status  
- `region`: Residential region in the U.S.  
- `charges`: Annual medical insurance cost (target variable)

To enable robust modeling, categorical variables were encoded, and the target variable was log-transformed to address skewness.

---

## Analytical Pipeline

### **Part A: Data Preprocessing & Exploratory Analysis**
- Cleaned and validated data, addressed missing entries.
- Encoded categorical features (binary and one-hot encoding).
- Visualized distributions, trends, and outliers using histograms, boxplots, and scatterplots.
- Constructed a **correlation heatmap** to evaluate relationships between numerical variables.

### **Part B: Hypothesis Testing**
- Applied statistical tests to evaluate the impact of specific factors on insurance charges:
  - **T-tests** and **ANOVA** to assess mean differences across groups.
  - **Chi-square tests** for independence on categorical variables.
- **Top hypotheses supported**:
  1. **Smokers incur significantly higher charges** than non-smokers.
  2. **Charges increase with age**, consistent with higher medical risks.
  3. **Higher BMI** is weakly associated with increased costs, though not as impactful as smoking.

### **Part C: Linear Regression Modeling**
- **Simple Linear Regression (SLR)**: Modeled the log-transformed charges against each of `age`, `bmi`, and `smoker` individually to evaluate baseline predictive strength.
- **Multiple Linear Regression (MLR)**: Developed two comprehensive models:
  - **Core Trio Model** using `age`, `bmi`, and `smoker`
  - **Full Feature Model** incorporating all encoded variables (`sex`, `children`, `region` dummies, etc.)
- Evaluated models using R², RMSE, MAE, and diagnostic plots to assess fit and generalization.

---

## Key Insights

- **Smoking status** remains the dominant predictor across models, significantly raising costs even after controlling for other variables.
- **Age** shows a steady, linear impact on charges, but less extreme than smoking.
- **BMI**, while intuitively important, shows limited standalone predictive power.
- The **multivariate models** perform substantially better than univariate models, capturing the combined effects of features and reducing prediction error.

---

## Conclusion

Through this analysis, a systematic approach has been demonstrated to model real-world healthcare cost data. From simulating missing values to hypothesis-driven modeling, this project illustrates how domain knowledge, EDA, and statistical rigor can work in tandem to extract meaningful patterns and deliver predictive insights.

---
