Diabetes Prediction using Random Forest: This project implements a machine learning pipeline to predict the onset of diabetes based on diagnostic measurements from the Pima Indians Diabetes Dataset. It uses a Random Forest Classifier to achieve high predictive accuracy and interpretability.

Overview : The script performs the following end-to-end tasks: 1.Data Loading: Fetches the Pima Indians dataset directly from a remote repository. 2.Data Cleaning: Identifies physically impossible "0" values in features like Glucose and BMI, treating them as missing data and imputing them with the median. 3.Preprocessing: Scales features using StandardScaler to ensure the model treats all variables fairly. 4.Modeling: Trains a Random Forest model with 100 trees and balanced class weights to account for dataset imbalance. 5.Evaluation: Generates a Confusion Matrix, ROC-AUC curve, and Feature Importance plot. 6.Inference: Includes a utility function to predict the status of a single patient based on custom input.

Requirements : To run this script, you will need Python 3.x and the following libraries: pandas, numpy, matplotlib, seaborn, scikit-learn. You can install them via pip command.

Key Features & Logic : Handling Missing Data : A unique aspect of this dataset is that missing values are often encoded as 0 (e.g., a Blood Pressure of 0 is medically impossible). Action: The script replaces 0 with NaN for specific columns and uses Median Imputation to fill those gaps.

Model Evaluation :The script produces three critical visualizations: (i) Confusion Matrix: Shows True Positives vs. False Positives. (ii) ROC Curve: Displays the trade-off between sensitivity and specificity. (iii) Feature Importance: Ranks which health factors (like Glucose or BMI) most influence the prediction.

Usage : Simply run the script to train the model and see the evaluation metrics.

Predicting for a New Patient : You can use the built-in function to test specific cases: new_patient = { "Pregnancies": 2, "Glucose": 148, "BloodPressure": 72, "SkinThickness": 35, "Insulin": 0, "BMI": 33.6, "DiabetesPedigreeFunction": 0.627, "Age": 50 } predict_patient(new_patient)

Results: The output includes a saved image diabetes_results.png which summarizes the model's performance. The use of class_weight="balanced" ensures that the model remains sensitive to detecting diabetic cases even if they are the minority class in the data.
