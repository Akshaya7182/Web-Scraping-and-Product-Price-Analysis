# Stage 1 – Data Loading & Reading

**Presented by:** T. Yeghna Surya Teja (Yeghu)

**Files:** `01_Data_Loading_and_Reading.ipynb`

## What this stage does
Reads `Air_Conditioners_Raw.csv` with Pandas and inspects it: file size, raw text lines, shape, column names, data types, head/tail/sample, column profile (missing / unique values), summary statistics, `usecols`/`nrows` reading options and first impressions of problems.

## Output
Nothing is modified – a list of issues (missing prices, selling price > MRP, missing derived columns) is handed to later stages.

## Key techniques
`pd.read_csv`, `info()`, `describe()`, `value_counts()`

## How to run
Open the notebook in Google Colab or Jupyter and run the cells top to bottom. The notebook finds its input in `../0. DataSet/`
(or in `/content` / the current folder; in Colab it will ask you to upload the file if it is missing).
Run the stages in order 1 → 8 because each stage uses the output of the previous one.
