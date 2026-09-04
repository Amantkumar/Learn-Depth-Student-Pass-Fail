# Problem 07 | Student Placement Eligibility

## 1. Objective
Build a binary classification solution to predict whether a student belongs to the positive placement-eligibility/event class.

## 2. Dataset
The supplied CSV contains 1,000 rows and 7 columns.
Predictors: cgpa, attendance_pct, coding_score, projects_completed, internship_months, backlogs.
Target: target (0/1).

## 3. Data Quality
- Missing values: 0
- Duplicate rows: 0
- Target class 0: 500 (50.0%)
- Target class 1: 500 (50.0%)
- Observed ranges were checked for all predictors.
- IQR flags: cgpa=12, attendance_pct=0, coding_score=11, projects_completed=9, internship_months=0, backlogs=9. These were treated as statistical flags rather than automatically invalid values.

## 4. Preprocessing
No imputation was required because there were no missing values. No duplicate removal was required. Predictors were standardized using StandardScaler. An 80/20 stratified train-test split was used with random_state=42.

## 5. Model
Logistic Regression baseline with:
- solver: lbfgs
- penalty: L2
- C: 1.0
- max_iter: 1000
- random_state: 42

## 6. Test Evaluation
| Metric | Score |
|---|---:|
| Accuracy | 0.7000 |
| Precision | 0.6887 |
| Recall | 0.7300 |
| F1-score | 0.7087 |
| ROC-AUC | 0.7874 |

### Confusion Matrix
TN=67, FP=33, FN=27, TP=73.

## 7. Coefficient Interpretation
Because predictors were standardized, coefficient signs show the direction of association with the positive class. Positive coefficients increase modeled log-odds of target=1; negative coefficients decrease them. This is an association in the fitted model, not causal evidence.

## 8. Limitations and Improvements
The dataset contains only the supplied variables and may not capture every real-world placement factor. Performance may not generalize to other student populations. Future work could use cross-validation, threshold tuning, regularization comparison, external validation, and alternative classification models.

## 9. Conclusion
The project provides a reproducible implementation of data inspection, quality checking, preprocessing, Logistic Regression, metric-based evaluation, confusion-matrix analysis, ROC-AUC analysis, and coefficient interpretation.
