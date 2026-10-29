# Airbnb Price Prediction

**Exploratory Data Analysis and Machine Learning with Python**

## Overview

This project aims to predict the logarithm of Airbnb listing prices from property characteristics, location, room type, amenities, and other listing attributes.

Developed as part of an academic Data Analysis course at ESILV, the project combines exploratory data analysis, feature engineering, regression modelling, and prediction export.

## Objectives

- Understand the dataset through statistical analysis and visualisation.
- Identify features that may influence listing prices.
- Prepare numerical and categorical data for machine learning.
- Compare regression models using a validation set.
- Generate a CSV file containing predictions for unseen listings.

## Methodology

### 1. Exploratory Data Analysis

The notebook investigates the distribution of `log_price` and explores relationships between listing prices and selected features.

Visualisations include:
- Target variable distribution.
- Correlation heatmap for numerical variables.
- Price comparisons across room types and cities.
- Relationship between accommodation capacity and price.
- Geographic distribution of listings and prices.

### 2. Data Preprocessing and Feature Engineering

The preprocessing pipeline includes:
- Median imputation for selected numerical features.
- Conversion of Boolean features into numerical values.
- Feature engineering based on the number of amenities.
- Encoding of categorical variables using one-hot encoding.
- Selection and alignment of features between training and test data.

### 3. Model Comparison

Two regression models are evaluated using an 80/20 train-validation split:

| Model | Validation RMSE |
|---|---:|
| Linear Regression (baseline) | 0.4737 |
| Random Forest Regressor | 0.4193 |

The Random Forest achieves a lower validation RMSE than the linear regression baseline, making it the selected model for the final prediction step.

### 4. Final Predictions

The selected model is retrained on the full training dataset and used to predict `log_price` for the test dataset.

The generated file, `prediction_finale_airbnb_Jeanne_Faizan.csv`, contains **51,877 predictions** with the expected `id` and `log_price` columns.

## Technologies

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- Jupyter Notebook

## Repository Structure

- `Projet_Airbnb.ipynb` — Exploratory analysis, preprocessing, model comparison, and final prediction workflow.
- `prediction_finale_airbnb_Jeanne_Faizan.csv` — Final prediction output.
- `images/` — Selected visualisations from the notebook.
- `requirements.txt` — Python dependencies.

## Getting Started

Install the dependencies:

```bash
pip install -r requirements.txt
```

Open `Projet_Airbnb.ipynb` in Jupyter Notebook or Google Colab.

The original training and test CSV files are not included in this repository. Obtain the datasets from the original course materials and update the notebook's file paths before running the workflow.

## Project Context

Academic group project completed by Faizan Norat and Jeanne Nicolas as part of the Data Analysis course at ESILV.
