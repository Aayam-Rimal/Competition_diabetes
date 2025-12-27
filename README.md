# Diabetes Classification - Kaggle Competition

## Overview
This notebook implements a binary classification model to predict diabetes diagnosis based on patient health and demographic features.

## Approach
- **Data Processing**: One-hot encoding for categorical variables
- **Model**: LightGBM with hyperparameter tuning via RandomizedSearchCV
- **Metric**: ROC-AUC Score
- **Submission**: Probability predictions for test set

## Files
- `Main.ipynb` - Main notebook with full pipeline
- `train.csv` - Training data
- `test.csv` - Test data
- `submission.csv` - Final predictions

## Note
This notebook will be polished further once the competition ends. Future improvements will include enhanced feature engineering, interaction features, and additional model refinements.

## Results
See notebook output for best CV score, test ROC-AUC, and model comparison metrics.
