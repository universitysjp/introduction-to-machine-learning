---
title: "Getting Started"
---

# Getting Started

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
- Intro to Jupyter: [intro.ipynb](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/notebooks/intro.ipynb)
- Data cleaning (Iris): [data-cleaning.ipynb](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/notebooks/data-cleaning.ipynb)
- Classification on Iris: [iris-data-for-beginners.ipynb](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/notebooks/iris-data-for-beginners.ipynb)

Datasets
- Small CSVs live in data/
- Iris dataset: [Iris.csv](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/data/Iris.csv)
- Iris (with missing values for cleaning practice): [Iris for cleaning.csv](https://github.com/universitysjp/introduction-to-machine-learning/blob/main/data/Iris%20for%20cleaning.csv)

Next steps
- Continue to: [data preprocessing](./data-preprocessing)
- Or jump to: [classification](./classification)
