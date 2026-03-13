
# Parkinson's Disease Severity Prediction using Acoustic Biomarkers

## Project Overview
This project applies machine learning techniques to predict the severity of Parkinson’s disease using acoustic voice biomarkers derived from speech recordings. The goal is to explore whether non‑invasive voice features can help estimate disease severity and support remote monitoring in healthcare.

The notebook performs the complete machine learning workflow including data loading, preprocessing, exploratory data analysis, model training, evaluation, and model comparison.

## Dataset
Dataset used: Parkinson Telemonitoring Dataset.

The dataset contains demographic variables, clinical severity scores, and multiple acoustic features extracted from speech recordings of patients.

Key variables include:

| Type | Variables |
|-----|-----|
| Demographic | age, sex |
| Recording information | test_time |
| Targets | motor_UPDRS, total_UPDRS |
| Acoustic features | jitter, shimmer, HNR, PPE, DFA, RPDE and others |

Target variable used for modelling:
motor_UPDRS

## Machine Learning Workflow

### 1. Data Loading
The dataset is loaded using pandas and basic dataset inspection is performed including:
- previewing the first rows
- checking column names
- verifying dataset shape
- identifying feature and target variables

### 2. Data Preprocessing
The following preprocessing steps are applied:

- checking for missing values
- removing identifier column (subject#)
- feature scaling using StandardScaler
- train test split with 80 percent training and 20 percent testing data

### 3. Exploratory Data Analysis
Exploratory analysis includes:

- computing correlations between acoustic features and the target variable
- identifying the most relevant acoustic biomarkers
- correlation heatmap visualization
- feature importance exploration

### 4. Models Implemented

Three regression models are implemented and compared.

Random Forest Regressor
XGBoost Regressor
Support Vector Regression

Hyperparameter tuning is performed using GridSearchCV.

### 5. Evaluation Metrics

Models are evaluated using the following regression metrics:

R2 Score  
Root Mean Squared Error (RMSE)  
Mean Absolute Error (MAE)  
Cross Validation R2

### 6. Model Comparison

Performance of the three models is compared to determine the most accurate predictor of Parkinson disease severity.

Random Forest achieved the best predictive performance followed by XGBoost while Support Vector Regression showed lower accuracy.

## Libraries Used

from sklearn.ensemble import RandomForestRegressor
from sklearn.inspection import permutation_importance
from sklearn.metrics import mean_squared_error, mean_absolute_error, r2_score
from sklearn.model_selection import train_test_split
from sklearn.model_selection import train_test_split, cross_val_score
from sklearn.preprocessing import StandardScaler
from sklearn.svm import SVR
from xgboost import XGBRegressor
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import seaborn as sns

## Results Summary

| Model | R2 | RMSE | MAE |
|-----|-----|-----|-----|
| Random Forest | 0.9731 | 1.3094 | 0.6152 |
| XGBoost | 0.9557 | 1.6822 | 1.1464 |
| SVR | 0.5274 | 5.4923 | 4.1525 |

Random Forest demonstrated the best overall performance for predicting Parkinson disease severity using acoustic biomarkers.

## Project Structure

| File | Description |
|-----|-----|
| main.ipynb | Jupyter notebook containing full analysis and model training |
| parkinsons_updrs.csv | Dataset used for training and evaluation |
| README.md | Project documentation |

## Conclusion
The results demonstrate that machine learning models can effectively predict Parkinson disease severity using acoustic voice biomarkers. Ensemble models such as Random Forest and XGBoost perform particularly well due to their ability to capture nonlinear relationships between features.

Voice based biomarkers combined with machine learning offer a promising approach for remote monitoring and early detection of Parkinson disease.
