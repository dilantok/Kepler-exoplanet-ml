# Kepler Exoplanet ML

A guided learning project exploring Kepler stellar light curves
and binary classification with scikit-learn.

## Sources

The exploratory analysis is adapted from
[Priyanshu Jain's Kaggle notebook](https://www.kaggle.com/code/priyanshujain070/exoplanet-hunting-habitability-detection).

Data:
[Exoplanet Hunting in Deep Space](https://www.kaggle.com/datasets/keplersmachines/kepler-labelled-time-series-data).

## Added experiment

I extended the notebook with:
- A stratified 80/20 training and test split.
- A pipeline combining StandardScaler and logistic regression.
- Balanced class weights.
- Evaluation using precision, recall and a confusion matrix.

## Results

The test set contains 1,018 examples, including 7 positive examples.

| Metric | Result |
|---|---:|
| True positives | 1 |
| False negatives | 6 |
| False positives | 49 |
| True negatives | 962 |
| Positive-class precision | 2% |
| Positive-class recall | 14.3% |
| Accuracy | 94.6% |

The model performs poorly at identifying positive examples.
Accuracy alone is misleading because the dataset is highly imbalanced.
Only 7 positive test examples also limits confidence in the results.

This is an introductory classification experiment.
It does not assess planetary habitability.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn and KaggleHub.
