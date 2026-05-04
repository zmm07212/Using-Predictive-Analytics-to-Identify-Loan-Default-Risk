# Using Predictive Analytics to Identify Loan Default Risk

## Project Summary

This project uses predictive analytics and machine learning to predict whether a borrower is likely to default on a loan. The goal is to support credit risk assessment by identifying high-risk borrowers before loans are approved.

The analysis uses a credit risk dataset from Kaggle and applies exploratory data analysis, preprocessing, statistical modeling, machine learning, model comparison, hyperparameter tuning, and business interpretation.

## Objectives

The main objectives of this project are to:

- Identify borrower and loan characteristics associated with default risk
- Build models that predict whether a borrower will default
- Compare Logistic Regression, Random Forest, and Gradient Boosting models
- Evaluate model performance using classification metrics, confusion matrices, and ROC curves
- Recommend a final model that can support credit risk decision-making

## Dataset

Source: [Credit Risk Dataset by Laotse on Kaggle](https://www.kaggle.com/datasets/laotse/credit-risk-dataset)

The dataset contains over 32,000 loan observations and includes borrower, loan, and credit history variables.

Key variables include:

- person_age
- person_income
- person_home_ownership
- person_emp_length
- loan_intent
- loan_grade
- loan_amnt
- loan_int_rate
- loan_percent_income
- cb_person_default_on_file
- cb_person_cred_hist_length
- loan_status

The target variable is loan_status, where:

- 0 = non-default
- 1 = default

## Tools and Libraries

This project was completed using Python in Google Colab.

Libraries used:

- pandas
- NumPy
- matplotlib
- seaborn
- scikit-learn
- statsmodels

## Notebook

The full analysis notebook is included in this repository:

- [Martin_Maxwell_ISOM835_Project.ipynb](https://colab.research.google.com/drive/1DJvZhbe46LaLqhzSQnPTO0MHIUoHXXkF?usp=sharing)

## Instructions to Run the Analysis

1. Download or clone this repository.
2. Open Martin_Maxwell_ISOM835_Project.ipynb in Google Colab.
3. Make sure credit_risk_dataset.csv is in the same working directory as the notebook.
4. Run the notebook cells from top to bottom.
5. The notebook will load the data, perform EDA, preprocess the dataset, train models, evaluate performance, and produce figures/tables used in the final report.

## Models Used

Three models were developed and evaluated:

- Logistic Regression
- Random Forest
- Gradient Boosting

Logistic Regression was used as an interpretable baseline model. Random Forest and Gradient Boosting were used to improve predictive performance and capture nonlinear relationships.

## Model Results

| Model | Accuracy | Precision Default | Recall Default | F1 Score Default | AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | 0.86 | 0.76 | 0.54 | 0.64 | 0.87 |
| Random Forest | 0.93 | 0.94 | 0.72 | 0.82 | 0.93 |
| Gradient Boosting | 0.92 | 0.92 | 0.69 | 0.79 | 0.93 |

Random Forest was selected as the final model because it achieved the best balance of accuracy and default detection.

## Key Findings

- loan_percent_income was the most important predictor of default.
- Tree-based models outperformed Logistic Regression.
- Random Forest produced the fewest missed default cases.
- Recall for the default class was the most important metric because missed defaults create financial risk for lenders.

## Repository Contents

- README.md: Project overview and summary
- .gitignore: Files and folders excluded from version control
- credit_risk_dataset.csv: Dataset used for analysis
- Martin_Maxwell_ISOM835_Project.pdf: Final written report
- Martin_Maxwell_ISOM835_Project.ipynb: Full analysis notebook
- visualizations/: Figures used in the report and notebook

## Author

Maxwell Martin  
FIN 835 Predictive Analytics and Machine Learning
