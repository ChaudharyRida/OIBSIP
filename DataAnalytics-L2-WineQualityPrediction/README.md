# 🍷 Wine Quality Prediction — Multi-Model Classification

## Objective
Train and compare multiple classification models to predict wine quality (grouped into low/medium/high categories) based on physicochemical properties.

**Track:** Data Analytics — Oasis Infobyte SIP (Level 2, Task 2)

## Dataset
- **Source:** UCI Machine Learning Repository / Kaggle — Red Wine Quality Dataset
- **File:** `winequality-red.csv` (semicolon-separated)
- **Size:** 1,599 rows × 12 columns (11 chemical features + quality score)

## Tools & Libraries
- Python, pandas, numpy, scikit-learn (RandomForestClassifier, SGDClassifier, SVC, StandardScaler), matplotlib, seaborn, Google Colab

## Analysis Steps
1. Loaded dataset and inspected class distribution (highly imbalanced across quality scores 3–8)
2. Explored feature distributions and correlation with quality
3. Discussed class imbalance and its modeling implications
4. Binned quality scores into 3 practical classes: low (3–4), medium (5–6), high (7–8)
5. Standardized features and performed a stratified train/test split
6. Trained 3 classifiers: Random Forest, SGD, and SVC
7. Evaluated each model using accuracy, classification report, and confusion matrices
8. Extracted feature importance from the Random Forest model
9. Compared all models side-by-side

## Key Findings
| Model | Accuracy |
|---|---|
| **Random Forest** | **86.9%** (best) |
| SVC | 84.4% |
| SGD | 82.8% |

- **Alcohol** (correlation: 0.48) and **volatile acidity** (correlation: -0.39) were the two strongest predictors of wine quality — confirmed independently by both correlation analysis and Random Forest feature importance
- All three models achieved strong performance on "medium" quality wines (the majority class) but **completely failed on "low" quality wines** (0.00 precision/recall/F1 across all models), due to severe class imbalance — only 50 "low" examples existed in the training set versus 1,055 "medium" examples
- Random Forest was selected as the best-performing and most deployment-suitable model, given its higher accuracy and interpretable feature importance output

## Limitations & Future Work
The current models cannot reliably identify low-quality wines due to insufficient training examples for that class. Future improvement would require either collecting more low-quality wine samples or applying a class-imbalance technique such as SMOTE oversampling or class weighting.

## Files in This Folder
| File | Description |
|---|---|
| `Wine_Quality_Prediction.ipynb` | Full modeling and evaluation notebook |
| `winequality-red.csv` | Dataset used for analysis |
| `screenshots/` | Key chart and output screenshots |

## Author
Rida Chaudhary — BS Business Data Analytics, COMSATS University Islamabad, Lahore campus
