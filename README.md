# Multiple-Linear-Regression-Marketing-Analysis

## Multiple Linear Regression Evaluation

# Multi-Channel Marketing Analysis Using Multiple Linear Regression

## Project Overview

This project analyzes the impact of multiple marketing channels on Sales performance using Multiple Linear Regression. The objective is to identify which marketing variables significantly influence Sales and provide data-driven recommendations for marketing budget allocation.

The analysis includes exploratory data analysis (EDA), multicollinearity assessment, regression modeling, diagnostic testing, statistical interpretation, and business recommendations.

---

## Project Objectives

* Load and inspect the marketing dataset
* Perform exploratory data analysis (EDA)
* Assess multicollinearity using Correlation Matrix and Variance Inflation Factor (VIF)
* Build a Multiple Linear Regression model using Ordinary Least Squares (OLS)
* Evaluate model performance using R-squared and Adjusted R-squared
* Assess predictor significance using p-values
* Validate regression assumptions using diagnostic plots
* Interpret regression coefficients in a business context
* Provide evidence-based marketing budget recommendations

---

## Dataset Variables

| Variable         | Description                          |
| ---------------- | ------------------------------------ |
| Radio            | Radio advertising expenditure        |
| Social Media     | Social media advertising expenditure |
| TV_Low           | Low TV advertising category          |
| TV_Medium        | Medium TV advertising category       |
| Influencer_Mega  | Mega Influencer category             |
| Influencer_Micro | Micro Influencer category            |
| Influencer_Nano  | Nano Influencer category             |
| Sales            | Product sales (Target Variable)      |

---

## Methodology

The project followed the steps below:

1. Data Loading and Inspection
2. Missing Value Assessment
3. Exploratory Data Analysis (EDA)
4. Correlation Analysis
5. Multicollinearity Testing (VIF)
6. Multiple Linear Regression Modeling
7. Model Evaluation
8. Residual Diagnostic Testing
9. Business Interpretation and Recommendations

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Statsmodels
* SciPy
* Jupyter Notebook

---

## Installation

Install the required libraries using:

```bash
pip install -r requirements.txt
```

Or install manually:

```bash
pip install pandas numpy matplotlib seaborn statsmodels scipy
```

---

## Running the Project

### 1. Clone the repository

```bash
git clone <repository-url>
```

### 2. Navigate to the project folder

```bash
cd Multiple-Linear-Regression-Marketing-Analysis
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open

```text
multiple_regression_analysis.ipynb
```

### 5. Run all cells sequentially

---

## Multicollinearity Analysis

Variance Inflation Factor (VIF) was used to evaluate multicollinearity among predictors.

| Variable         |  VIF |
| ---------------- | ---: |
| Radio            | 6.70 |
| Social Media     | 5.34 |
| TV_Low           | 1.66 |
| TV_Medium        | 1.66 |
| Influencer_Mega  | 2.00 |
| Influencer_Micro | 2.08 |
| Influencer_Nano  | 2.08 |

Although Radio and Social Media exhibited moderate multicollinearity, all VIF values remained below the critical threshold of 10. Therefore, all predictors were retained in the regression model.

---

## Model Performance

### OLS Regression Results

| Metric             | Value     |
| ------------------ | --------- |
| R-squared          | 0.904     |
| Adjusted R-squared | 0.903     |
| F-statistic        | 760.4     |
| Prob(F-statistic)  | 1.82e-282 |
| Observations       | 572       |

The model explained approximately **90.3% of the variation in Sales**, indicating excellent predictive performance.

---

## Key Findings

### Significant Predictors

| Variable  | Coefficient | P-value |
| --------- | ----------: | ------: |
| Radio     |      2.9735 | < 0.001 |
| TV_Low    |   -154.5736 | < 0.001 |
| TV_Medium |    -75.5947 | < 0.001 |

### Non-Significant Predictors

* Social Media (p = 0.837)
* Influencer_Mega (p = 0.471)
* Influencer_Micro (p = 0.385)
* Influencer_Nano (p = 0.811)

---

## Regression Interpretation

### Radio Advertising

Holding all other variables constant, a one-unit increase in Radio advertising expenditure is associated with an average increase of approximately **2.97 units in Sales**.

### TV Advertising Categories

Relative to the reference TV category:

* TV_Low is associated with approximately **154.57 fewer Sales units**
* TV_Medium is associated with approximately **75.59 fewer Sales units**

These findings indicate that maintaining higher levels of TV advertising contributes positively to Sales performance.

---

## Diagnostic Testing

### Normality

Residual histograms and Q-Q plots indicated that residuals were approximately normally distributed, with only minor deviations in the tails.

### Linearity

Residuals were randomly distributed around zero, supporting the linearity assumption.

### Homoscedasticity

Residual variance remained relatively constant across fitted values, indicating acceptable homoscedasticity.

---

## Recommendation

Based on the regression analysis:

* Prioritize Radio advertising investments, as Radio demonstrated the strongest positive and statistically significant relationship with Sales.
* Maintain adequate TV advertising levels, as lower TV investment categories were associated with substantial decreases in Sales.
* Reassess Social Media and Influencer marketing expenditures, as these variables did not exhibit statistically significant effects after controlling for other predictors.
* Future analyses may explore simplified models by removing non-significant variables and comparing Adjusted R-squared performance.

Overall, the model provides strong evidence that Radio advertising and sustained TV investment are the most effective drivers of Sales within this dataset.

---

## Repository Structure

```text
Multiple-Linear-Regression-Marketing-Analysis/
│
├── README.md
├── marketing_sales_data.csv
├── multiple_regression_analysis.ipynb
├── requirements.txt
│
└── images/
    ├── correlation_matrix.png
    ├── residual_histogram.png
    ├── qq_plot.png
    └── residual_vs_fitted.png
```

---

## Author

**Godwill Morgan Lekwa**
