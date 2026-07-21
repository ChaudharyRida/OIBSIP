# 🧹 Data Cleaning — Marketing Campaign Dataset

## Objective
Take a real-world messy dataset and systematically clean it into an analysis-ready state, documenting every decision made along the way.

**Track:** Data Analytics — Oasis Infobyte SIP (Level 1, Task 3)

## Dataset
- **Source:** Kaggle — Customer Personality Analysis (Marketing Campaign dataset)
- **File:** `marketing_campaign.csv` (tab-separated)
- **Size:** 2,240 rows × 29 columns

## Tools & Libraries
- Python, pandas, numpy, Google Colab

## Cleaning Steps Performed
1. Data quality report (nulls, dtypes, duplicates)
2. Inspected categorical columns for inconsistent values
3. Standardized `Marital_Status` — merged "Alone" into "Single," reclassified nonsensical entries "Absurd" and "YOLO" as "Single"
4. Imputed 24 missing `Income` values using the median
5. Converted `Dt_Customer` from text to proper datetime format
6. Detected and removed 3 rows with implausible `Year_Birth` values (as early as 1893)
7. Detected 8 `Income` outliers using the IQR method (including one extreme value of $666,666) and capped them at the upper bound instead of removing them
8. Produced a before/after summary table
9. Saved cleaned dataset to a new CSV file

## Key Findings
| Metric | Before Cleaning | After Cleaning |
|---|---|---|
| Total Rows | 2,240 | 2,237 |
| Null Values (Income) | 24 | 0 |
| Duplicate Rows | 0 | 0 |
| Dt_Customer dtype | object (text) | datetime64 |

- `Marital_Status` contained clear data entry errors ("Absurd," "YOLO") alongside a semantically overlapping category ("Alone")
- Income was right-skewed (mean ~$52,247 vs. median ~$51,382), justifying median imputation over mean
- One extreme income outlier of $666,666 was capped at $117,418 (the IQR upper bound) rather than removed, preserving the customer's other valid behavioral data

## Files in This Folder
| File | Description |
|---|---|
| `Data_Cleaning_MarketingCampaign.ipynb` | Full cleaning notebook |
| `marketing_campaign.csv` | Original raw dataset |
| `marketing_campaign_cleaned.csv` | Cleaned output dataset |
| `screenshots/` | Key output screenshots |

## Author
Rida Chaudhary — BS Business Data Analytics, COMSATS University Islamabad, Lahore campus
