# Stage 2 – Data Acquisition & Filtering

**Presented by:** M. Akshaya

**Files:** `02_Data_Acquisition_and_Filtering.ipynb`, `amazon_ac_scraper.py`

## What this stage does
Scrapes Amazon India air-conditioner search pages with `requests` + `BeautifulSoup` (switch `RUN_SCRAPER = True`), then filters the data: genuine-AC filter, valid link / unique ASIN, condition-based subsets, sorting and a filter funnel.

## Output
`Air_Conditioners_Raw.csv` (scraped) and `Air_Conditioners_Filtered.csv`.

## Key techniques
`requests`, `BeautifulSoup` CSS selectors, regex, boolean filtering, `sort_values`, `drop_duplicates`

## How to run
Open the notebook in Google Colab or Jupyter and run the cells top to bottom. The notebook finds its input in `../0. DataSet/`
(or in `/content` / the current folder; in Colab it will ask you to upload the file if it is missing).
Run the stages in order 1 → 8 because each stage uses the output of the previous one.
