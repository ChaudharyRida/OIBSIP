# 🎯 Customer Segmentation Analysis — RFM & K-Means Clustering

## Objective
Segment customers into distinct behavioral groups using RFM (Recency, Frequency, Monetary) analysis and K-Means clustering, to enable targeted marketing strategies.

**Track:** Data Analytics — Oasis Infobyte SIP (Level 1, Task 2)

## Dataset
- **Source:** Cleaned output from the Data Cleaning task (`marketing_campaign_cleaned.csv`)
- **Size:** 2,237 rows (post-cleaning)

## Tools & Libraries
- Python, pandas, scikit-learn (KMeans, StandardScaler), matplotlib, seaborn, Google Colab

## Analysis Steps
1. Loaded the pre-cleaned dataset and confirmed zero missing values
2. Built RFM features: **Recency** (existing column), **Frequency** (sum of web + catalog + store purchases), **Monetary** (sum of all product category spend)
3. Standardized RFM features using `StandardScaler`
4. Applied the Elbow Method to determine optimal cluster count (K=4)
5. Ran K-Means clustering and assigned each customer a cluster
6. Visualized clusters across two feature-pair combinations
7. Profiled each cluster's average RFM values
8. Analyzed customer distribution across clusters
9. Developed marketing recommendations per segment

## Key Findings
**Average customer behavior:** ~12.5 purchases, ~$605.74 total spend, ~49 days since last purchase.

**Cluster Profiles:**

| Cluster | Recency (days) | Frequency | Monetary | Segment Type |
|---|---|---|---|---|
| 0 | 73.5 | 7.0 | $146.37 | Low-Value Lapsed Customers |
| 1 | 73.1 | 19.2 | $1,181.34 | High-Value Lapsed Customers |
| 2 | 23.5 | 7.1 | $151.58 | Low-Value Active Customers |
| 3 | 22.9 | 19.8 | $1,183.09 | VIP Active Customers |

The data reveals a clean two-way split: Recency separates "lapsed" (~73 days) from "active" (~23 days) customers, while Frequency/Monetary separates "low-value" (~7 purchases, ~$150) from "high-value" (~19-20 purchases, ~$1,180) customers.

## Marketing Recommendations
1. **VIP Active Customers (Cluster 3):** Highest priority — reward with loyalty programs and early access to new products to maintain engagement.
2. **High-Value Lapsed Customers (Cluster 1):** Critical win-back opportunity — these customers have proven high lifetime value but have gone quiet; target with personalized re-engagement campaigns.
3. **Low-Value Active Customers (Cluster 2):** Currently engaged but low-spending — good candidates for upselling and cross-sell campaigns.
4. **Low-Value Lapsed Customers (Cluster 0):** Lowest priority — minimal investment recommended given low historical value and inactivity.

## Files in This Folder
| File | Description |
|---|---|
| `Customer_Segmentation.ipynb` | Full clustering analysis notebook |
| `marketing_campaign_cleaned.csv` | Cleaned dataset used for analysis |
| `screenshots/` | Key chart screenshots |

## Author
Rida Chaudhary — BS Business Data Analytics, COMSATS University Islamabad, Lahore campus
