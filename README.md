::: {align="center"}
# Loan Applications --- Statistical Analysis

### Python \| Statistics \| Probability \| Data Visualization \| Linear Algebra

**Author: Rami Ashutosh**

A practical data-analysis project exploring loan application patterns
using a synthetic dataset of 5,000 records.
:::

------------------------------------------------------------------------

## 📌 Project Overview

This project applies core statistical and mathematical concepts to a
loan applications dataset. Using Python, it explores customer income,
requested loan amounts, credit scores, and default status through
descriptive statistics, probability calculations, visualizations, and
vector operations.

> **Important:** This project uses synthetic practice data. It does not
> contain real customer information and must not be used to make real
> lending or credit decisions.

## 🎯 Project Objectives

-   Summarize customer income using mean, median, and mode.
-   Measure loan-amount variation using range, variance, and standard
    deviation.
-   Estimate the observed probability of loan default.
-   Compare credit-score ranges with default status using a contingency
    table.
-   Calculate conditional probability for customers with credit scores
    below 600.
-   Visualize credit-score distribution with a histogram and Gaussian
    reference curve.
-   Examine loan-amount skewness and kurtosis.
-   Assess income distribution with a Q-Q plot.
-   Apply linear algebra to customer income and loan-amount vectors.

## 📂 Dataset Information

**File:** `loan_applications_5000_records.csv`\
**Records:** 5,000\
**Columns:** 7\
**Format:** CSV

  Column               Data type   Description
  -------------------- ----------- --------------------------------------------
  `Customer_ID`        Text        Unique sample customer identifier
  `Age`                Integer     Customer age
  `Income`             Integer     Sample customer income, represented in INR
  `Loan_Amount`        Integer     Requested loan amount, represented in INR
  `Credit_Score`       Integer     Sample credit score
  `Loan_Term_months`   Integer     Loan term in months
  `Default_Status`     Category    Sample default outcome: `Yes` or `No`

## 🧰 Tools & Libraries

-   **Python** --- programming language
-   **Pandas** --- data loading and analysis
-   **NumPy** --- numerical calculations and vector operations
-   **Matplotlib** --- charts and plots
-   **Seaborn** --- statistical visualization toolkit
-   **SciPy** --- probability distributions and Q-Q plot calculations
-   **Jupyter Notebook** --- interactive coding environment

## ⚙️ Installation

Install the required packages in your terminal or notebook environment:

``` bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

## 🚀 Getting Started

### 1. Keep the files together

Place these files in the same project folder:

``` text
Loan-Applications-Analysis/
├── loan_applications_5000_records.csv
├── loan_applications_analysis.ipynb
└── README.md
```

The notebook filename above is a suggested name; use your actual
notebook filename if it differs.

### 2. Open Jupyter Notebook

``` bash
jupyter notebook
```

### 3. Import libraries and load the data

Run this in the first notebook cell:

``` python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy import stats

df = pd.read_csv("loan_applications_5000_records.csv")

print("Dataset shape:", df.shape)
print(df.head())
print(df.info())
```

Expected dataset shape:

``` text
(5000, 7)
```

If you get `FileNotFoundError`, check that the CSV is in the notebook's
working folder or provide the correct file path.

## 🧪 Practical Tasks

### Step 1 --- Central Tendency & Dispersion

**Tasks** - Find the mean, median, and mode of `Income`. - Calculate the
range, variance, and standard deviation of `Loan_Amount`.

**Methods** - `df["Income"].mean()` - `df["Income"].median()` -
`df["Income"].mode()` -
`df["Loan_Amount"].max() - df["Loan_Amount"].min()` -
`df["Loan_Amount"].var()` - `df["Loan_Amount"].std()`

### Step 2 --- Probability & Events

**Tasks** - Calculate the proportion of applications marked `Yes` for
default. - Create a contingency table of credit-score ranges and default
status. - Calculate `P(Default | Credit_Score < 600)`.

**Interpretation** Conditional probability is the share of defaults
among only those records whose credit score is below 600. It is not the
default probability for all customers.

### Step 3 --- Distributions & Visualization

**Tasks** - Plot a histogram of `Credit_Score` with a Gaussian reference
curve. - Calculate the skewness and kurtosis of `Loan_Amount`. - Draw a
Q-Q plot for `Income`.

**Interpretation** - A histogram shows the shape and spread of values. -
Skewness describes distribution asymmetry. - Pandas' `.kurt()` reports
excess kurtosis. - A Q-Q plot compares sample quantiles with theoretical
normal-distribution quantiles.

### Step 4 --- Linear Algebra Application

Use the first five rows of `[Income, Loan_Amount]` as two-dimensional
vectors.

**Tasks** - Calculate the dot product between the first and second
customer vectors. - Calculate the L2 norm of the first customer's
vector. - Calculate the angle between the first and second customer
vectors in radians and degrees.

**Key functions** - `np.dot(vector_1, vector_2)` -
`np.linalg.norm(vector_1, ord=2)` - `np.arccos(...)` and
`np.degrees(...)`

## 📊 Expected Deliverables

By completing the notebook, you should have:

-   Descriptive-statistics results printed in the notebook.
-   A default-probability estimate and a credit-score contingency table.
-   A Credit Score histogram with a Gaussian reference curve.
-   Skewness and kurtosis values for Loan Amount.
-   An Income Q-Q plot.
-   Dot product, L2 norm, and vector-angle calculations.

Numerical results depend on the provided CSV file. Do not copy example
values from another dataset as if they were calculated from this one.

## ▶️ Suggested Project Workflow

1.  Load and inspect the CSV.
2.  Check column names and data types.
3.  Calculate descriptive statistics.
4.  Calculate probabilities and build the contingency table.
5.  Generate and inspect the plots.
6.  Perform the vector calculations.
7.  Add short interpretations below the outputs.
8.  Save the notebook with the executed results.

## ⚠️ Limitations & Responsible Use

-   The dataset is synthetic and intended for learning only.
-   Results describe this sample and should not be treated as real-world
    banking statistics.
-   A Gaussian curve is a comparison reference; it does not prove that
    credit scores follow a normal distribution.
-   Statistical association does not prove causation.
-   Credit decisions require validated data, appropriate governance,
    fairness checks, and domain expertise.

## 👨‍💻 Author

**Rami Ashutosh**

Project topic: Loan Applications Statistical Analysis\
Purpose: Educational practical assignment in Python and statistics

------------------------------------------------------------------------

::: {align="center"}
**Thank you for viewing this project!**
:::
