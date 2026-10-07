---
title: "Getting Started"
---

Goal: set up your environment and run your first notebooks in this repo.

What you'll learn
- Install Python and Jupyter
- Open and run notebooks
- Understand the repository layout

Prerequisites
- Python 3.9+ (3.10+ recommended)
- pip or conda

Quick setup (pip)
1) Create a virtual environment
   - macOS/Linux: `python3 -m venv .venv && source .venv/bin/activate`
2) Install basics: `pip install -U jupyter numpy pandas seaborn scikit-learn matplotlib`
3) Start Jupyter: `jupyter notebook`

First notebooks
- Intro to Jupyter: [read the code below](#intro-notebook-code)
- Data cleaning (Iris): follow the [Data Preprocessing lesson](./data-preprocessing)
- Classification on Iris: follow the [Classification lesson](./classification)
- To run the original notebooks, open the module's [notebooks folder on GitHub](https://github.com/universitysjp/introduction-to-machine-learning/tree/main/notebooks)

Datasets
- Small CSVs live in data/
- Iris dataset: [Iris.csv](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/data/Iris.csv)
- Iris (with missing values for cleaning practice): [Iris for cleaning.csv](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/data/Iris%20for%20cleaning.csv)

Next steps
- Continue to: [data preprocessing](./data-preprocessing)
- Or jump to: [classification](./classification)


## Intro notebook code

The code cells below are included in the original `intro.ipynb` notebook in the module's [notebooks folder on GitHub](https://github.com/universitysjp/introduction-to-machine-learning/tree/main/notebooks).

```python
print("Hello World!")
```

```python
# Variable declaration
a = 5
b = 3
# Arithmetic operations
sum_result = a + b
difference_result = a - b
product_result = a * b
quotient_result = a / b
print("Sum:", sum_result)
print("Difference:", difference_result)
print("Product:", product_result)
print("Quotient:", quotient_result)
```

```python
# Data types
integer_var = 10
float_var = 3.14
string_var = "Hello"
print("Integer Variable:", integer_var)
print("Float Variable:", float_var)
print("String Variable:", string_var)
```

```python
# List creation
numbers = [10, 5, 8, 15, 7]
# List operations
sum_of_numbers = sum(numbers)
average_of_numbers = sum_of_numbers / len(numbers)
sorted_numbers = sorted(numbers)
print("Sum of Numbers:", sum_of_numbers)
print("Average of Numbers:", average_of_numbers)
print("Sorted Numbers:", sorted_numbers)
```

```python
# Looping through the list
for num in numbers:
    print("Current Number:", num)
# While loop example
i = 0
while i < len(numbers):
    print("Current Number (while loop):", numbers[i])
    i += 1
```

```bash
pip install pandas
```

```python
import pandas as pd
# Creating a DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie'],
'Age': [25, 30, 22],
'City': ['New York', 'San Francisco', 'Los Angeles']}
df = pd.DataFrame(data)
print(df)
```

```python
# Accessing columns
names = df['Name']
ages = df['Age']
# Adding a new column
df['Gender'] = ['Female', 'Male', 'Male']
print("Names:", names)
print("Ages:", ages)
print("Modified DataFrame:")
print(df)
```

```python
# Creating a text file with sample data
with open('data.txt', 'w') as file:
    file.write("This is sample data.\nLine 2: More data.")
```

```python
# Reading and printing contents of the file
with open('data.txt', 'r') as file:
    file_contents = file.read()
print("File Contents:")
print(file_contents)
```

```python
# Reading CSV file into DataFrame
df_csv = pd.read_csv(r'C:\Users\ICT-LAPTOP\Downloads\sample_dataset.csv')
```

```python
# Displaying DataFrame head, tail, and descriptive statistics
print("DataFrame Head:")
print(df_csv.head())
print("DataFrame Tail:")
print(df_csv.tail())
print("DataFrame Descriptive Statistics:")
print(df_csv.describe())
```

```bash
pip install matplotlib
```

```python
import matplotlib.pyplot as plt
# Plotting a simple graph
x = [1, 2, 3, 4, 5]
y = [10, 5, 8, 15, 7]
plt.plot(x, y)
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.title('Simple Plot')
plt.show()
```
