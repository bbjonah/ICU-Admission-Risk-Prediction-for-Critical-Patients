# ICU Admission Risk Prediction for Critical Patients

## Overview

Early identification of critically ill patients is essential for improving clinical outcomes and optimizing hospital resource allocation. Delayed admission to the Intensive Care Unit (ICU) can significantly increase patient morbidity, mortality, and healthcare costs.

This project develops a machine learning-based predictive system capable of estimating a patient's likelihood of requiring ICU admission using demographic information, vital signs, laboratory measurements, comorbidities, and clinical assessment scores. The model is designed to support healthcare professionals by providing data-driven risk assessments that facilitate timely intervention and critical care planning.

---

## Problem Statement

Hospitals frequently face challenges related to limited ICU capacity and increasing patient volumes. Accurately identifying high-risk patients before clinical deterioration occurs can help clinicians:

* Improve patient outcomes
* Reduce mortality rates
* Optimize ICU bed utilization
* Enhance emergency department workflows
* Support evidence-based clinical decision-making

The objective of this project is to build a predictive model that classifies whether a hospitalized patient is likely to require ICU admission.

---

## Project Objectives

* Develop a robust ICU admission prediction model.
* Analyze patient demographics, vital signs, and laboratory findings.
* Identify key clinical factors associated with critical illness.
* Evaluate model performance using healthcare-focused metrics.
* Generate actionable insights for healthcare decision support.

---

## Dataset

This project uses a realistic synthetic healthcare dataset containing patient-level information commonly collected during hospital admission and clinical assessment.

### Dataset Features

#### Demographic Information

* Patient_ID
* Age
* Gender
* BMI

#### Vital Signs

* Heart Rate
* Respiratory Rate
* Oxygen Saturation (SpO₂)
* Systolic Blood Pressure
* Diastolic Blood Pressure
* Body Temperature

#### Laboratory Results

* White Blood Cell Count
* Hemoglobin
* Platelet Count
* Blood Glucose
* Creatinine
* Lactate
* C-Reactive Protein (CRP)

#### Comorbidities

* Diabetes
* Hypertension
* Chronic Kidney Disease
* Heart Disease
* COPD
* Cancer

#### Clinical Indicators

* Glasgow Coma Scale (GCS)
* Early Warning Score (EWS)
* Sepsis Indicator

#### Hospital Information

* Admission Type

#### Target Variable

* ICU_Admission

  * 1 = ICU Admission Required
  * 0 = No ICU Admission Required

---

## Machine Learning Workflow

### 1. Data Preprocessing

* Missing value handling
* Data validation
* Feature scaling
* Categorical encoding

### 2. Feature Engineering

Additional clinical risk indicators are created, including:

* Shock Index
* Comorbidity Count
* High Lactate Flag

### 3. Model Development

The project utilizes:

* Random Forest Classifier

Additional models that can be evaluated:

* Logistic Regression
* XGBoost
* LightGBM
* CatBoost
* Gradient Boosting

### 4. Model Evaluation

Performance is assessed using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC Score
* Confusion Matrix

---

## Project Structure

```text
ICU-Admission-Risk-Prediction/
│
├── data/
│   └── icu_admission_risk_prediction_dataset.csv
│
├── notebooks/
│   └── analysis.ipynb
│
├── models/
│   └── icu_admission_prediction_model.pkl
│
├── images/
│   ├── roc_curve.png
│   ├── confusion_matrix.png
│   └── feature_importance.png
│
├── src/
│   └── icu_prediction.py
│
├── requirements.txt
│
├── README.md
│
└── LICENSE
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/yourusername/ICU-Admission-Risk-Prediction.git

cd ICU-Admission-Risk-Prediction
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux/Mac

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Required Libraries

```text
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

Install manually:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

---

## Running the Project

```bash
python icu_prediction.py
```

The script will:

* Load and preprocess data
* Train the machine learning model
* Evaluate predictive performance
* Generate visualizations
* Save the trained model

---

## Sample Results

Typical model performance on the synthetic dataset:

| Metric    | Score  |
| --------- | ------ |
| Accuracy  | 85–92% |
| Precision | High   |
| Recall    | High   |
| ROC-AUC   | 0.90+  |

Actual performance may vary depending on random sampling and model tuning.

---

## Feature Importance Analysis

Key predictors commonly associated with ICU admission include:

* Lactate
* Oxygen Saturation (SpO₂)
* Glasgow Coma Scale
* Shock Index
* Early Warning Score
* Sepsis Indicator
* Creatinine
* Age
* Blood Pressure

These variables align with established clinical indicators of patient deterioration and critical illness.

---

## Visualizations

The project generates several healthcare analytics visualizations:

### Clinical Analytics

* ICU Admission Distribution
* Age Group Risk Analysis
* Comorbidity Impact Assessment

### Machine Learning Evaluation

* Confusion Matrix
* ROC Curve
* Feature Importance Ranking

### Explainability

* SHAP Analysis (Optional Extension)
* Clinical Risk Interpretation

---

## Potential Applications

* Hospital Decision Support Systems
* Emergency Department Triage
* Critical Care Resource Planning
* Clinical Risk Stratification
* Healthcare Operations Analytics
* Predictive Patient Monitoring

---

## Future Improvements

* Incorporate temporal patient monitoring data
* Deploy as a web application using Streamlit
* Integrate explainable AI techniques (SHAP/LIME)
* Compare multiple machine learning models
* Develop real-time ICU risk scoring dashboards
* Implement deep learning approaches

---

## Ethical Considerations

This project uses synthetic data for educational and research purposes.

The model is not intended for direct clinical use without:

* Clinical validation
* Regulatory approval
* External performance assessment
* Healthcare professional oversight

Predictions should be used only as decision-support recommendations rather than definitive medical judgments.

---

## Author

**Jonah Buka**

**Data Science & Machine Learning Portfolio Project**

Focused on applying predictive analytics and machine learning techniques to healthcare risk assessment and clinical decision support systems.

---

## License

This project is licensed under the MIT License.

Feel free to use, modify, and distribute this project for educational and research purposes.
