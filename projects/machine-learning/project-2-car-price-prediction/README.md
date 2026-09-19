# Outlier Handling Comparison for Regression Models

This project compares the impact of different outlier-handling strategies on regression model performance, and evaluates the effect of hyperparameter tuning on top of each strategy.

## 🎯 Objective

To find out:
1. Whether removing outliers improves regression model performance
2. Which outlier detection method (Z-Score vs IQR) works better for this dataset
3. How much additional improvement hyperparameter tuning provides on top of outlier handling

## 🛠️ Methodology

- **Models compared:** Lasso, Linear Regression, Random Forest Regressor
- **Metric:** R² Score
- **Outlier detection methods:**
  - **Z-Score** — flags a row as an outlier if any numeric column has `|z| > 3`
  - **IQR (Interquartile Range)** — flags a row as an outlier if any numeric column falls outside `Q1 - 1.5*IQR` to `Q3 + 1.5*IQR`
- **Tuning methods (Random Forest only):** `RandomizedSearchCV` and `GridSearchCV`

## 📊 Results

### Raw Data (No Outlier Handling)

| Model | R² Score |
|---|---|
| Lasso | 0.4031 |
| Linear Regression | 0.4031 |
| Random Forest Regressor | 0.5085 |

**After Tuning (Random Forest Regressor):**
| Method | R² Score |
|---|---|
| RandomizedSearchCV | 0.5280 |
| GridSearchCV | 0.5245 |

---

### Z-Score Outlier Handling

| Model | R² Score |
|---|---|
| Lasso | 0.5042 |
| Linear Regression | 0.5042 |
| Random Forest Regressor | 0.5887 |

**After Tuning (Random Forest Regressor):**
| Method | R² Score |
|---|---|
| RandomizedSearchCV | 0.6077 |
| GridSearchCV | 0.6033 |

---

### IQR Outlier Handling

| Model | R² Score |
|---|---|
| Lasso | 0.5445 |
| Linear Regression | 0.5445 |
| Random Forest Regressor | 0.5953 |

**After Tuning (Random Forest Regressor):**
| Method | R² Score |
|---|---|
| RandomizedSearchCV | 0.6047 |
| GridSearchCV | 0.6025 |

## 📈 Summary Comparison

| Condition | Lasso | Linear Regression | Random Forest (default) | RF Tuned (best) |
|---|---|---|---|---|
| Raw | 0.4031 | 0.4031 | 0.5085 | 0.5280 |
| Z-Score | 0.5042 | 0.5042 | 0.5887 | **0.6077** |
| IQR | **0.5445** | **0.5445** | 0.5953 | 0.6047 |

## 🔍 Key Findings

- **Outlier handling clearly helps.** Every model improves noticeably after removing outliers compared to raw data, regardless of which method is used.
- **IQR gives a bigger boost to linear models** (Lasso and Linear Regression jump from ~0.40 to ~0.54), while Z-Score gives a slightly bigger boost to Random Forest (best tuned score: 0.6077 vs 0.6047).
- **Hyperparameter tuning adds a smaller, but consistent improvement** (roughly +0.01 to +0.02 R²) on top of outlier handling — outlier handling has a much larger impact on performance than tuning alone.
- **Random Forest consistently outperforms the linear models** across all conditions, suggesting the relationship between features and the target is likely non-linear.

## 💡 Next Steps

- Investigate why Z-Score and IQR affect linear vs tree-based models differently (e.g. compare which specific rows each method removes)
- Try different thresholds (e.g. IQR multiplier of 2.0–3.0, or Z-score threshold of 2.5) to find a better trade-off between data retention and outlier removal
- Consider capping/winsorizing as an alternative to row removal, to avoid losing potentially useful data
- Check residual plots for Lasso/Linear Regression to confirm whether the linear assumption is a limiting factor

## 🛠️ Tools Used

- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-Learn 
- SciPy 
