# MSDS692panicscore

# Panic Attack Severity Prediction

## Project Overview
This project aimed to predict **Panic Score** based on various lifestyle and medical factors such as age, panic attack frequency, duration of panic attacks, caffeine intake, exercise frequency, sleep hours, and alcohol consumption. Several machine learning models were tested, but the best-performing model only achieved **13% accuracy**, which is quite low.

## Dataset Description
The dataset contains **1200 samples** with the following key features:
- **Age**: Age of the individual.
- **Panic_Attack_Frequency**: Number of panic attacks per period.
- **Duration_Minutes**: Length of panic attacks in minutes.
- **Caffeine_Intake**: Number of caffeinated drinks consumed daily.
- **Exercise_Frequency**: Frequency of exercise per week.
- **Sleep_Hours**: Average sleep duration in hours.
- **Alcohol_Consumption**: Frequency of alcohol consumption per week.
- **Panic_Score (Target Variable)**: Severity of panic attacks on a scale of 1 to 10.

## Machine Learning Models Used
We tested multiple models, including:
- **K-Nearest Neighbors (KNN)**
- **Random Forest Regressor**
- **TPOT (AutoML for feature selection and model tuning)**
- **H2O AutoML**

Despite trying various models, the best model achieved only **13% accuracy**, which is significantly low.

## Reasons for Low Accuracy
### 1. **Low Variability in Features**
- Features like **Caffeine Intake, Exercise Frequency, and Sleep Hours** have very little variation, which limits the model’s ability to distinguish between different levels of panic severity.
- The only feature with significant variability is **Duration_Minutes**, but on its own, it is insufficient to make strong predictions.

### 2. **Limited Data Representativeness**
- The dataset might not contain enough distinguishing factors to accurately predict panic attack severity.
- Important psychological or environmental factors (e.g., stress levels, medication adherence, social support) were not included, potentially missing key predictors.

### 3. **Potential Overfitting or Underfitting**
- Some models might have struggled to generalize due to insufficient feature significance.
- AutoML techniques tried multiple configurations but couldn't significantly improve performance, indicating a fundamental limitation in the dataset itself.

## Conclusion
This project highlights the challenges of predicting **Panic Score** based on lifestyle and physiological factors alone. The low accuracy suggests that additional data, better feature engineering, or alternative modeling approaches might be necessary for meaningful predictions.

## Next Steps
- **Data Collection:** Gather more diverse and representative data to improve variability.
- **Modeling Approaches:** Experiment with deep learning models or ensemble techniques to enhance predictive power.

Despite the low accuracy, this project provides valuable insights into the complexity of predicting panic attack severity and the need for richer datasets in mental health analytics.

