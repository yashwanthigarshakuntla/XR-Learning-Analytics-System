# XR Learning Analytics

## Overview
This project develops a machine learning system to predict learner quiz performance and identify whether additional support is required in an XR learning environment.

## Problem Statement
In immersive learning environments, educators need early signals to identify struggling learners and intervene before performance drops further. This project uses learner session data to support that decision-making.

## Objectives
- Predict next quiz score using regression
- Predict support requirement using classification
- Compare multiple models using a shared preprocessing pipeline
- Apply threshold-based decision logic for intervention recommendations

## Dataset
The dataset contains learner session-level behavioural and performance features such as session duration, help requests, attention ratio, pause count, modality usage, previous quiz history, and mastery indicators.

## Methodology
- Cleaned and prepared tabular data
- Used a preprocessing pipeline with imputation, scaling, and one-hot encoding
- Trained regression and classification models
- Evaluated model performance using suitable metrics
- Applied cost-sensitive threshold logic for support decisions

## Tech Stack
Python, pandas, NumPy, scikit-learn, matplotlib, Jupyter Notebook

## Results
Summarise your best regression and classification results here.
Example:
- Best regression model: Random Forest Regressor
- Best classification model: Logistic Regression / Random Forest
- Evaluation metrics: MAE, MSE, R², precision, recall, F1-score

## Repository Structure
- notebooks/xr_learning_analytics_pipeline.ipynb
- images/
- outputs/
- requirements.txt

## How to Run
1. Clone the repository
2. Install dependencies using `pip install -r requirements.txt`
3. Open the notebook
4. Run cells in sequence

## Key Learnings
This project showed the importance of consistent preprocessing, fair model comparison, and decision threshold tuning when building learning analytics systems.

## Future Improvements
- Add model explainability using SHAP
- Deploy as a simple dashboard
- Validate on larger real-world XR datasets
