# Diabetes Prediction Project

## Overview
This project aims to predict the likelihood of diabetes in patients using various machine learning models. The dataset used is derived from a structured medical dataset containing features such as glucose levels, BMI, insulin, and age.

## Dataset Information
The dataset is read from `data/diabetes.csv`, and it contains the following features:

### Independent Features:
- `Pregnancies`
- `Glucose`
- `BloodPressure`
- `SkinThickness`
- `Insulin`
- `BMI`
- `DiabetesPedigreeFunction`
- `Age`

### Dependent Feature:
- `Outcome` (0 = No Diabetes, 1 = Diabetes)

## Exploratory Data Analysis (EDA)

1. **Descriptive Statistics:**
   - Used `df.describe()` to analyze the statistical distribution.
   - Checked missing values using `df.isnull().sum()`.
   - Visualized the distribution of numerical variables using histograms and density plots.

2. **Data Visualization:**
   - Histogram of `Age` variable.
   - Density plots for each numerical feature.
   - Pie chart and count plot for `Outcome`.
   - Heatmap of feature correlation.

## Data Preprocessing

- Handled missing values by replacing `0` with `NaN` and imputing them with median values.
- Performed outlier detection using:
  - **Interquartile Range (IQR)**
  - **Local Outlier Factor (LOF)**
- Feature engineering:
  - Categorized BMI into `Underweight`, `Normal`, `Overweight`, and `Obesity` classes.
  - Created new categorical features for `Insulin` and `Glucose` levels.
- Applied one-hot encoding to categorical features.
- Scaled numerical data using `RobustScaler` and `StandardScaler`.

## Machine Learning Models

The dataset was split into `80-20` train-test split, and the following models were implemented:

1. **Logistic Regression**
   - Achieved an accuracy of `log_reg_acc`.
   - Evaluated using confusion matrix and classification report.

2. **K-Nearest Neighbors (KNN)**
   - Implemented KNN classifier with default parameters.
   - Evaluated using accuracy score, confusion matrix, and classification report.

3. **Support Vector Machine (SVM)**
   - Used `GridSearchCV` to find the best `C` and `gamma` values.
   - Trained the final model with best parameters.
   - Evaluated on test data.

4. **Decision Tree Classifier**
   - Trained using default parameters.
   - Evaluated using classification metrics.

5. **Random Forest Classifier**
   - Used ensemble learning to improve performance.
   - Evaluated using ROC curves.

6. **Gradient Boosting Classifier**
   - Used boosting technique to enhance accuracy.
   - Compared results with other models.

## Performance Evaluation

- Used `accuracy_score`, `confusion_matrix`, `classification_report`, and `roc_auc_score` for performance evaluation.
- Plotted ROC curves for model comparison.
- Conducted cross-validation to validate generalization performance.

## Conclusion
The Diabetes Prediction project successfully analyzes and classifies patients as diabetic or non-diabetic using multiple machine learning models. The best-performing model can be chosen based on accuracy and ROC analysis. Further improvements can be made by hyperparameter tuning and using deep learning techniques.

## Future Enhancements
- Use deep learning models for improved prediction.
- Implement feature selection to reduce dimensionality.
- Test with additional datasets for better generalization.
- Deploy the model as a web application for real-time predictions.

---



