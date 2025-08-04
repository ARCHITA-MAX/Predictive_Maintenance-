# Predictive Maintenance - IBM AutoAI Project

## Overview
This project predicts machine failures using IBM AutoAI on IBM Cloud.  
It was built as part of SB4Academia 2025, Problem Statement 39 – Predictive Maintenance of Industrial Machinery.

The solution leverages **IBM AutoAI** to automatically preprocess data, train multiple machine learning models, select the best pipeline, and deploy the model as an online REST API endpoint for real-time predictions.

---

## Problem Statement
Unexpected machine failures in manufacturing industries cause production losses and costly downtime.  
The goal is to **predict potential machine failures** based on sensor data such as:

- Air temperature
- Process temperature
- Rotational speed
- Torque
- Tool wear

**Output:**  
- `0` → No Failure  
- `1` → Machine Failure

---

## Workflow

1. **Data Upload**  
   - Uploaded the Kaggle Predictive Maintenance dataset to IBM Cloud Object Storage

2. **AutoAI Experiment**  
   - Created an AutoAI experiment in Watson Studio  
   - AutoAI automatically performed:
     - Data preprocessing (encoding, scaling, missing value handling)
     - Feature selection
     - Model training using multiple ML algorithms
     - Hyperparameter optimization

3. **Model Deployment**  
   - Selected the **best-performing pipeline** from AutoAI leaderboard  
   - Deployed the model as an **online endpoint** using IBM Watson Machine Learning  
   - Generated a **REST API endpoint** for real-time predictions

---

## Tech Stack

- **IBM Cloud Services**:
  - IBM Watson Studio AutoAI
  - IBM Cloud Object Storage
  - IBM Watson Machine Learning (Deployment Space)

- **Languages & Tools**:
  - Python (for API testing)
  - JSON (for input/output schema)

---

## Project Architecture

```text
Dataset → IBM AutoAI → Model Selection & Training → Watson Machine Learning Deployment → REST API → Prediction
```

---

## Results

- **Model Accuracy:** ~90% (from AutoAI leaderboard)
- **Selected Algorithm:** Random Forest / Gradient Boosting (auto-selected by AutoAI)
- **Deployed Endpoint:** IBM Watson Machine Learning REST API

---

## Author

**Archita Agarwal**  
BTech AI & Data Science, Graphic Era Deemed to be University  
