---
title: "Data Preprocessing"
---

Learn the basics of cleaning and preparing data before modeling.

What you'll learn
- Inspect missing values
- Fill, forward/backward fill, and interpolate
- Basic visualization of missingness

Hands-on notebook
- Read the code below: [data-cleaning.ipynb](#data-cleaning-notebook-code)
- Run the original notebook from the module's [notebooks folder on GitHub](https://github.com/universitysjp/introduction-to-machine-learning/tree/main/notebooks)
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


## Data-cleaning notebook code

The code cells below are included in the original `data-cleaning.ipynb` notebook in the module's [notebooks folder on GitHub](https://github.com/universitysjp/introduction-to-machine-learning/tree/main/notebooks).

```python
import numpy as np
import pandas as pd
import seaborn as sns

import os
for dirname, _, filenames in os.walk('/kaggle/input/iris-data'):

print(os.listdir())
```

```python
df = pd.read_csv("data/Iris for cleaning.csv")
df
```

```python
 df.isnull().sum()
```

```python
missing_value = ["N/A","na",np.nan]
df = pd.read_csv("data/Iris for cleaning.csv", na_values=missing_value)
df
```

```python
 df.isnull().sum()
```

```python
 sns.heatmap(df.isnull(),yticklabels=False, annot=True)
```

```python
df_nulldropped = df.dropna(how = "all")
df_nulldropped
```

```python
df_fillwithzero = df.fillna(0)
df_fillwithzero
```

```python
df_forwardfilled = df.fillna(method = 'ffill')
df_forwardfilled
```

```python
df_backwardfilled = df.fillna(method = 'bfill')
df_backwardfilled
```

```python
df_interpolate = df_nulldropped.interpolate()
df_interpolate
```
