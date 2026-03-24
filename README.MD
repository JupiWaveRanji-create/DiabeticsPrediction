# HTIN5006 — Diabetes Prediction Analysis
**University of Sydney | Semester 1 2026**
#Ranjith Ambalakandy Kanakarajan
**HTIN5006 Foundation to Healthcare Data Science
**University of Sydney | ramb0160@uni.sydney.edu.au

## Project Overview
This project analyses the BRFSS 2015 dataset to predict 
diabetes outcomes using machine learning methods in R.
The analysis covers feature selection, class imbalance 
handling, lifestyle risk factors, and BMI stratification 
across five sub-questions.

## Research Question
How can machine learning methods be applied to predict 
diabetes-related outcomes and identify meaningful risk 
patterns in the BRFSS 2015 dataset?

## Sub-questions
- Q1: Which features predict prediabetes? (0 vs 1)
- Q2: How do feature selection methods compare? (0 vs 2)
- Q3: How does class imbalance handling affect performance?
- Q4: Which lifestyle factors are associated with diabetes?
- Q5: Does BMI stratification improve prediction?

## Dataset
- Source: CDC BRFSS 2015 via Kaggle
- Records: 253,680 survey responses
- Variables: 22 health indicators
- Link: https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset

## Methods Used
- Logistic Regression (baseline + SMOTE balanced)
- Random Forest (100 trees, importance = TRUE)
- XGBoost (gain-based feature importance)
- LASSO Regularisation (glmnet)
- SMOTE class balancing (themis / smotefamily)
- Correlation-based feature filtering

## Progress
| Task | Status |
|---|---|
| Data preprocessing | complete |
| Train/test split (80/20, stratified) | omplete |
| Logistic Regression (imbalanced) | omplete |
| Logistic Regression (SMOTE balanced) | omplete |
| Random Forest (100 trees) | omplete |
| RF Variable Importance Plot | omplete |
| ROC Curve Comparison | omplete |
| XGBoost training | n progress |
| LASSO feature selection | In progress |
| BMI stratification analysis | In progress |

## Output Files
| File | Description |
|---|---|
| `rf_varimp_plot.png` | Random Forest variable importance plot |
| `rf_importance_scores.csv` | Ranked importance scores for all 22 variables |
| `diabetes_analysis.Rmd` | Main R Markdown analysis file |
| `README.md` | Project overview |

## How to Run
1. Open `diabetes_analysis.Rmd` in RStudio
2. Install required packages (see first code chunk)
3. Click **Knit** to reproduce full analysis

## Key Packages Required
```r
install.packages(c("randomForest", "pROC", "caret", 
                   "glmnet", "xgboost", "themis", 
                   "ggplot2", "dplyr", "smotefamily"))
