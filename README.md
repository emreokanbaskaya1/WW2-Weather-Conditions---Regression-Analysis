# WW2 Weather Conditions - Regression Analysis

This project predicts daily mean temperature using maximum and minimum temperatures from a World War II weather dataset. The goal is to compare several linear regression models and evaluate their performance with common regression metrics.

## Overview
- Task: supervised regression
- Target: mean temperature
- Features: max temperature, min temperature
- Models: Linear Regression, Lasso, Ridge, ElasticNet, ElasticNetCV
- Metrics: MAE, MSE, R2

## Dataset
The dataset contains daily weather observations from World War II. It includes temperature readings and additional meteorological fields. Only the columns required for this experiment are used.

## Workflow
1. Load data and inspect basic structure.
2. Remove columns that are fully missing.
3. Drop columns with more than 70% missing values.
4. Remove remaining columns containing any missing values.
5. Parse date column and clean precipitation values.
6. Explore correlations and visualize heatmap.
7. Select features and target.
8. Split into train/test sets.
9. Apply standard scaling to numeric features.
10. Train multiple linear models and compare results.

## Feature Selection
- Input features: MaxTemp, MinTemp
- Target: MeanTemp

## Train/Test Split
- Train size: 20%
- Random state: 15

## Models
- Linear Regression
- Lasso Regression
- Ridge Regression
- ElasticNet
- ElasticNetCV (5-fold cross-validation)

## Evaluation Metrics
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- R2 Score

## Results
Below is a template table for your final numbers. Replace the placeholders with the values shown in the notebook output.

| Model           | MAE    | MSE    | R2     |
|----------------|--------|--------|--------|
| Linear         | 0.1708 | 0.2661 | 0.9961 |
| Lasso          | 0.7451 | 1.3046 | 0.9810 |
| Ridge          | 0.1707 | 0.2661 | 0.9961 |
| ElasticNet     | 1.5194 | 4.8404 | 0.9294 |
| ElasticNetCV   | 0.1709 | 0.2676 | 0.9961 |

## Example Prediction
A simple example uses max temp = 30 and min temp = 20 to predict mean temperature after scaling.

## Visuals
- Correlation heatmap
- Boxplots before and after scaling
- Scatter plots of predicted vs. actual values for each model

## How To Run
1. Put the dataset CSV in the working directory.
2. Run the notebook from top to bottom.
3. Review printed metrics and plots.

## Notes
- StandardScaler is applied only to features.
- Regularized models are tested to evaluate stability and generalization.

## License
Choose a license if you plan to share the project publicly (MIT is common).

## Acknowledgments
Dataset provided by Kaggle.
