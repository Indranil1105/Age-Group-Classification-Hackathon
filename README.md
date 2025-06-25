## Age Group Classification Hackathon

This repository contains the solution for a binary classification hackathon task: predicting whether a respondent is an "Adult" (0) or "Senior" (1) based on health and demographic features. The project demonstrates data preprocessing, exploratory data analysis (EDA), feature engineering, and machine learning model development using Python and scikit-learn.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Getting Started](#getting-started)
- [How to Run](#how-to-run)
- [Modeling Approach](#modeling-approach)
- [Submission Format](#submission-format)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

The goal is to classify individuals into two age groups:
- **Adult (0):** Respondents under 65 years of age.
- **Senior (1):** Respondents 65 years old and older.

You are provided with anonymized health and demographic data. The challenge is to preprocess the data, handle missing values, engineer features if needed, and build a robust machine learning model for accurate predictions.

---

## Dataset

The dataset consists of three CSV files:

- `train.csv` — Training data with features and target (`age_group`)
- `test.csv` — Test data with features only (no target)
- `sample-submission.csv` — Sample format for submission

**Note:** The dataset may contain missing values.

---

## Features

- `SEQN` — Sequence number (identifier)
- `RIAGENDR` — Gender (1=Male, 2=Female)
- `PAQ605` — Physical activity response
- `BMXBMI` — Body Mass Index
- `LBXGLU` — Glucose level
- `DIQ010` — Diabetes questionnaire response
- `LBXGLT` — Glucose tolerance (Oral)
- `LBXIN` — Insulin level
- `age_group` — Target: 0 (Adult), 1 (Senior) [**only in train.csv**]

---

## Getting Started

### Requirements

- Python 3.7+
- pandas
- scikit-learn
- numpy

### Installation

Install dependencies using pip:

pip install -r requirements.txt

text

Or individually:

pip install pandas scikit-learn numpy

text

---

## How to Run

1. **Clone the repository:**
git clone https://github.com/yourusername/age-group-classification-hackathon.git
cd age-group-classification-hackathon


2. **Add the dataset files** (`train.csv`, `test.csv`, `sample-submission.csv`) to the project directory.

3. **Run the main script:**
python main.py


This will generate a `submission.csv` file with your predictions.

---

## Modeling Approach

- **Data Cleaning:** Median imputation for missing values.
- **Feature Selection:** Dropped identifier column (`SEQN`).
- **Model:** Random Forest Classifier.
- **Validation:** 80/20 train/validation split.
- **Prediction:** Generates a submission file in the required format.

---

## Submission Format

The output file `submission.csv` will have:

age_group
0
1
0
...

- Only the `age_group` column, as shown in `sample-submission.csv`.
- Values: 0 (Adult), 1 (Senior).

---

## Results

- **Validation Accuracy:** ~87% (on sample split)
- **Model:** Random Forest Classifier
- **Handling Missing Values:** Median imputation

---

## Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change or improve.

---

## License

This project is for educational purposes only. Data provided is for hackathon use and not for commercial redistribution.

---

## Acknowledgements

- [scikit-learn](https://scikit-learn.org/)
- [pandas](https://pandas.pydata.org/)
- [NHANES Dataset (modified for hackathon)](https://www.cdc.gov/nchs/nhanes/)
