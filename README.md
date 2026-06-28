# Stellar Object Classification — Kaggle Playground S6E6

Multiclass classification of astronomical objects into **GALAXY**, **QSO** (quasar), and **STAR** from photometric and spectroscopic measurements. 

**Result:** 0.9499 balanced accuracy (held-out test), LightGBM.

---

## Approach

- **LightGBM** classifier, selected over logistic regression. Cross-validated balanced accuracy.
- **Metric:** balanced accuracy
- Hyperparameters tuned with `RandomizedSearchCV` (3-fold).

## Repository structure

```
.
├── data/
├── predicting_stellar_class.ipynb
├── submission.csv
├── pyproject.toml
└── README.md
```

## Running it

```bash
uv sync
```

Place the competition `train.csv` and `test.csv` in `data`, then run the notebook.

## What I'd do to climb the leaderboard

Treated as done for portfolio purposes, but the standard next steps would be: blend LightGBM / XGBoost / CatBoost probabilities, tune longer, and calibrate per-class thresholds for balanced accuracy.

---