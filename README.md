# Flu Vaccine Prediction (DataHack)

Hackathon entry that predicts, for each survey respondent, the probability of receiving two vaccines: the xyz vaccine and the seasonal flu vaccine (`xyz_vaccine` and `seasonal_vaccine` are the target columns in the competition data).

## Approach

- Features: the survey answers. Numeric columns are median-imputed and standardised; categorical columns are imputed with the most frequent value and one-hot encoded, all inside a scikit-learn `ColumnTransformer`.
- Model: an RBF-kernel `SVC` with probability outputs, wrapped in `MultiOutputClassifier` to predict both targets.

## Files

- `submission.ipynb`: the full pipeline
- `submission_csv.csv`: predicted probabilities for the test set

The competition data files are not included.
