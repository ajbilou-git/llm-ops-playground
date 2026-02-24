# Lab 07 — ML Prediction Pipeline

## Objective
Build a classical ML pipeline for equipment failure prediction, served via a FastAPI endpoint.

## Concepts Covered
- Feature Engineering: transforming raw data into predictive features
- Model Training: Random Forest, XGBoost
- ML Pipeline: ingestion → preprocessing → training → evaluation
- Model Serving: FastAPI REST API

## Enterprise Scenario
Predict equipment failures before they occur using historical sensor logs (vibration, temperature, pressure, runtime hours).

## Steps
1. Generate synthetic equipment sensor data
2. Feature engineering (rolling averages, anomaly indicators)
3. Train prediction models (Random Forest, XGBoost)
4. Evaluate with classification metrics (precision, recall, F1)
5. Serve the model via FastAPI
6. Build a simple metrics dashboard

## Deliverable
Failure prediction API with performance dashboard.

## Tech Stack
- Scikit-learn, XGBoost
- Pandas, NumPy
- FastAPI
- Streamlit or Gradio (dashboard)
- Python
