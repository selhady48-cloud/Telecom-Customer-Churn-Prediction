# Customer Churn Prediction for Interconnect

## Project Overview
This project builds a machine learning model to predict customer churn for Interconnect, a telecom operator. The goal is to identify customers who are likely to leave so the company can target them with retention offers such as promotional pricing or alternative plans.

## Business Problem
Customer churn directly affects revenue and customer lifetime value. Interconnect wants to detect at-risk customers early in order to improve retention and reduce avoidable losses.

## Data
The dataset consists of customer information collected from four sources:

- `contract.csv` — contract details
- `personal.csv` — personal customer information
- `internet.csv` — internet service details
- `phone.csv` — phone service details

The target variable was created from the `EndDate` column:
- `0` = active customer (`EndDate == "No"`)
- `1` = churned customer (`EndDate != "No"`)

## Project Workflow
1. Merged the datasets using `customerID`
2. Cleaned and prepared the data
3. Performed exploratory data analysis
4. Engineered features such as customer tenure
5. Trained and compared multiple classification models
6. Selected the best model based on ROC-AUC

## Models Tested
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting

## Results
The best-performing model was **Gradient Boosting**:

- **ROC-AUC:** 0.884
- **Accuracy:** 0.833

This exceeded the project target and placed the model in the highest performance tier.

## Key Findings
The strongest predictors of churn were:

- Customer tenure
- Contract type
- Internet service type
- Payment method
- Monthly charges

Customers with shorter tenure, month-to-month contracts, fiber optic internet, and higher monthly charges were more likely to churn.

## Business Recommendations
Interconnect should prioritize retention efforts for:

- newer customers
- customers on month-to-month contracts
- fiber optic users
- customers with higher monthly charges
- customers paying by electronic check

Targeted promotions, service improvements, and contract incentives could help reduce churn in these segments.

## Tools and Libraries
- Python
- pandas
- numpy
- scikit-learn
- matplotlib
- Jupyter Notebook

## How to Run
1. Clone the repository
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
