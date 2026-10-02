# Stage 5 – Data Aggregation & Representation

**Presented by:** P. Jagannadha Veera Manikanta (Jagan)

**Files:** `05_Data_Aggregation_and_Representation.ipynb`

## What this stage does
Summarises listings by brand, tonnage, energy star, AC type, inverter and Wi-Fi; builds price bands, a pivot table, a cross-tabulation, brand rankings and a wide→long (`melt`) representation.

## Output
10 summary tables in `0. DataSet/aggregates/`.

## Key techniques
`groupby`, `pivot_table`, `crosstab`, `pd.cut`, `rank`

## How to run
Open the notebook in Google Colab or Jupyter and run the cells top to bottom. The notebook finds its input in `../0. DataSet/`
(or in `/content` / the current folder; in Colab it will ask you to upload the file if it is missing).
Run the stages in order 1 → 8 because each stage uses the output of the previous one.
