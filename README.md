# Dry Bean Classification

This project compares multiple classifiers using the UCI Dry Bean Dataset.

The main goals are:

- Understand the dataset and its features
- Compare different classification models
- Analyze model errors
- Study how training data size affects model performance
- Evaluate the final selected model on an unseen test set

## Dataset

The dataset used in this project is the
[UCI Dry Bean Dataset](https://archive.ics.uci.edu/dataset/602/dry+bean+dataset).

It contains:

- 13,611 samples
- 16 numerical features
- 7 bean classes

The seven classes are:

- BARBUNYA
- BOMBAY
- CALI
- DERMASON
- HOROZ
- SEKER
- SIRA

The data is fetched directly from the UCI Machine Learning Repository using the `ucimlrepo` package.

```python
from ucimlrepo import fetch_ucirepo

dry_bean = fetch_ucirepo(id=602)
```

## Models

- Dummy Classifier
- Logistic Regression
- Random Forest
- PyTorch Multilayer Perceptron (MLP)

## Experimental Setup

The dataset is divided using a stratified split:

- Training: 60%
- Validation: 20%
- Test: 20%

The same split is used for all models.

Models are compared using:

- Accuracy
- Macro-F1

## Installation

Install the required packages:

```bash
pip install -r requirements.txt