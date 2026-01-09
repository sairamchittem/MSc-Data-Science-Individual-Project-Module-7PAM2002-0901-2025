# MSc-Data-Science-Individual-Project-Module-7PAM2002-0901-2025

## Predicting Parkinson’s Disease Severity Using Machine Learning

This repository contains the exported HTML file of a data science project focused on predicting Parkinson’s disease severity using acoustic voice biomarkers and machine learning regression models.

The analysis is presented as a static HTML document generated from a Jupyter Notebook and is intended for viewing and academic evaluation purposes.

## Project Overview

Parkinson’s disease is a progressive neurological disorder that affects motor control and speech.
This project applies machine learning regression techniques to predict disease severity using non invasive acoustic biomarkers derived from voice recordings.

Two regression models are implemented and compared:

Linear Regression as a baseline model

Decision Tree Regressor to capture nonlinear relationships

Model performance is evaluated using standard regression metrics.

## Dataset

Dataset Name: UCI Parkinson’s Telemonitoring Dataset

Samples: 5,875 voice recordings

Subjects: 42 individuals with Parkinson’s disease

Features: Acoustic biomarkers including jitter, shimmer, DFA, RPDE, HNR

Target Variable: total_UPDRS (overall disease severity score)

The dataset is publicly available, anonymised, and suitable for academic research.

## Methods and Analysis

The following steps were performed in the analysis:

Data loading and inspection

Exploratory Data Analysis (EDA)

Feature scaling using standardisation

Model training using an 80 percent training and 20 percent testing split

Model evaluation using R², RMSE, and MAE

Feature importance analysis for interpretability


## Evaluation Metrics Used

R² Score: Measures variance explained by the model

RMSE: Penalises large prediction errors

MAE: Average absolute prediction error

These metrics were chosen to provide a balanced evaluation of accuracy and error magnitude.

## Results Summary

The Decision Tree Regressor significantly outperformed Linear Regression, achieving higher explanatory power and lower prediction error.
This demonstrates that nonlinear models are more effective for capturing complex relationships between acoustic biomarkers and Parkinson’s disease severity.

## Ethical Considerations

The dataset used is publicly available and fully anonymised.
No personal identifiers are included.
The project complies with ethical data usage and academic research standards.


Module: DIS064

Institution: University of Hertfordshire
