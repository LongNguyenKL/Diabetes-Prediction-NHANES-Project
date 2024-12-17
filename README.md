
# Financial Well-being Evaluation Based on Self-Reported Financial Metrics 

## Introduction
Due to limited healthcare resources and specialist access, early detection and intervention of diabetes remains a challenge. Machine learning (ML) models offer a promosing potential, enabling early detection by analyzing patient data to support traditional medical diagnosis methods.

This project aims to develop a diabetes prediction model using ML techniques and available data to identify individuals at risk, allowing timely support and data-driven healthcare decisions.

![alt text](https://github.com/LongNguyenKL/Diabetes-Prediction-NHANES-Project/blob/main/assets/chartscreenshots.png?raw=true)


## Documentation

- **NHANES_age_prediction.csv**: data from the [National Health and Nutrition Health Survey 2013-2014 (NHANES) Age Prediction Subset](https://archive.ics.uci.edu/dataset/887/national+health+and+nutrition+health+survey+2013-2014+(nhanes)+age+prediction+subset). The data was created by the Centers for Disease Control and Prevention (CDC) through interviews, physical examinations, and lab tests. *The sample used for this project is only a subset of the original dataset*.
- HealthPredictionProject.ipynb: Python notebook including the full model building process.
- ProjectPresentation.pptx: a summarized project report.

## Features

Project includes:
- Uploading and cleaning data
- Model selection and normalization
- ML models:
  - K-nearest neighbor (KNN) Classifier
  - Random Forest Classifier
  - XGBoost classifier
  - Logistic Regression: OneVsRest Classifier
  - Support Vector Machine
  - Naive Bayes
- Hyperparameter tuning using K-fold cross validation.

![alt text](https://github.com/LongNguyenKL/Diabetes-Prediction-NHANES-Project/blob/main/assets/metrics.png?raw=true)

## Lessons Learned

The major concern with the dataset is the class imbalance as only **0.9%** of the respondents in the subset are diabetic. This raises the question about how biased it was when the subset was selected. 

To address the class imbalance, we specified **"class_weight = 'balanced'"** and **"average = 'macro'"** during the model bulding process. However, resampling or increasing sample size would be needed to improve the model performance.

However, for the reason above, we did not expect outstanding performance from our models. The best performing one was Logistic Regression using multiclass method, resulting in **0.33 F1-score, 0.52 recall, and 0.66 ROC AUC**. Notably, the models would perform significantly better if we used average = 'micro' or 'weighted'. However, it is important for our project to emphasize on the minority class (diabetic = YES).  

## Authors

Thank you to those who have contributed and supported this project:

- [Long Nguyen](https://www.linkedin.com/in/long-nguyen-4583791a2/)
- [Tasnim Shairy](https://www.linkedin.com/in/tasnimshairy901/)
- [Brian Kimotho](https://www.linkedin.com/in/briankimotho/)
- [Prof. Abdallah Musmar](https://www.linkedin.com/in/abdallahmusmar/)

