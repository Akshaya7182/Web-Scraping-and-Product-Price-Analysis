# Stage 6 – Data Analysis

**Presented by:** K. Sai Krishna (Sai)

**Files:** `06_Data_Analysis.ipynb`

## What this stage does
Descriptive statistics, percentiles, correlation matrix, price-per-ton regression, energy-star premium with Welch t-test, brand premium, inverter / Wi-Fi effect, value-for-money, weighted rating and Top-N tables.

## Output
`Most_Expensive_Products.csv`, `Top_Discounted_Products.csv`, `Top_Rated_Products.csv`, `aggregates/correlation_matrix.csv`.

## Key techniques
`corr`, `np.polyfit`, `scipy.stats.ttest_ind`, weighted-rating formula

## How to run
Open the notebook in Google Colab or Jupyter and run the cells top to bottom. The notebook finds its input in `../0. DataSet/`
(or in `/content` / the current folder; in Colab it will ask you to upload the file if it is missing).
Run the stages in order 1 → 8 because each stage uses the output of the previous one.
