
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
- Best ROC AUC after tuning: **0.82**
- Threshold adjusted to increase recall

### 2. Random Forest
- Tuned with GridSearchCV
- Best ROC AUC: **0.84**
- Strong balance between recall and precision

### 3. XGBoost
- Tuned with hyperparameters including `max_depth`, `learning_rate`, and `subsample`
- Best ROC AUC: **0.83**
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

##  Conclusion

In this project, we analyzed a medical dataset to predict the likelihood of diabetes in patients using various classification models.

We started with a baseline Logistic Regression model, then explored more complex algorithms such as Random Forest and XGBoost. For each model, we applied hyperparameter tuning using GridSearchCV and evaluated performance based on multiple metrics including Accuracy, Precision, Recall, F1 Score, and ROC AUC.

The results showed that:

XGBoost After Tuning achieved the best overall performance with an AUC of 0.83 and Accuracy of 0.75.
Logistic Regression After Tuning had the highest Recall (0.71), which is important in medical settings where identifying positive cases is critical.
Random Forest After Tuning also performed well, with a strong AUC of 0.837, offering a good balance between complexity and interpretability.
Through this analysis, we demonstrated how model selection, evaluation, and hyperparameter tuning play a crucial role in building effective machine learning solutions, especially in healthcare applications.

This project highlights the importance of precision and recall trade-offs in medical predictions, and the value of interpretability and model evaluation in responsible AI development.

## Final Comparison Between Models
<img width="1098" height="670" alt="image" src="https://github.com/user-attachments/assets/2036e433-b451-48ab-ad2c-2bbeadfd5324" />


