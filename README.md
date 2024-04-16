# ML Regression Models for Aircraft Noise Prediction

<p align="center">
  <img src="https://images.unsplash.com/photo-1520437358207-323b43b50729?q=80&w=800&auto=format&fit=max&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Aircraft Noise">
</p>

## Overview
This project aims to predict aircraft noise levels using machine learning regression models. Aircraft noise is a significant concern for communities near airports, and accurate prediction models can aid in noise mitigation efforts. In this project, we explore various regression techniques to predict noise levels based on different parameters.

## Dataset
The dataset used in this project is sourced from the Aircraft Noise and Performance (ANP) Data of the EASA. The 'aircraft_noise.csv' file is a cleaned dataset with the necessary parameters needed for the models. It contains information on various parameters related to aircraft noise, including sound metrics, operational characteristics, and aircraft sound levels at 10,000 ft altitude.

## Technologies Used
- Python
- Libraries: NumPy, pandas, Matplotlib, seaborn, scikit-learn, XGBoost, CatBoost

## Model Building Process
1. **Data Preprocessing**: 
    - Imported necessary libraries and loaded the dataset.
    - Encoded categorical data using label encoding and one-hot encoding.
    - Visualized the correlation matrix of independent variables and eliminated high correlations in variables.

2. **Model Training and Evaluation**:
    - **Multiple Linear Regression**: Trained a linear regression model and evaluated its performance.
    - **Polynomial Regression**: Applied polynomial features and trained a regression model.
    - **Support Vector Regression (SVR)**: Utilized SVR with feature scaling for prediction.
    - **Decision Tree Regression**: Employed decision tree regression for noise prediction.
    - **Random Forest Regression**: Trained a random forest ensemble model for noise prediction.
    - **XGBoost Model**: Built a gradient boosting model using XGBoost.
    - **CatBoost Model**: Implemented a boosting model using CatBoost.

3. **Fine Tuning and Validation**:
    - Fine-tuned the XGBoost model using grid search and cross-validation.
    - Validated the final model's performance using accuracy metrics.

## Results
- Multiple Linear Regression:
    - MAPE: 8.36%
    - R-squared (r2): 0.6604
    - Adjusted R-squared (adj_r2): 0.6517

- Polynomial Regression:
    - MAPE: 6.87%
    - R-squared (r2): 0.7628
    - Adjusted R-squared (adj_r2): 0.7566

- SVR:
    - MAPE: 20.14%
    - R-squared (r2): 0.7966
    - Adjusted R-squared (adj_r2): 0.7914

- Decision Tree Regression:
    - MAPE: 3.90%
    - R-squared (r2): 0.8991
    - Adjusted R-squared (adj_r2): 0.8965

- Random Forest Regression:
    - R-squared (r2): 0.9279
    - Adjusted R-squared (adj_r2): 0.9261

- XGBoost Model:
    - R-squared (r2): 0.9742
    - Adjusted R-squared (adj_r2): 0.9735

- CatBoost Model:
    - R-squared (r2): 0.9722
    - Adjusted R-squared (adj_r2): 0.9715

## Fine-Tuning Results
- Best Hyperparameters for XGBoost Model:
    - Learning Rate: 0.205
    - Max Depth: 4
    - Subsample: 0.8
    - Number of Estimators: 558
- Cross-validated Accuracy: 97.42%
- Standard Deviation: 0.66%

## Conclusion
The XGBoost model outperformed other regression models with the highest R-squared value and demonstrated excellent accuracy after fine-tuning. This project showcases the effectiveness of machine learning techniques in predicting aircraft noise levels, which can aid in urban planning and noise mitigation strategies around airports.
