# XR Learning Analytics System

## Overview

This project builds a machine learning–based decision support system to predict learner quiz performance and identify whether additional support is required in an Extended Reality (XR) learning environment. The system combines regression and classification models with threshold-based logic to enable early intervention.

---

## Problem Statement

In immersive XR learning environments, educators often lack real-time visibility into learner engagement and performance. This makes it difficult to identify struggling learners early.

This project addresses that gap by using session-level learner data to provide early signals for intervention, helping reduce the risk of performance decline.

---

## Objectives

* Predict next quiz score using regression
* Identify learners requiring support using classification
* Compare multiple models using a shared preprocessing pipeline
* Apply threshold-based decision logic for intervention recommendations

---

## Dataset

The dataset consists of session-level learner data, including:

* Engagement metrics: attention ratio, active time, pause count
* Behavioural indicators: help requests, hint usage, error count
* Session features: duration, latency, modality usage
* Performance history: previous quiz scores, mastery level
* Temporal features: session timing and frequency

---

## Methodology

### Data Preprocessing

* Missing values handled using imputation
* Numerical features scaled using StandardScaler
* Categorical features encoded using OneHotEncoder
* Pipeline implemented using ColumnTransformer to avoid data leakage

### Models Used

**Regression:**

* Linear Regression
* Random Forest Regressor

**Classification:**

* Logistic Regression
* Random Forest Classifier

### Evaluation Metrics

* Regression: MAE, MSE, R²
* Classification: Precision, Recall, F1-score

### Decision Logic

A threshold-based approach is used to determine whether a learner requires support, based on predicted probabilities and practical intervention considerations.

---

## Results

### Regression Performance

* Best Model: Random Forest Regressor
* MAE: ~3.5
* R² Score: ~0.94

### Classification Performance

* Achieved balanced precision and recall across classes
* Model effectively identifies learners requiring support

The system demonstrates strong predictive performance and practical usefulness for early intervention scenarios.

---

## Repository Structure

```
xr-learning-analytics/
│
├── notebooks/
│   └── xr_learning_analytics_pipeline.ipynb
│
├── images/
│   ├── workflow.png
│   ├── regression_results.png
│   ├── classification_results.png
│
├── outputs/
│
├── requirements.txt
└── README.md
```

---

## How to Run

1. Clone the repository

   ```bash
   git clone https://github.com/yashwanthigarshakuntla/xr-learning-analytics.git
   ```

2. Install dependencies

   ```bash
   pip install -r requirements.txt
   ```

3. Open the notebook

   ```bash
   jupyter notebook
   ```

4. Run all cells to reproduce results

---

## Key Learnings

* Importance of consistent preprocessing for fair model comparison
* Avoiding data leakage using pipelines
* Trade-offs between regression accuracy and classification reliability
* Practical use of thresholds in real-world decision systems

---

## Limitations

* Dataset is synthetic/simulated
* Limited real-world validation
* Model performance depends on feature quality

---

## Future Improvements

* Add model explainability (SHAP/LIME)
* Deploy as an interactive dashboard
* Integrate real-time learner data streams
* Evaluate fairness across different learner groups

---

## Tech Stack

* Python
* pandas, NumPy
* scikit-learn
* matplotlib
* Jupyter Notebook

---

## Author

Yashwanthi Garshakuntla Durgesh
MSc Artificial Intelligence Student
Former Salesforce Developer at Accenture

