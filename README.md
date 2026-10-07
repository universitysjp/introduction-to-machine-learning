# Introduction to Machine Learning

Beginner-friendly notebooks and topic pages to learn ML hands-on.

## Quickstart

1) Create a virtual environment
- macOS/Linux: `python3 -m venv .venv && source .venv/bin/activate`
2) Install basics: `pip install -U jupyter numpy pandas seaborn scikit-learn matplotlib`
3) Launch: `jupyter notebook`

## How to use this repo

- Start with a topic page in docs/, then open the linked notebook in notebooks/.
- Data files are in data/; notebooks expect relative paths like data/Iris.csv.

## Learning path (Beginner)

- Getting started: docs/en/getting-started.md
- Data preprocessing: docs/en/data-preprocessing.md → notebooks/data-cleaning.ipynb
- Classification (Iris): docs/en/classification.md → notebooks/iris-data-for-beginners.ipynb
- Next topics: docs/en/trees-and-ensembles.md, docs/en/unsupervised-learning.md, docs/en/regularization-and-overfitting.md, docs/en/regression.md

## Repository structure

- docs/ — topic pages and guidance
- notebooks/ — hands-on notebooks
  - intro.ipynb
  - data-cleaning.ipynb
  - iris-data-for-beginners.ipynb
- data/ — small CSV datasets
  - Iris.csv
  - Iris for cleaning.csv
- exercises/ and solutions/ — practice (WIP)
- src/ — optional helpers (WIP)

## Progress tracker

- [ ] Getting Started
- [ ] Data Preprocessing
- [ ] Classification
- [ ] Trees & Ensembles
- [ ] Unsupervised Learning
- [ ] Regularization & Overfitting
- [ ] Regression

## Contributing

See CONTRIBUTING.md. Beginners welcome—docs updates, typo fixes, small notebooks are great first PRs.

## License

MIT. See LICENSE.

---

Legacy content from the previous long-form README is archived in docs/legacy/README-legacy.md.
