 Web Scraping & Product Price Analysis – Amazon India Air Conditioners
📌 Project Overview
This project performs a complete data-analysis workflow on Amazon India Air Conditioner listings using Python.

We collected 720 raw product listings through web scraping and transformed them into structured insights about prices, discounts, brands, tonnage, and energy ratings. After cleaning and preprocessing, the dataset was reduced to 652 genuine AC listings, enabling clear analysis of pricing trends and market patterns.

The workflow demonstrates how raw e-commerce data can be converted into statistical summaries, visual insights, and buyer-focused conclusions.

🎯 Problem Statement
E-commerce platforms list thousands of products with constantly changing prices, discounts, and ratings.
Manually comparing this scattered information is:

Time-consuming

Error-prone

Difficult to scale

This project addresses the following question:

How do price, brand, tonnage, energy rating, and discounts influence AC market patterns on Amazon India?

🏆 Objectives
Scrape product listings from Amazon India.

Clean and preprocess raw data (remove non-AC items, convert text to numbers, extract tonnage/energy-star/brand).

Perform Exploratory Data Analysis (EDA) using Pandas, NumPy, and Matplotlib.

Study price distributions, brand-wise pricing, tonnage-wise trends, energy-star shares, and discount patterns.

Visualize insights with bar charts, pie charts, histograms, scatter plots, and correlation heatmaps.

Summarize findings to support buyers and sellers in making informed decisions.

📂 Dataset Information
Source: Amazon India – Air Conditioner Listings (March 2023)

Raw Records: 720

Final Records: 652 genuine ACs

Attributes:

Product Name (brand, tonnage, stars extracted)

Ratings / Number of Ratings

Discount Price (₹)

Actual Price (₹)

Tonnage / Energy Star

Discount Percentage

Brand

🛠️ Tools & Technologies
Programming Language: Python

Libraries: Pandas, NumPy, Matplotlib

Platforms: Google Colab / Jupyter Notebook

OS: Windows

📊 Key Insights
Median AC price: ₹39,990 (mean ₹43,104)

Price range: ₹24,990 – ₹1,28,800

Average discount: 29.1% (max 57.3%)

Top Discounts: Lloyd, Haier, Voltas, LG

Most Expensive Brand: O General (~₹58k avg, only 9% off)

Cheapest Brands: Godrej & Lloyd (~₹35k avg)

Tonnage Trends: 1.5-ton ACs form ~50% of listings; price rises with tonnage (r = 0.67)

Energy Ratings: 59% are 3-star, 29% are 5-star; 5-star models cost ~₹5k more

Price vs Rating: Almost uncorrelated (r = −0.05) → higher price ≠ better rating

🔄 Project Workflow
Web Scraping → Collect raw AC listings

Data Cleaning → Convert text to numbers, remove non-AC items

Preprocessing → Extract tonnage, energy star, brand

EDA → Analyze price, discount, rating distributions

Visualization → Charts & heatmaps for trends

Insights & Reporting → Summarize findings

📌 Repository Structure
Code
AirConditioner_Price_Analysis/
│
├── Dataset/
│   └── amazon_ac_listings.csv
│
├── 1. Data Collection/
│   ├── Web_Scraping.ipynb
│   └── Output.csv
│
├── 2. Data Cleaning/
│   ├── Data_Cleaning.ipynb
│   └── Output.csv
│
├── 3. Data Preprocessing/
│   ├── Preprocessing.ipynb
│   └── Output.csv
│
├── 4. Data Analysis/
│   ├── EDA.ipynb
│   └── Output.pdf
│
├── 5. Data Visualization/
│   ├── Visualizations.ipynb
│   └── Charts.pdf
│
├── PPTs/
│   └── Air_Conditioners_Data_Analysis.pptx
│
├── Abstract/
│   └── Web_Scraping_Product_Price_Analysis_Abstract_Team4.pdf
│
└── README.md



👥 Team Details
Team Number: 4

25B11CS608 – M. Akshaya

25B11CS710 – P. Jagannadha Veera Manikanta

25B11CS388 – K. Sai Krishna

25B11CS923 – T. Yeghna Surya Teja

Guide: Mr. K. Ashok Teja, Assistant Professor, CSE Dept.

🚀 Future Scope
Scrape prices over time to track trends.

Predict AC prices using regression models.

Perform sentiment analysis on customer reviews.

Build interactive dashboards for real-time monitoring.
