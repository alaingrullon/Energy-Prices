# Energy-Prices
A time-series prediction of electricity prices in Spain based on forecasted demand and supply features.

# Methodologies
- Imputation strategies: K Nearest Neighbors to fill in missing values based on rows with similar features.
- Feature Engineering: Spanish Holidays, Daylight using Astral (solar and lunar behaviour based on time), peak-hours (both weekend and weekday).
- Cyclical features: Treating datetime cyclical features with sin and cos to better represent hour, month, and day.
- Train/Validation split: 75% to 25%
- Ensembled Regression: Tried most of the regressors in the sklearn library and xgboost (Random Forest, ExtraTrees, AdaBoost, Gradient Boost, Bagging, Stacking, Voting)
- Cross Validation Randomized Search: 5 fold CV, Random Forest performed best hyperparameters Max depth, max features, number of estimators, bootstrap
- Evaluation: r2= .96, mae=1.99, mse=7.79
