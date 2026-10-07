---
title: "Data Preprocessing"
---

Learn the basics of cleaning and preparing data before modeling.

What you'll learn
- Inspect missing values
- Fill, forward/backward fill, and interpolate
- Basic visualization of missingness

Hands-on notebook
- Open: [data-cleaning.ipynb](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/notebooks/data-cleaning.ipynb)
- Data used: [Iris for cleaning.csv](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/data/Iris%20for%20cleaning.csv)

Key steps covered
- df.isnull().sum(), heatmaps of missingness
- Strategies: dropna, fillna(0), ffill, bfill, interpolate

Tips
- Keep a copy of raw data
- Track which columns are imputed

Next steps
- Move to classification with Iris: [classification](./classification)
- Or read more: [regularization and overfitting](./regularization-and-overfitting)
