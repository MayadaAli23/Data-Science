
# Diabetes Prediction using Machine Learning

This project aims to build predictive models that can identify whether a person is diabetic based on medical attributes. It includes data preprocessing, imputation, model training, evaluation, and comparison across different classifiers.

##  Dataset
The dataset used is the **Pima Indians Diabetes Database** from Kaggle. It contains medical information of female patients and whether they are diagnosed with diabetes.

**Features include:**
- Pregnancies
- Glucose
- BloodPressure
- SkinThickness
- Insulin
- BMI
- DiabetesPedigreeFunction
- Age

Target variable: `Outcome` (1 = diabetic, 0 = non-diabetic)

##  Preprocessing

- Replaced zero values in key features (e.g., Glucose, BloodPressure, BMI) with `NaN`
- Imputed missing values using **MICE (Multiple Imputation by Chained Equations)**
- Scaled the features using **StandardScaler**

##  Models Applied

We applied and compared the performance of the following models:

### 1. Logistic Regression
- Baseline model
- Used L2 regularization
- Best ROC AUC after tuning: **0.83**
- Threshold adjusted to increase recall

### 2. Random Forest
- Tuned with GridSearchCV
- Best ROC AUC: **0.84**
- Strong balance between recall and precision

### 3. XGBoost
- Tuned with hyperparameters including `max_depth`, `learning_rate`, and `subsample`
- Best ROC AUC: **0.85**
- Highest overall performance

##  Evaluation Metrics
For all models, the following metrics were used:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC AUC
- Confusion Matrix
- Precision-Recall Threshold Tuning

##  ROC Curve Comparison

ROC curves were plotted to visually compare model performance and select the most appropriate threshold.

##  Key Takeaways

- XGBoost achieved the best performance with AUC = **0.85**
- Logistic Regression gave reasonable results with good interpretability
- Precision-Recall tuning helped balance Type I and II errors depending on project goals

## Final Comparison Between Models
<img width="1098" height="670" alt="image" src="https://github.com/user-attachments/assets/2036e433-b451-48ab-ad2c-2bbeadfd5324" />


