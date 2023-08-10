# ModelAndOptimization

## Overview
This class is designed to simplify the process of finding the optimal machine learning model and hyperparameters by utilizing both grid search and Bayesian optimization techniques.

## Workflow
The key steps of this class are as follows:

### 1. Model Selection and Fitting
The class accepts a list of models and their respective hyperparameter grids. It then performs a standard fitting process for each model using the provided dataset. The primary evaluation metric (scoring) can be specified by the developer (e.g., accuracy, ROC AUC, precision, mean absolute error).

### 2. Top Model Selection
Following the model fitting stage, the class ranks the models based on their scores and selects the top N models, where N is determined by the developer. This ensures that the subsequent hyperparameter tuning is focused on the most promising models.

### 3. Hyperparameter Optimization
For the selected top models, the class applies grid search to explore various hyperparameter combinations. The best hyperparameters are chosen for each model, and the corresponding scores are recorded. You may select grid, random or bayesian as search methods

### 4. Results and Rankings
The class provides insights into the model rankings based on their scores post hyperparameter optimization. This ranking assists developers in identifying the most suitable models for their specific problem.

## Limitations and Considerations
- **Computational Cost:** Grid search is applied exclusively to the top N models to manage computational resources efficiently.
- **Developer Input:** Developers must supply the models list, hyperparameter grids, and desired evaluation metric. The class does not perform automated feature selection or data preprocessing.
- **Model Dependencies:** Ensure that the necessary dependencies for the selected models are installed. This class assumes access to models and their associated methods for fitting and prediction. 
