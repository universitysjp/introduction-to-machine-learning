---
title: "Classification"
---

Use the classic Iris dataset to practice classification end-to-end.

What you'll learn
- Explore data and visualize classes
- Train/evaluate KNN and Logistic Regression
- Split train/test and tune k

Hands-on notebook
- Read the code below: [iris-data-for-beginners.ipynb](#iris-classification-notebook-code)
- Run the original notebook from the module's [notebooks folder on GitHub](https://github.com/universitysjp/introduction-to-machine-learning/tree/main/notebooks)
- Data: [Iris.csv](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/data/Iris.csv)

Outline
- EDA: pairplots, violin plots
- Train/test split
- KNN accuracy vs k
- Logistic Regression baseline

Next steps
- Trees and ensembles: [trees and ensembles](./trees-and-ensembles)
- Overfitting and regularization: [regularization and overfitting](./regularization-and-overfitting)


## Iris classification notebook code

The code cells below are included in the original `iris-data-for-beginners.ipynb` notebook in the module's [notebooks folder on GitHub](https://github.com/universitysjp/introduction-to-machine-learning/tree/main/notebooks).

```bash
pip install seaborn scikit-learn numpy
```

```python
import numpy as np
import pandas as pd
import seaborn as sns
sns.set_palette('husl')
import matplotlib.pyplot as plt
%matplotlib inline

from sklearn import metrics
from sklearn.neighbors import KNeighborsClassifier
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split

data = pd.read_csv("data/Iris.csv")
data.head()
```

```python
data.info()
```

```python
data.describe()
```

```python
 data['Species'].value_counts()
```

```python
tmp = data.drop('Id', axis=1)
g = sns.pairplot(tmp, hue='Species', markers='+')
plt.show()
```

```python
g = sns.violinplot(y='Species', x='SepalLengthCm', data=data, inner='quartile')
plt.show()
g = sns.violinplot(y='Species', x='SepalWidthCm', data=data, inner='quartile')
plt.show()
g = sns.violinplot(y='Species', x='PetalLengthCm', data=data, inner='quartile')
plt.show()
g = sns.violinplot(y='Species', x='PetalWidthCm', data=data, inner='quartile')
plt.show()
```

```python
X = data.drop(['Id', 'Species'], axis=1)
Y = data['Species']
# print(X.head())
print(X.shape)
# print(y.head())
print(Y.shape)
```

```python
# experimenting with different n values
k_range = list(range(1,26))
scores = []
for k in k_range:
    knn = KNeighborsClassifier(n_neighbors=k)
    knn.fit(X, Y)
    y_pred = knn.predict(X)
    scores.append(metrics.accuracy_score(Y, y_pred))

plt.plot(k_range, scores)
plt.xlabel('Value of k for KNN')
plt.ylabel('Accuracy Score')
plt.title('Accuracy Scores for Values of k of k-Nearest-Neighbors')
plt.show()
```

```python
logreg = LogisticRegression()
logreg.fit(X, Y)
y_pred = logreg.predict(X)
print(metrics.accuracy_score(Y, y_pred))
```

```python
 X_train, X_test, y_train, y_test = train_test_split(X, Y, test_size=0.4,random_state=5)
print(X_train.shape)
print(y_train.shape)
print(X_test.shape)
print(y_test.shape)
```

```python
 # experimenting with different n values
k_range = list(range(1,26))
scores = []
for k in k_range:
    knn = KNeighborsClassifier(n_neighbors=k)
    knn.fit(X_train, y_train)
    y_pred = knn.predict(X_test)
    scores.append(metrics.accuracy_score(y_test, y_pred))

plt.plot(k_range, scores)
plt.xlabel('Value of k for KNN')
plt.ylabel('Accuracy Score')
plt.title('Accuracy Scores for Values of k of k-Nearest-Neighbors')
plt.show()
```

```python
logreg = LogisticRegression()
logreg.fit(X_train, y_train)
y_pred = logreg.predict(X_test)
print(metrics.accuracy_score(y_test, y_pred))
```

```python
knn = KNeighborsClassifier(n_neighbors=12)
knn.fit(X, Y)
# make a prediction for an example of an out-of-sample observation
knn.predict([[6, 3, 4, 2]])
```
