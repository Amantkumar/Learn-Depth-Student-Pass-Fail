# PROBLEM 07 | STUDENT PLACEMENT ELIGIBILITY

## Project Overview

This project focuses on predicting whether a student is likely to meet the placement eligibility criteria using a binary classification approach.

## Objective

To build a simple and reproducible binary classification solution for the student placement eligibility use case.

## Dataset

**Dataset:** `dataset_07_student_placement_eligibility.csv`

The dataset contains student-related information used to predict placement eligibility.

## Target Variable

- `target = 1` → Positive class / eligible
- `target = 0` → Negative class / not eligible

## Input Variables

- CGPA
- Attendance Percentage
- Coding Score
- Projects Completed
- Internship Months
- Backlogs

## Work Performed

- Inspected the dataset and understood the variables and target.
- Checked missing values and duplicate records.
- Examined class balance and data-quality issues.
- Performed appropriate preprocessing.
- Used a train/test split while avoiding data leakage.
- Trained a Logistic Regression model.
- Evaluated the model using Accuracy, Precision, Recall, F1-Score and ROC-AUC.
- Analyzed the confusion matrix.
- Interpreted Logistic Regression coefficients.
- Discussed limitations and possible improvements.

## Algorithm

### Logistic Regression

Logistic Regression was used as the baseline classification algorithm because the target variable represents two classes.

## Evaluation

The project includes:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

Detailed results are available in the Jupyter Notebook and supporting files.

## Project Files

- `dataset_07_student_placement_eligibility.csv` — Dataset
- `Problem_07_Student_Placement_Eligibility.ipynb` — Source notebook
- `evaluation_metrics.xlsx` — Evaluation metrics
- `logistic_coefficients.xlsx` — Model coefficients
- `Problem_07_Student_Placement_Eligibility.md` — Short project report

## Conclusion

This project demonstrates a complete machine-learning workflow for student placement eligibility, covering data inspection, preprocessing, Logistic Regression, evaluation, confusion-matrix analysis and feature interpretation.
