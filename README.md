# HOSPITAL READMISSION PREDICTION

## Introduction

This repository hosts the code and analysis pipeline for predicting patient readmission rates using clinical data. By integrating SHAP (SHapley Additive exPlanations) with a robust Random Forest-based model, the project leverages advanced machine learning techniques to classify patient readmission risks with high predictive performance (Weighted F1-score: 0.73). Beyond classification, the system provides interpretable local and global explanations to enhance transparency and trust, ultimately aiming to improve healthcare resource allocation, clinical decision-making, and patient outcomes

## Authors

Pauline Lorteau

Ivan Barona

## Phase 1: Data Processing & Advanced Modeling
This phase addresses the challenge of cleaning complex medical datasets and building a robust classification model.

Our goal is to accurately predict the binary target readmitted. The dataset involves various patient attributes including age, weight, and medication history.

To achieve high performance, we implemented Advanced Feature Engineering, specifically focusing on ICD-9 Diagnosis Grouping. Raw diagnosis codes were mapped into meaningful clinical categories (e.g., Circulatory, Respiratory, Diabetes) to reduce dimensionality and improve model interpretability.

Models & Techniques
Random Forest Classifier: A robust ensemble method chosen for its ability to handle non-linear relationships.

GridSearchCV: Employed for hyperparameter tuning (optimizing n_estimators and max_depth) to maximize the F1-weighted score.

Stratified Train-Test Split: Ensures the model is evaluated on a representative sample of the data.

## Phase 2: Explainability with SHAP
The second phase addresses the "Black Box" problem in machine learning. We utilize SHAP (SHapley Additive exPlanations) to provide transparent reasoning behind every prediction.

This is critical in healthcare, where understanding why a model predicts a readmission is just as important as the prediction itself.

### Explainability Pipeline
Force Plots: To visualize the push and pull of features for individual patients.

Waterfall Plots: To break down the decision path for specific predictions.

Beeswarm & Summary Plots: To visualize global feature importance and impact direction.

## Dependencies
To run this code, you will need the following libraries:

pandas

numpy

sklearn

shap

matplotlib

