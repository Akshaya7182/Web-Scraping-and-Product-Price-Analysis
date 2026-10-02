# Stage 4 – Data Validation & Cleaning

**Presented by:** P. Jagannadha Veera Manikanta (Jagan)

**Files:** `04_Data_Validation_and_Cleaning.ipynb`

## What this stage does
Checks missing values, duplicates, data types, text consistency, value ranges and MRP-vs-selling-price consistency; blanks impossible values (no median filling), derives discount columns from verified prices only, flags price outliers (IQR) and prints a before/after scorecard.

## Output
`Air_Conditioners_Cleaned.csv`.

## Key techniques
`isna`, `duplicated`, `to_numeric(errors='coerce')`, IQR rule, boolean masks

## How to run
Open the notebook in Google Colab or Jupyter and run the cells top to bottom. The notebook finds its input in `../0. DataSet/`
(or in `/content` / the current folder; in Colab it will ask you to upload the file if it is missing).
Run the stages in order 1 → 8 because each stage uses the output of the previous one.
