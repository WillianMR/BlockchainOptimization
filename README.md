# BlockchainOptimization
Repository with files and code used in the production of the article 'Performance Improvement in Blockchain Applications Using Machine Learning Techniques'

## Project Overview
This project aims to evaluate the performance of a blockchain network using various machine learning models. The evaluation involves predicting different blockchain metrics based on simulation data.


## Data Files
The dataset used in this study can be found in the following GitHub repository: [BlockchainPerformanceML](https://github.com/AlbshriAdel/BlockchainPerformanceML/tree/main)

## Scripts
### Train Models
- **Main Functions:**
  - `calculate_metrics(y_true, y_pred)`: Calculates R2 and RMSE metrics.
  - `objective(trial, model, X_train, X_test, y_train, y_test)`: Objective function for Optuna hyperparameter optimization.
  - `make_predictions(model, model_name, results, save_dir, n_repeats=3, search_type=None, param_distributions=None)`: Trains and evaluates models, storing the results.
  - `run_model_predictions(model, model_name, search_type=None, param_distributions=None)`: Runs the model predictions in parallel.

### Evaluate Models
- **Main Functions:**
  - `load_results(results_path, models_dir)`: Loads the results and best models from the saved files.
  - `describe_results(results_df)`: Prints descriptive statistics of the results.
  - `plot_metrics(results_df)`: Plots boxplots of various metrics for comparison.
  - `plot_mean_metrics(results_df)`: Plots mean metrics across different repeats.
  - `remove_outliers(df, metric)`: Removes outliers based on the IQR method.
  - `plot_metrics_filtered(results_df)`: Plots metrics after removing outliers.
  - `plot_mean_metrics_filtered_after(results_df)`: Plots mean metrics after outlier removal.
  - `plot_mean_metrics_filtered_before(results_df)`: Plots mean metrics before outlier removal.


## Dependencies
- Python 3.7+
- pandas
- numpy
- scikit-learn
- optuna
- xgboost
- catboost
- lightgbm
- joblib
- matplotlib
- seaborn

## Contributing
Feel free to open issues or submit pull requests if you have any improvements or suggestions for this project.

## License
This project is licensed under the MIT License.
