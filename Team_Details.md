# Team Contributions

## Project

**Web Scraping & Product Price Analysis — Air Conditioners (Amazon India)**

## Team Members

| Roll Number | Member                       | Role                    | Assigned Work                                                    |
| ----------- | ---------------------------- | ------------------------ | ----------------------------------------------------------------- |
| 25B11CS608  | M. Akshaya                   | Team Lead                | Data Collection (Web Scraping); Project Coordination & Requirements |
| 25B11CS710  | P. Jagannadha Veera Manikanta | Data Lead                | Data Cleaning & Validation; Feature Extraction & Preprocessing     |
| 25B11CS388  | K. Sai Krishna                | Tech Lead                | Data Aggregation & Analysis; Code Implementation                  |
| 25B11CS923  | T. Yeghna Surya Teja           | Q&A and Strategy Lead    | Data Visualization; Results, Insights & Conclusion                 |

## Individual Responsibilities

### M. Akshaya (25B11CS608) — Team Lead — Data Collection (Web Scraping); Project Coordination & Requirements

- Scraping air conditioner listings from Amazon India (name, price, rating, link, etc.).
- Loading the scraped CSV dataset using Pandas.
- Checking dataset shape, column names, and data types.
- Inspecting initial records and verifying listing categories.
- Coordinating task allocation and integrating each member's work into the final notebook and presentation.
- Defining hardware and software requirements for the project.

### P. Jagannadha Veera Manikanta (25B11CS710) — Data Lead — Data Cleaning & Validation; Feature Extraction & Preprocessing

- Converting text price, rating, and review-count fields into numeric values.
- Checking and handling missing values without median-filling, to avoid distorting price and discount statistics.
- Checking and removing duplicate listings.
- Validating price and rating ranges (e.g. removing listings where selling price exceeds MRP).
- Extracting tonnage, energy star rating, and brand from product names.
- Filtering out non-AC items (stands, motors, portable coolers, etc.) from the dataset.

### K. Sai Krishna (25B11CS388) — Tech Lead — Data Aggregation & Analysis; Code Implementation

- Grouping listings by brand, tonnage, and energy star rating using Pandas.
- Calculating average price, average discount percentage, and average rating per group.
- Computing overall summary statistics (median/mean price, price range, discount range).
- Computing correlations between price, discount, tonnage, star rating, and customer rating.
- Structuring and maintaining the Colab notebook code end-to-end.

### T. Yeghna Surya Teja (25B11CS923) — Q&A and Strategy Lead — Data Visualization; Results & Interpretation

- Creating visualizations using Matplotlib: brand-wise price bar chart, energy star pie chart, price distribution histogram, correlation heatmap, and price-vs-rating scatter plot.
- Comparing brand, tonnage, and star-rating patterns visually.
- Bringing together numerical and visual results into key findings.
- Preparing insights, conclusion, and future scope.
- Preparing the team for questions and anchoring the presentation strategy.

## Team Responsibility

Although responsibilities are divided for detailed stage-wise work, all four team members are responsible for understanding the complete project and being able to explain the overall data-analysis workflow, Pandas operations, analysis, visualizations, results, and conclusions.
