# Fraud-Detection-in-Transactions

## Project Overview
This project aims to predict fraudulent transactions using machine learning techniques. Fraud detection is a crucial challenge in the financial industry, where accurately identifying fraudulent transactions can save significant financial losses. The project explores various classification models, including **Logistic Regression**, **Random Forest**, and **XGBClassifier**, to address this issue effectively.

## Key Features
- **Exploratory Data Analysis (EDA)**: Understand the dataset, feature distributions, and class imbalance.
- **Class Imbalance Handling**: Used **SMOTE** (Synthetic Minority Over-sampling Technique) to balance the dataset.
- **Feature Engineering**: Created new features such as `errorBalanceOrig` and `errorBalanceDest` to improve model performance.
- **Modeling**: Implemented multiple machine learning models to predict fraud, including:
  - **Logistic Regression**
  - **Random Forest**
  - **XGBClassifier**
- **Evaluation**: Evaluated models using metrics such as accuracy, precision, recall, F1-score, and confusion matrices.

## Dataset
The dataset contains transaction details such as:
- `step`: Time step of the transaction
- `type`: Type of transaction (e.g., payment, transfer)
- `amount`: Amount of money involved in the transaction
- `oldbalanceOrg`: The balance of the origin account before the transaction
- `newbalanceOrig`: The balance of the origin account after the transaction
- `nameOrig` and `nameDest`: IDs for the origin and destination accounts
- `isFraud`: Whether the transaction is fraudulent (1) or not (0)
- `isFlaggedFraud`: Whether the transaction is flagged as potentially fraudulent

## Approach
1. **Data Preprocessing**:
   - Checked for missing values and outliers.
   - Standardized feature values where necessary.
   
2. **Exploratory Data Analysis**:
   - Analyzed data distribution and class imbalance.
   - Identified patterns and correlations between transaction types, amounts, and fraudulent activity.

3. **Model Training**:
   - Split the data into training and testing sets.
   - Applied **SMOTE** to handle class imbalance.
   - Trained and tuned the following models:
     - Logistic Regression
     - Random Forest
     - XGBClassifier

4. **Evaluation**:
   - Used accuracy, precision, recall, F1-score, and confusion matrices to evaluate the models.
   - Achieved high performance, with **Random Forest** and **XGBClassifier** performing particularly well on imbalanced data.

## Results
- **Random Forest**:
  - Accuracy: **99.9%**
  - F1-score: **0.97**
  - Best performance across all types of transactions.

- **XGBClassifier**:
  - Handled the class imbalance effectively, showing high precision for fraudulent transactions.

## Conclusion
This project demonstrated the effectiveness of using machine learning models like **Random Forest** and **XGBClassifier** for fraud detection in financial transactions. Handling class imbalance using **SMOTE** and engineering new features significantly improved the model's ability to detect fraud with high accuracy and minimal false positives.

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/Bilal-Shabbir/fraud-detection.git
