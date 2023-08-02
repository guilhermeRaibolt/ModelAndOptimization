# ModelAndOptimization
Function that finds the best model and search for the best hyperparameters using grid search and Bayesian optimization

The main idea is to perform a standard fit using the listed models and select the top N scores, where N is determined by the developer.
After that, the code applies a grid search to the top N models and ranks them from best to worst.
The reason I only apply the grid search to a limited number of models is due to the computational cost.



TBD: I plan on learning and applying the Bayesian optimization later
