# Real-Time ML Inference REST API & Capstone

## Project Overview
This project provides a real-time Machine Learning inference service using FastAPI and a trained Random Forest model.

## Features
- FastAPI REST API
- JSON input and output
- ML prediction with probabilities
- Docker support
- Unit testing
- GitHub documentation

## API Endpoint

### POST /predict

Example request:

{
  "sepal_length": 5.1,
  "sepal_width": 3.5,
  "petal_length": 1.4,
  "petal_width": 0.2
}

The API returns the predicted class and prediction probabilities.

## System Flow

User
→ JSON Request
→ FastAPI
→ Input Validation
→ ML Model
→ Prediction
→ JSON Response

## Technologies
- Python
- FastAPI
- Scikit-learn
- Docker
- Pytest

## Project Files
- main.py - FastAPI server
- model.joblib - trained ML model
- train_model.py - model training
- test_api.py - unit tests
- requirements.txt - dependencies
- Dockerfile - container configuration
- README.md - project documentation

## How to Run

Install dependencies:

pip install -r requirements.txt

Run the API:

uvicorn main:app --reload

Open:

http://127.0.0.1:8000/docs

## Docker

Build:

docker build -t ml-inference-api .

Run:

docker run -p 8000:8000 ml-inference-api
