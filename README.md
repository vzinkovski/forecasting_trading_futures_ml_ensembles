**Forecasting and Trading CME Soybean Futures with ML Ensembles**

In this project we build an ensemble of supervised learning machine models to forecast price returns of CME soybean futures. In contrast to absolute price levels, returns are stationary and therefore lend themselves well to modeling. Our model aims to forecast whether the closing price tomorrow will be higher than today. Naturally, we could extend this methodology and build another model to forecast whether tomorrow's price will be lower than today. However, for brevity, this project will focus on the former. The code, however, is easily extendable to the latter scenario.

First, we build four individual models from different families of machine learning algorithms, perform time series cross validation to tune their hyperparameters using the training set, then ensemble these into a final model via a soft voting approach. Second, we adjust the classification threshold of the ensemble model using the validation set to find the optimum balance between precision and recall. Third, we develop a simple long-only trading strategy where if we predict tomorrow's price to close higher, we enter a long position for a holding period of just one day. Finally, using the holdout test set, we evaluate the performance of this strategy versus an outright buy-and-hold strategy.

Note that the code and model building process can equally be used to forecast returns for other commodities and asset classes. Please feel free to copy the code and repurpose as per your needs.

**Key themes covered:**
- Absolute prices vs. returns
- Binary classification
- Class imbalance
- Feature engineering: return features, rolling features, lagged features, custom features
- Scikit-learn pipelines
- Hyperparameter tuning via time series cross validation
- Ensembling models via soft voting
- Precision-recall curve
- Adjusting the classification threshold
- Dummy classifier as a benchmark
- Confusion matrix
- Equity curves for long-only trading strategy vs. buy-and-hold strategy
