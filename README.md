# Smart Loan Recovery System with Machine Learning

## Overview
The **Smart Loan Recovery System** leverages machine learning to predict loan defaults and optimize recovery strategies. By analyzing borrower profiles, payment behaviors, and risk factors, we can improve loan recovery efficiency and minimize financial losses.

## Dataset Overview
Our dataset consists of key attributes related to borrowers and their loan details:

- **Demographic Information**: Age, employment type, income level, and number of dependents.
- **Loan Details**: Loan amount, tenure, interest rate, and collateral value.
- **Repayment History**: Number of missed payments, days past due, and monthly EMI payments.
- **Collection Efforts**: Collection methods used, number of recovery attempts, and legal actions taken.
- **Loan Recovery Status**: Fully recovered, partially recovered, or outstanding.

## Graph Demonstrations: Data Analysis & Insights
### Analyzing Data Distribution and Relationships
- A **positive correlation** exists between loan amounts and monthly income.
- Higher income individuals tend to secure larger loans.
- The density curve indicates that **higher loan amounts** are more frequent among high-income borrowers.

### Analyzing Payment History
- **On-time payments** lead to **higher full recovery rates**.
- **Delayed payments** result in mixed recoveries, with some loans written off.
- **Missed payments** significantly reduce recovery chances.
- Fully recovered loans typically have **0-2 missed payments**, while written-off loans often have **6+ missed payments**.

### Analyzing Loan Recovery Based on Monthly Income
- Higher-income borrowers are more likely to **fully recover** their loans, even for large amounts.
- Borrowers in lower-income brackets face a **higher risk of partial recovery or write-offs**.
- Borrowers were segmented based on financial stability and repayment behavior:
  - **Segment 0**: Lower income, moderate loan sizes → **Higher risk**
  - **Segment 1**: Moderate to high loan amounts → **Financial stability**
  - **Segment 2**: Balanced distribution of borrowers
  - **Segment 3**: High loan amounts, high incomes → **Default-prone despite income**

## Building an Early Detection System for Loan Defaults
We trained a **Random Forest Classifier** to identify high-risk borrowers and assign recovery strategies:

- **Labelled borrowers** as high-risk based on segment classification.
- Selected key **financial and behavioral features**.
- Split data into **training and testing sets**.
- Trained the model to **predict default probability**.
- Applied model to test data to **generate risk scores**.

### Recovery Strategy Based on Risk Scores
Borrowers were categorized into three groups:

- **High-risk (score > 0.75)** → **Immediate legal action**
- **Moderate-risk (score 0.50 – 0.75)** → **Settlement offers & repayment plans**
- **Low-risk (score < 0.50)** → **Automated reminders**

This ensures cost-effective, personalized recovery strategies for each borrower.

## Summary
By leveraging **borrower profiles, payment behaviors, and machine learning**, we can develop a **smart loan recovery system** that:
- Identifies **high-risk borrowers** early.
- Predicts **default probabilities** accurately.
- Assigns **targeted recovery strategies** for cost-effective and efficient recovery.



