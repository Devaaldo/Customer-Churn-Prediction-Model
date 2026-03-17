# Customer Churn Prediction Model

A machine learning project for predicting customer churn in banking using multiple classification algorithms with exploratory data analysis and model comparison.

## Project Overview

This project implements and compares five classification algorithms to predict whether a bank customer will churn. The analysis includes exploratory data analysis, data preprocessing, model training, and evaluation metrics.

Dataset: 10,000 bank customers with 14 features
Target: Customer churn (Exited: 1 = churned, 0 = retained)

## Dataset Features

- CreditScore: Customer's credit score
- Geography: Country (France, Germany, Spain)
- Gender: Customer gender
- Age: Customer's age
- Tenure: Years as customer
- Balance: Account balance
- NumOfProducts: Number of products owned
- HasCrCard: Has credit card (1=Yes, 0=No)
- IsActiveMember: Is active member (1=Yes, 0=No)
- EstimatedSalary: Annual estimated salary
- Exited: Target variable (1=Churned, 0=Retained)

## Data Processing

1. Removed non-predictive columns (RowNumber, CustomerId, Surname)
2. Encoded categorical variables (Geography, Gender) using LabelEncoder
3. Normalized numerical features using MinMaxScaler to [0, 1]
4. Split data: 80% training (8,000), 20% testing (2,000)

## Models and Performance

| Model                  | Accuracy | Precision | Recall | F1-Score |
| ---------------------- | -------- | --------- | ------ | -------- |
| K-Nearest Neighbors    | 82.40%   | 59.53%    | 32.57% | 0.421    |
| Decision Tree          | 77.95%   | 44.67%    | 51.15% | 0.477    |
| Random Forest          | 86.65%   | 76.25%    | 46.56% | 0.578    |
| Support Vector Machine | 85.30%   | 82.78%    | 31.81% | 0.460    |
| Naive Bayes            | 82.85%   | 68.12%    | 23.92% | 0.354    |

Best performing model: Random Forest with 86.65% accuracy and 0.578 F1-Score.

## Technologies Used

- Python 3
- pandas, numpy
- scikit-learn
- seaborn, matplotlib

## Running the Project

1. Open the Jupyter notebook:

   ```
   jupyter notebook identify_customers_churn.ipynb
   ```

2. Run all cells to execute the full pipeline from data loading through model evaluation

## Results

Random Forest achieved the best overall performance with the highest accuracy and balanced precision-recall metrics. The model demonstrated superior ability to identify potential churners while maintaining reasonable precision.

## Project Structure

```
Identify-Customer-Churn/
├── identify_customers_churn.ipynb
├── README.md
└── data/
    └── house-prices-advanced-regression-techniques/
```
