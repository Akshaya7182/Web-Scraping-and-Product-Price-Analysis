# Web Scraping & Product Price Analysis – Air Conditioners (Amazon India)

An end-to-end e-commerce data pipeline: **scrape** air-conditioner listings from Amazon India, **filter, extract, validate and clean** them,
**aggregate, analyse and visualise** the data, and **interpret** the results for buyers and sellers.

**Tools:** Python · Pandas · NumPy · Matplotlib · Requests · BeautifulSoup · SciPy · Google Colab / Jupyter

## Problem statement
Product prices, discounts and ratings on e-commerce sites are scattered over many pages and are hard to compare by hand.
This project collects AC listings automatically and analyses how **price, brand, capacity (tonnage), energy-star rating, features and discounts** relate to each other.

## The 8-stage pipeline

| Stage | Folder | Notebook | Output |
|---|---|---|---|
| 1 | `1. Data Loading and Reading` | `01_Data_Loading_and_Reading.ipynb` | first look at `Air_Conditioners_Raw.csv` |
| 2 | `2. Data Acquisition & Filtering` | `02_Data_Acquisition_and_Filtering.ipynb` (+ `amazon_ac_scraper.py`) | `Air_Conditioners_Filtered.csv` |
| 3 | `3. Data Extraction` | `03_Data_Extraction.ipynb` | `Air_Conditioners_Extracted.csv` |
| 4 | `4. Data Validation & Cleaning` | `04_Data_Validation_and_Cleaning.ipynb` | `Air_Conditioners_Cleaned.csv` |
| 5 | `5. Data Aggregation & Representation` | `05_Data_Aggregation_and_Representation.ipynb` | `0. DataSet/aggregates/*.csv` |
| 6 | `6. Data Analysis` | `06_Data_Analysis.ipynb` | Top-N tables, correlation matrix |
| 7 | `7. Data Visualization` | `07_Data_Visualization.ipynb` | `charts/*.png` |
| 8 | `8. Results & Interpretation` | `08_Results_and_Interpretation.ipynb` | `Results_Key_Findings.csv` |

Data flow: `Raw → Filtered → Extracted → Cleaned → aggregates / analysis → charts → results`

## Repository structure
```
Web_Scraping_and_Product_Price_Analysis/
├── 0. DataSet/                      # raw, intermediate and final CSV files
├── 1. Data Loading and Reading/
├── 2. Data Acquisition & Filtering/ # notebook + amazon_ac_scraper.py
├── 3. Data Extraction/
├── 4. Data Validation & Cleaning/
├── 5. Data Aggregation & Representation/
├── 6. Data Analysis/
├── 7. Data Visualization/
├── 8. Results & Interpretation/
├── requirements.txt
└── README.md
```

## How data was collected
Amazon India search result pages for the keyword *"air conditioner"* are downloaded with `requests` (browser-like headers, random delays,
retries) and parsed with `BeautifulSoup`. For every product card the scraper reads: name, image, link, rating, number of ratings,
selling price and MRP. Duplicate sponsored listings are removed by their ASIN (Amazon product id).
The raw scrape has **9 columns**; brand, tonnage, energy star, AC type, inverter / Wi-Fi flags and discounts are derived in Stages 3 and 4.

> Amazon blocks automated traffic and changes its HTML often, so the scraper may need CSS-selector updates. Scraping is slow, polite and for educational use only.
> Prices and discounts change daily – the dataset is a snapshot of the day it was scraped.

## Cleaning policy
- Missing prices / ratings are **kept blank – never filled with the median**, so averages and discounts are not distorted.
- Impossible values (for example **selling price > MRP**) are removed; discounts are calculated only from verified prices.
- Outliers are **flagged, not deleted**.

## Data dictionary (final cleaned file)
| Column | Meaning |
|---|---|
| name, image, link | product title, image URL, product page URL |
| ratings, no_of_ratings | customer rating (1–5) and number of ratings |
| discount_price | selling price (Rs) |
| actual_price | MRP (Rs) – blank when not verified |
| discount_amount, discount_percent | MRP − selling price; as % of MRP |
| tonnage, energy_star | cooling capacity and BEE star rating (from title) |
| brand, asin, ac_type | standardised brand, Amazon product id, Split / Window / Other |
| is_inverter, has_wifi | feature flags from title |
| price_available, price_outlier | helper flags |

## How to run
```bash
pip install -r requirements.txt
```
Open the notebooks in order (Google Colab or Jupyter) – Stage 1 → Stage 8. Every notebook finds its input automatically.
To scrape fresh data set `RUN_SCRAPER = True` in Stage 2 (or run `python "2. Data Acquisition & Filtering/amazon_ac_scraper.py"`) and re-run the stages.

## Team (Team 04)
| Member | Stages |
|---|---|
| M. Akshaya (25B11CS608) | 2. Data Acquisition & Filtering, 3. Data Extraction |
| P. Jagannadha Veera Manikanta (25B11CS710) | 4. Data Validation & Cleaning, 5. Data Aggregation & Representation |
| T. Yeghna Surya Teja (25B11CS923) | 1. Data Loading & Reading, 8. Results & Interpretation |
| K. Sai Krishna (25B11CS388) | 6. Data Analysis, 7. Data Visualization |

Guide: Mr. K. Ashok Teja, Assistant Professor, CSE Dept.
