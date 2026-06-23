# HOKY Immobilien

![Python 3.11+](https://img.shields.io/badge/python-3.11%2B-blue)
![Flask](https://img.shields.io/badge/framework-Flask-orange)

## What this project does

HOKY Immobilien is a real-estate price prediction and visualization project for properties in Lower Saxony, Germany. It combines a trained machine learning pipeline, a Flask web application, and supporting scripts for data preparation, analysis, and mapping.

The repository includes:

- A Flask-based web UI that predicts property prices based on feature input.
- A model training pipeline that cleans data, engineers features, and compares candidate regression models.
- Data utilities for CSV-to-SQLite conversion, SQL querying, and district-level price mapping.
- Example notebooks and saved model artifacts for quick experimentation.

## Why this project is useful

- Provides a local property valuation engine for Niedersachsen real estate.
- Demonstrates feature engineering and model training for price prediction.
- Includes an interactive web app and reusable prediction scripts.
- Supports rapid iteration on models and data preprocessing.

## Key features

- `website/app.py`: Flask app serving price prediction pages and API endpoint.
- `scripts/train_model.py`: Train or retrain the predictive pipeline from `data/price_clean.csv`.
- `scripts/predict.py`: Run example property predictions with the trained model.
- `scripts/niedersachsen_map.py`: Generate an interactive price heatmap for Niedersachsen.
- `scripts/csv_to_sqlite.py` and `scripts/query_sqlite.py`: Convert and query listing data via SQLite.

## Getting started

### Prerequisites

- Python 3.11 or newer
- `pip`
- A local clone of this repository

### Install dependencies

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### Run the web app

```bash
python website/app.py
```

Then open `http://127.0.0.1:5000` in your browser.

### Run the sample predictor script

```bash
python scripts/predict.py
```

This script loads the saved pipeline from `model/price_model.joblib` and prints example predictions.

### Train the model from scratch

```bash
python scripts/train_model.py --data data/price_clean.csv --out model/price_model.joblib
```

This command trains the best candidate model on the cleaned dataset and saves the pipeline to `model/price_model.joblib`.

## Repository structure

- `website/`: Flask app, templates, and static frontend resources.
- `scripts/`: Training, prediction, data conversion, mapping, and email utilities.
- `model/`: Saved model artifacts and model source files.
- `data/`: Cleaned dataset and raw CSV data.
- `notebooks/`: Analysis and visualization notebooks.

## Where to get help

- Open an issue in this repository for bugs or feature requests.
- Review the source code in `website/app.py` and `scripts/train_model.py` for behavior details.
- Use the notebooks in `notebooks/` for data exploration and model insights.

## Contributing

Contributions are welcome via issues and pull requests. If you add features or fix bugs, keep changes focused and document any new dependencies.

If you want to extend the project, a good entry point is:

- `scripts/train_model.py` for model improvements
- `website/app.py` for web UI enhancements
- `scripts/niedersachsen_map.py` for map or visualization updates

---

*This README was generated to help developers get started with the HOKY Immobilien repository.*