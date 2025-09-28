# 🏦 Loan Approval Prediction

This project is designed to predict whether a loan application will be approved based on various applicant features.
The primary goal is to build a robust classification model that identifies the key factors influencing loan approval and can handle class imbalance effectively.

---

## 📌 Project Overview
- **Data Preprocessing**: Cleaned the dataset by removing irrelevant columns (loan_id) and extra spaces, and encoded all categorical variables (Education, Self_Employed) into a numerical format.
- **Exploratory Data Analysis (EDA)**: Utilized count plots, box plots, and a correlation heatmap to analyze patterns. The key insight was the strong relationship between a high CIBIL score and loan approval.
- **Handling Imbalance**: Applied the **SMOTE (Synthetic Minority Over-sampling Technique)** on the training data to address the significant class imbalance between approved and rejected loans.
- **Models Trained**: Implemented Logistic Regression as a stable baseline and a Decision Tree Classifier to capture potentially non-linear relationships.
- **Evaluation**: Assessed model performance using Accuracy, Precision, Recall, and F1-score, which are crucial metrics for imbalanced classification tasks.

---

## 🛠️ Tech Stack
- **Python**
- **KaggleHub** → Dataset downloading and management
- **Pandas, NumPy** → Data manipulation and numerical operations
- **Matplotlib, Seaborn** → Data visualization
- **Scikit-learn** → Machine learning models and evaluation
- **Imbalanced-learn** → SMOTE for handling imbalanced data

---

## 📂 Dataset
The dataset contains applicant information, including:
- **Financials**: `income_annum`, `loan_amount`, `loan_term`
- **Credit History**: `cibil_score` (most critical feature)
- **Assets**: `residential_assets_value`, `commercial_assets_value`, etc.
- **Demographics**: `no_of_dependents`, `education`, `self_employed`
- **Loan Status** (Approved / Rejected) → Target variable

---

## 📊 Data & Model Analysis
- Cleaned and prepared all features for modeling, ensuring they were numerical.
- Created visualizations to understand feature distributions and their relationship with the target.
- Split the data into 80% training and 20% testing sets to ensure a fair evaluation.
- Corrected class imbalance in the training set using SMOTE before model fitting.
- Compared the performance of a linear model against a tree-based model.

---

## 🤖 Models Implemented
- **Logistic Regression** → A reliable and interpretable linear model that serves as a strong baseline.
- **Decision Tree Classifier** → A non-linear model capable of learning complex decision boundaries.

---

## 📈 Model Evaluation & Insights
- The **CIBIL score** was overwhelmingly the most significant predictor of loan approval.
- Applying **SMOTE** was crucial for improving the model's ability to correctly identify rejected loans (the minority class).
- Both models achieved high accuracy (>97%), but the Decision Tree showed slightly better precision and recall for the 'Rejected' class.
- The project demonstrates a complete workflow for a real-world classification problem.

---

## 📷 Visualizations
- **Count Plot** of Loan Approval Status
- **Box Plot** of CIBIL Score vs. Loan Status
- **Correlation Heatmap** of all features against the target variable
