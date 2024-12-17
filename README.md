# Machine Learning course project: T12 - Factors of success in abstract theoretical courses
Team: Pirjo Vainjärv, Anna Maria Tammin, Kaidi Tootmaa, Hanna-Maria Kukk

The goal is to find activity patterns to separate students by efficiency and thus predicting the students final score.

Given dataset of student activity in course webpage: activity_log_A.csv; activity_log_B.csv; grades_A.csv; grades_B.csv.
Description of given data can be found in 'data_description.txt' file.

Questions we try to find answers to:
How to predict final grade based on activity?
What are the activity patterns that correlate with a good grade?
What to recommend for low achieving students?

Activity log data had some random typos which we manually fixed, and following analysis uses fixed data: activity_log_A_parandatud.csv; activity_log_B_parandatud.csv.

First we searched for meaningful features which correlate with the grade.
Making of the found important features can be followed in 'making_features.ipynb'.
This code puts together training data for modeling: 'all_features.csv'.

Made training data is used in 'testing_models.ipynb' which tries normalization (StandardScaler), regularization (Lasso), oversampling (SMOTE), Random Forest Classifier, Gradient Boosting Classifier, Tree Classifier, K-Neighbors Classifier, Logistic Regression, AdaBoost Classifier, XGB Classifier, Random Forest Regressor, Gradient Boosting Regressor, Linear Regression, SVR, and Decision Tree Regressor on training data.

The used evaluation metric is MAE (mean absolute error).
Our best model reached MAE of 0.74 for validation data. For final model MAE for testing data is 1.55.
