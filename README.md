# Spotter AI — Freight Rate Prediction Assessment

Candidate: Md Rakibul Islam

## Project overview
This project predicts freight rates using shipment, route, equipment,
weight, and date-related features. CatBoost was selected in the recorded
model comparison based on the lowest validation MAE.

## Included deliverables
- `validation_predictions.csv`: validation predictions
- `data/december_chart_inputs.csv`: December daily predictions
- `scorer_results/candidate_december.png`: generated December chart
- `Spotter_ML_Assessment_Report.docx`: technical report
- `score.py`: assessment validation script
- `requirements.txt`: Python dependencies

## Validation
The supplied scorer reported that 12,000 validation predictions and
31 December predictions passed its structural checks. Final validation
metrics are calculated by Spotter after submission.

## Reproducibility
The model-training notebook or source code and complete run instructions
must be added before this repository is considered complete.
