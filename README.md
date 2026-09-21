````markdown
# Credit Card Fraud Detection — FraudShield AI

An end-to-end machine learning application for detecting potentially fraudulent credit card transactions using supervised learning, explainable AI, and a real-time web interface.

## Project Overview

Credit card fraud detection is a highly imbalanced classification problem where the goal is to identify fraudulent transactions while minimizing false positives.

This project demonstrates an end-to-end fraud detection workflow using transaction features, machine learning, SHAP explainability, FastAPI, and Streamlit.

## Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- LightGBM
- SHAP
- Matplotlib
- Streamlit
- FastAPI
- Docker

## Machine Learning Workflow

```text
Transaction Data
       ↓
Data Preprocessing
       ↓
Feature Engineering
       ↓
Class Imbalance Handling
       ↓
LightGBM Model
       ↓
Model Evaluation
       ↓
SHAP Explainability
       ↓
Fraud Risk Prediction
       ↓
FastAPI + Streamlit
````

## Model

The project uses **LightGBM** for fraud classification.

Because fraud datasets are highly imbalanced, evaluation focuses on metrics that provide more information than accuracy alone.

Key evaluation metric:

* ROC-AUC

The dashboard displays a model ROC-AUC of approximately **0.9783** for the provided model.

## Explainable AI

SHAP is used to explain individual model predictions and understand which transaction features contribute to the predicted fraud risk.

This provides greater interpretability compared with treating the ML model as a black box.

## Streamlit Dashboard

The interactive dashboard allows users to enter transaction information and receive a fraud-risk prediction.

The interface includes:

* Transaction amount
* Transaction time
* PCA-based transaction features
* Fraud prediction
* Risk information
* Model performance information
* SHAP-based explanations

## FastAPI

A FastAPI backend is included for serving model predictions through an API.

Swagger documentation can be accessed when the API is running:

```text
http://127.0.0.1:8000/docs
```

## Project Structure

```text
credit-card-fraud-detection/
│
├── assets/
├── data/
├── notebooks/
├── src/
│   ├── api/
│   ├── dashboard/
│   └── ...
│
├── .dockerignore
├── .gitignore
├── Dockerfile
├── Procfile
├── requirements.txt
└── README.md
```

## Running Locally

### 1. Clone the repository

```bash
git clone https://github.com/AyushGupta-07/credit-card-fraud-ml.git
cd credit-card-fraud-ml
```

### 2. Create/activate a Python environment

```bash
conda activate mlproject
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Start the Streamlit dashboard

```bash
streamlit run src/dashboard/app.py
```

The application will be available at:

```text
http://localhost:8501
```

### 5. Start the FastAPI backend

```bash
uvicorn src.api.main:app --reload
```

API documentation:

```text
http://127.0.0.1:8000/docs
```

## Docker

The repository also contains Docker configuration for containerized deployment.

```bash
docker build -t credit-card-fraud-ml .
```

## Key Learning Outcomes

This project provided practical experience with:

* Binary classification
* Imbalanced datasets
* Fraud detection
* LightGBM
* Model evaluation
* SHAP explainability
* Feature preprocessing
* REST APIs with FastAPI
* Interactive ML applications with Streamlit
* Docker-based deployment

## Attribution

This project is an adapted learning implementation.


## Author

**Ayush Gupta**

GitHub:
[https://github.com/AyushGupta-07](https://github.com/AyushGupta-07)
