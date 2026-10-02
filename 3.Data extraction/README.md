# Stage 3 – Data Extraction

**Presented by:** M. Akshaya

**Files:** `03_Data_Extraction.ipynb`

## What this stage does
Extracts hidden attributes from product titles and links with regex: ASIN, tonnage, energy-star rating, standardised brand, AC type, inverter and Wi-Fi flags. Audits extraction coverage and builds numeric / categorical views.

## Output
`Air_Conditioners_Extracted.csv` (9 scraped columns + 7 extracted columns).

## Key techniques
`str.extract`, regex, `select_dtypes`, dictionary-based brand standardisation

## How to run
Open the notebook in Google Colab or Jupyter and run the cells top to bottom. The notebook finds its input in `../0. DataSet/`
(or in `/content` / the current folder; in Colab it will ask you to upload the file if it is missing).
Run the stages in order 1 → 8 because each stage uses the output of the previous one.
