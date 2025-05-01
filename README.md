# Dynamic Pricing Demand Model & RL Environment

Procedure:

1. Generating synthetic price→demand datasets

2. Training and comparing multiple regressors (Ridge-regularized polynomial, Random Forest, Exponential, Neural Net)

3. Extracting exponential parameters 

4. Evaluating model performance (RMSE, MAE, R²)

5. Deploying a custom Gym environment for dynamic pricing reinforcement learning

# Features

Data Generation: Synthetic demand data based on an exponential decay model with configurable noise.

# Model Suite:

- Ridge-regularized polynomial regression (degree 2)

- Random Forest ensemble

- Curve-fitted exponential regressor

- Keras-based neural network

# Model Selection: 
- Automatic cross-validated grid search and best-model picking by R²

- Parameter Extraction: Estimate  and  from any fitted model via price samples

- Error Metrics: Compute RMSE, MAE, and R² on held-out test set

# RL Environment: PricingEnv Gym environment that:

Accepts price actions in  €/kWh

Samples demand 

Returns revenue as reward

Provides normalized time-step and last-demand as observation
