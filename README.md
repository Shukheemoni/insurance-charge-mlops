# insurance-charge-mlops

## Overview

This project is an end-to-end MLOps pipeline for predicting insurance charges using a Random Forest Regression model.

The project demonstrates the complete machine learning lifecycle, including:

- Data cleaning
- Feature engineering
- Model training
- Hyperparameter tuning using GridSearchCV
- Model evaluation
- Streamlit web application
- Docker containerization

---

## Project Structure

```
Insurance_MLOps/

├── app/
│   └── app.py

├── src/
│   ├── data.py
│   ├── features.py
│   ├── train.py
│   └── evaluate.py

├── models/
│   ├── model.joblib
│   └── metrics.json

├── data/

├── requirements.txt

├── Dockerfile

└── README.md
```

---

## Dataset

Medical Cost Personal Dataset

Target Variable:

- charges

Features:

- age
- sex
- bmi
- children
- smoker
- region

---

## Machine Learning Model

Algorithm:

- Random Forest Regressor

Hyperparameter Tuning:

- GridSearchCV

Evaluation Metrics:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

---

## Model Performance

R² Score

0.8672

MAE

2529.91

RMSE

4540.28

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Streamlit
- Joblib
- Docker

---

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

## Run the Streamlit App

```bash
streamlit run app/app.py
```

---

## Docker

### Build Docker Image

```bash
docker build -t insurance-mlops .
```

### Run Docker Container

```bash
docker run -p 8501:8501 insurance-mlops
```

The application will be available at:

```
http://localhost:8501
```

---

## MLOps Pipeline

1. Load raw insurance dataset
2. Clean and preprocess the data
3. Perform feature engineering
4. Split features and target
5. Train Random Forest model
6. Tune hyperparameters using GridSearchCV
7. Evaluate model performance
8. Save trained model using Joblib
9. Deploy using Streamlit
10. Containerize using Docker

---

## Future Improvements

- Deploy to Streamlit Cloud
- CI/CD using GitHub Actions
- Model versioning with DVC
- Cloud deployment using Azure or AWS
