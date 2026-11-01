# Predicting Credit Card Default: A Cost Sensitive Approach

CT4101 ML Project Portfolio, NUIG

## Can a classification model use a clients last 6 months of payments and details to predict if the client defaults next months payment? And what threshold ensures the banks cost is as low as possible, as missing a defaulter costs more money than falsely flagging a reliable customer?

## The Dataset
Default of Credit Card Clients (UCI #350), Yeh (2009), CC BY 4.0
DOI: https://doi.org/10.24432/C55S3H
Look at data/README.md for how to get all the data

## Setup(Python)
1. Clone the repo
2. Make a virtual environment; python -m venv <pathname>
3. Activate: <pathname>\Scripts\activate
4. Install all packages: pip install -r requirements.txt
5. Download the dataset into data/default of credit card clients.xls

## Run
1. From the repo root run jupyter notebook
2. Open and run in this order:
   1. notebooks/01_data_audit.ipynb (This audits the dataset, checking for missing values, duplicates and outliers)
   2. notebooks/02_baseline.ipynb (Preprocessing, cleans the data, does the stratified train/validation/test split, builds the preprocessing pipeline, adds majority class baseline and cost metric)