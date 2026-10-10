# Spotter AI — Freight Rate Prediction Assessment

**Candidate:** Md Rakibul Islam

## 1. Project Overview

This project develops a machine-learning solution to predict freight rates using shipment, route, equipment, weight, and date-related features.

Several models were evaluated, including CatBoost, XGBoost, Linear Regression, Random Forest, and K-Nearest Neighbors (KNN). CatBoost was selected because it achieved the lowest Mean Absolute Error (MAE) in the recorded temporal validation experiment.

## 2. Repository Contents

- `Freight_rate_ml_assessments_spotter.ipynb` — Model development, feature engineering, evaluation, and prediction notebook.
- `validation_predictions.csv` — Predictions for 12,000 validation records.
- `data/december_chart_inputs.csv` — Daily freight-rate predictions for December 2025.
- `scorer_results/candidate_december.png` — Generated December prediction chart.
- `Spotter_ML_Assessment_Report.docx` — Technical assessment report.
- `score.py` — Assessment scoring and validation script.
- `requirements.txt` — Python dependencies.

## 3. Model and Validation Approach

A temporal validation split was used, with January through September records for training and October records for validation.

The recorded model comparison selected CatBoost, configured with 354 iterations, depth 8, learning rate 0.04, MAE loss, L2 regularization of 5, and random seed 42.

The selected model was fitted on the full labeled training dataset to generate the final predictions.

## 4. Recorded Validation Results

| Model | Validation MAE | Validation RMSE |
|---|---:|---:|
| CatBoost | $108.35 | $645.59 |
| XGBoost | $174.89 | 721.867850	 |
| Linear Regression | $180.54 | 681.418029 |
| Random Forest | $216.49 | 723.550336	 |
| KNN | $273.07 | 713.205182 |

These are the recorded results from the local temporal validation experiment. Spotter calculates the final validation metrics after submission.

## 5. Submission Validation

The provided scorer reported that:
- 12,000 validation predictions passed its structural checks.
- 31 December predictions passed its fixed-input checks.
- The December chart was generated successfully.

These checks confirm the required prediction format and constraints; they do not establish the final hidden evaluation score.

## 6. Dependencies

Install the required Python packages with:

```bash
python -m pip install -r requirements.txt
```

## 7. Reproducibility

The notebook contains the model-development workflow. Running it from beginning to end may require the original assessment datasets and a compatible Python environment.

The prediction files and report are included as assessment deliverables. The scorer can be run using the command specified in the assessment instructions:

```bash
python score.py --predictions validation_predictions.csv --december-predictions data/december_chart_inputs.csv
```

## 8. Limitations

The final hidden validation metrics are not available in this repository. Further analysis of large prediction errors and performance across routes and time periods may help assess model robustness.
