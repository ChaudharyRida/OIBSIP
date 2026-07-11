# 📊 EDA on Retail Sales — Walmart Weekly Sales Analysis

## Objective
Perform a thorough Exploratory Data Analysis on Walmart's weekly retail sales data to uncover time-based trends, holiday impact, store performance patterns, and relationships with economic indicators — producing actionable business recommendations.

**Track:** Data Analytics — Oasis Infobyte SIP (Level 1, Task 1)

## Dataset
- **Source:** [Walmart Sales Dataset – Kaggle]
- **File:** `Walmart_sales.csv`
- **Size:** 6,435 rows × 8 columns
- **Coverage:** 45 Walmart stores, weekly sales from February 2010 to October 2012
- **Columns:** Store, Date, Weekly_Sales, Holiday_Flag, Temperature, Fuel_Price, CPI, Unemployment

## Tools & Libraries
- Python
- pandas — data loading, cleaning, and aggregation
- matplotlib & seaborn — data visualization
- Google Colab / Jupyter Notebook

## Analysis Steps
1. Data loading and initial inspection (shape, dtypes, null check)
2. Date column conversion to proper datetime format
3. Descriptive statistics on Weekly_Sales and economic indicators
4. Monthly and quarterly sales trend analysis (time series)
5. Holiday vs. non-holiday sales comparison
6. Top 10 store performance ranking (adapted from customer demographics, since this dataset does not include demographic fields)
7. Correlation heatmap: sales vs. economic factors
8. Monthly sales distribution (boxplot) — non-obvious insight
9. Business conclusions & recommendations

## Key Findings
- **No missing values** — the dataset was clean and required no imputation.
- **Strong seasonality:** December is consistently the highest-selling month each year, with 2010-12 and 2011-12 ranking as the two highest months in the entire dataset, driven by holiday shopping.
- **Holiday impact is real but moderate:** average weekly sales during holiday-flagged weeks are about **7.8% higher** ($1.12M vs. $1.04M) than non-holiday weeks — smaller than expected, suggesting a few specific weeks (Thanksgiving/Christmas) drive most of the effect rather than all flagged weeks uniformly.
- **Store performance varies significantly:** the top-performing stores generate meaningfully more revenue than lower-ranked stores, pointing to differences in location, size, or local demographics worth further investigation.
- **Weak correlation with macroeconomic factors:** Weekly_Sales showed very low correlation with Temperature (-0.06), Fuel_Price (+0.01), CPI (-0.07), and Unemployment (-0.11) — store-level and seasonal factors matter far more than broader economic conditions.
- **Variability spikes with sales in the holiday season:** December has both the highest average weekly sales (~$1.28M) and the widest spread in sales (std ≈ $774K) — roughly 60% higher variability than a typical mid-year month, making holiday-season sales both bigger and harder to predict.

## Business Recommendations
1. **Inventory planning:** Increase stock 3–4 weeks ahead of the November–December holiday season to meet the consistent seasonal demand spike.
2. **Store-specific strategy:** Study what top-performing stores are doing differently (location, size, local demographics) and look to replicate those practices at underperforming stores.
3. **Prioritize seasonal timing over macro conditions:** Since correlation with economic indicators is weak, marketing and promotional efforts should focus on seasonal calendar planning rather than reacting to fuel prices or unemployment trends.

## Files in This Folder
| File | Description |
|---|---|
| `EDA_Retail_Sales.ipynb` | Full analysis notebook |
| `Walmart_sales.csv` | Raw dataset used for analysis |
| `screenshots/` | Chart outputs from the notebook |

## Author
Rida Chaudhary — BS Business Data Analytics, COMSATS University Islamabad
