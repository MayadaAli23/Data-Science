
# 🏥 Medical Cost Prediction Project

This project focuses on predicting individual medical insurance charges based on demographic and health-related features using various regression models. The goal is to find the most accurate and interpretable model through data analysis, model evaluation, and hyperparameter tuning.

---

## 📁 Dataset

- **Source**: [Kaggle - Medical Cost Personal Dataset](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Features**:
  - `age`: Age of the primary beneficiary
  - `sex`: Gender (male/female)
  - `bmi`: Body mass index
  - `children`: Number of children covered by health insurance
  - `smoker`: Whether the person smokes
  - `region`: Residential region in the US
  - `charges`: Medical insurance cost (target)

---

## 🧪 Project Steps

1. **Data Exploration & Cleaning**
   - Checked for missing values, duplicates, and outliers
   - Handled duplicates and analyzed numeric distributions

2. **Exploratory Data Analysis (EDA)**
   - Visualized relationships between charges and features
   - Found clear patterns, especially with `smoker` and `bmi`

3. **Modeling**
   - Trained multiple regression models:
     - Linear Regression
     - Gradient Boosting
     - Random Forest (with tuning)
     - XGBoost (with tuning)

4. **Model Evaluation**
   - Used metrics: MAE, RMSE, and R² Score
   - Compared models using a heatmap

---

## 📊 Model Performance Comparison

| Model                   | MAE     | RMSE    | R² Score |
|-------------------------|---------|---------|----------|
| Linear Regression       | 4177.05 | 5956.34 | 0.81     |
| Gradient Boosting       | 2517.47 | 4268.28 | 0.90     |
| Random Forest (Tuned)   | 2413.17 | 4231.91 | 0.90     |
| XGBoost (Tuned)         | 2530.86 | 4322.45 | 0.90     |

📌 The **Random Forest (Tuned)** model achieved the best overall performance.

---

## 🔥 Key Insights

- Tree-based models clearly outperform Linear Regression.
- Tuning significantly improved performance (especially for XGBoost).
- Features like **smoking status**, **BMI**, and **age** have a strong impact on medical charges.
- All ensemble models explained 90% of the variance in the target variable (R² = 0.90).

---

## 📷 Visual Highlights

### 🔍 Heatmap of Model Comparison

<img width="943" height="539" alt="image" src="https://github.com/user-attachments/assets/b2fdb432-7942-4966-93a1-13b6938fe50f" />

---

## ✅ Conclusion

This project demonstrates a complete end-to-end regression pipeline:
- Data preprocessing and visualization
- Model building and evaluation
- Hyperparameter tuning and model comparison

🧠 It serves as a valuable addition to a data science portfolio, showcasing practical skills in regression, analysis, and decision making.

---

## 🚀 Tools Used

- Python (Pandas, NumPy)
- Scikit-learn
- XGBoost
- Seaborn & Matplotlib
- Jupyter Notebook

---

## 📌 Author

**Mayada Ali**  
_Data Analyst | Machine Learning Enthusiast_  
📫 [LinkedIn](https://www.linkedin.com/in/mayadaali23/) | [Email](mayada.ali.94@gmail.com)
