# Diabetes Classification - Kaggle Competition

## Competition Results
**Overall Rank:** 2442 out of 4208 participants

## Approach

### 1. Data Processing
- **Categorical Encoding**: Applied one-hot encoding to 6 categorical features (ethnicity, gender, education level, income level, smoking status, employment status)
- **Data Preparation**: Split training data into 80/20 train-test sets with stratified splitting to maintain class distribution

### 2. Feature Engineering
- **Feature Interactions**: Created interaction features including:
  - `bmi_age`: Product of BMI and age to capture combined effect
  - `family_history_squared`: Squared family history to capture non-linear relationships
  - `triglycerides_sq`: Squared triglycerides value
- **Correlation Analysis**: Analyzed feature correlations to identify and handle redundant features

### 3. Model Selection & Training
- **Primary Model**: LightGBM Classifier
- **Hyperparameter Tuning**: RandomizedSearchCV with 5-fold stratified cross-validation
- **Evaluation Metric**: ROC-AUC Score for binary classification task

### 4. Hyperparameter Configuration
LightGBM parameters optimized:
- `n_estimators`: 500
- `max_depth`: 5-6
- `learning_rate`: 0.1
- `subsample`: 0.8
- `colsample_bytree`: 0.8

### 5. Models Explored
- **LightGBM** (Primary) - Selected for final submission
- **XGBoost** - Alternative gradient boosting model
- **CatBoost** - Categorical feature handling

### 6. Submission Generation
- Applied same preprocessing pipeline to test data
- Ensured feature alignment between training and test sets
- Generated probability predictions for binary diabetes diagnosis

## Files
- `Main.ipynb` - Complete modeling pipeline with feature engineering, hyperparameter tuning, and predictions
- `train.csv` - Training dataset with features and target variable
- `test.csv` - Test dataset for predictions
- `submission.csv` - Final predictions submitted to Kaggle

## Key Learnings
- Feature engineering with domain-specific interactions improved model performance
- Stratified cross-validation critical for imbalanced classification tasks
- RandomizedSearchCV enabled efficient hyperparameter exploration
- Proper preprocessing pipeline alignment between train and test sets essential for valid predictions
