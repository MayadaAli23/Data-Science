# 🧠 HR Analytics: Employee Attrition Prediction

This project aims to predict employee attrition using real HR data from IBM. By analyzing employee demographics, job-related features, and satisfaction levels, we trained several machine learning models to identify employees at risk of leaving.

---

## 📁 Dataset

- **Source**: IBM HR Analytics Employee Attrition & Performance (available on Kaggle)
- **Rows**: 1470
- **Features**: 35
- **Target**: `Attrition` (Yes/No)

---

## ✅ Key Steps

1. **Data Exploration and Understanding**
2. **Data Cleaning and Preprocessing**
3. **Exploratory Data Analysis (EDA)**
4. **Feature Engineering**
5. **Model Building and Evaluation**
6. **Conclusion and Insights**

---

## 🔍 1. Data Exploration and Understanding

- Inspected dataset structure, data types, and shape.
- No missing values were found.
- Identified target variable imbalance: Only ~16% of employees had left.

---

## 🧹 2. Data Cleaning and Preprocessing

- Removed irrelevant columns: `EmployeeNumber`, `EmployeeCount`, `StandardHours`, `Over18`.
- Converted `Attrition` to binary format (`1` = Yes, `0` = No).
- Encoded categorical variables using **One-Hot Encoding**.
- Scaled numerical features using `StandardScaler`.

---

## 📊 3. Exploratory Data Analysis (EDA)

- Visualized relationships between key features and attrition:
  - Higher attrition among single employees and those working overtime.
  - Sales Representatives had the highest attrition rate.
  - Lower monthly income and fewer years at the company were linked to higher attrition.
- Used heatmaps and correlation charts to explore numeric relationships.

---

## 🏗️ 4. Feature Engineering

- Addressed **class imbalance** using **SMOTE** oversampling.
- Selected features based on correlation with target.
- Split the dataset into training and testing sets.

---

## 🤖 5. Model Building and Evaluation

### Models Trained:
- Logistic Regression
- Logistic Regression + SMOTE
- Random Forest (with and without tuning)
- XGBoost (with and without tuning)

### Evaluation Metrics:
Focus on **Recall (Yes)** due to business importance of catching true attrition cases.

| Model                       | Accuracy | Recall (Yes) | F1 Score (Yes) |
|----------------------------|----------|---------------|----------------|
| Logistic Regression        | 0.72     | 0.81          | 0.48           |
| Random Forest (Tuned)      | 0.81     | 0.36          | 0.38           |
| XGBoost (Tuned)            | 0.80     | 0.36          | 0.36           |

---

## 💡 6. Conclusion and Insights

- **Logistic Regression + SMOTE** gave the best recall, making it most suitable for predicting attrition.
- Most important features for attrition:
  - Overtime
  - Job Role: Sales Representative
  - Marital Status: Single
  - Monthly Income (lower)
  - YearsAtCompany (fewer)
- Hyperparameter tuning improved performance slightly, but class imbalance remains a key challenge.

---


## 🧰 Tools & Libraries

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Jupyter Notebook

---

## ✍️ Author

**Mayada Ali**  
Data Analyst & ML Enthusiast  
📫 [LinkedIn](https://www.linkedin.com/in/mayadaali23/) | [Email](mayada.ali.94@gmail.com)




