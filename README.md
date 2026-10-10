# Crop Yield Prediction Using a Heterogeneous Stacking Ensemble

This repository provides the experimental source code for the study entitled **“Multi-Model Fusion with Grid Search-Based Hyperparameter Tuning for Robust Crop Yield Prediction.”**

The proposed framework integrates Random Forest (RF), XGBoost, and a Neural Network (NN) through a Ridge regression meta-learner.

## Requirements

Install the required Python libraries using:

```bash
pip install -r requirements.txt
```

## Dataset

Download the publicly available crop yield prediction dataset from:

https://www.kaggle.com/datasets/patelris/crop-yield-prediction-dataset

The implementation uses the dataset file `yield_df.csv`.

## Running the Experiments

1. Download the dataset.
2. Open the experimental source code provided in this repository.
3. Configure the dataset path in the source code to point to `yield_df.csv`.
4. Run the complete code in a Python environment with the required libraries installed.

The implementation performs data preprocessing, hyperparameter optimization, model training, five-fold out-of-fold stacking, and model evaluation.

## Expected Main Results

The principal held-out evaluation reported in the manuscript is:

| Model | MAE (hg/ha) | RMSE (hg/ha) | R² |
|---|---:|---:|---:|
| Random Forest | 4,320.98 | 9,744.83 | 0.98658 |
| XGBoost | 9,187.40 | 14,625.03 | 0.96978 |
| Neural Network | 6,871.10 | 11,355.04 | 0.98178 |
| Stacking Ensemble | 4,192.67 | 9,033.90 | 0.98847 |

A fixed random seed of 42 is used to improve reproducibility. Results may exhibit minor differences across hardware and software environments.

## Additional Analyses

The source code also supports feature importance, bootstrap confidence intervals, ablation studies, chronological validation, and computational-efficiency evaluation.
