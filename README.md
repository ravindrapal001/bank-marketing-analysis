# Bank Marketing Analysis

Exploratory and Predictive Analysis of a Bank Marketing Campaign using Python

## Project Overview

This project analyzes a bank marketing campaign dataset to understand
customer characteristics and campaign-related factors associated with
term-deposit subscription.

The analysis covers data inspection, data-quality assessment, target-variable
analysis, customer demographics, campaign characteristics, numerical
correlations, and logistic regression modeling.

## Business Objective

The objective is to identify customer and campaign characteristics associated
with term-deposit subscription and use these findings to better understand
marketing campaign outcomes.

### Key Business Question

> What customer and campaign characteristics are associated with
> term-deposit subscription?

## Dataset

The dataset contains 41,188 customer records and 21 variables.

| Attribute | Value |
|---|---:|
| Rows | 41,188 |
| Columns | 21 |
| Target Variable | y |
| Missing Values | 0 |
| Duplicate Rows | 12 |

The target variable `y` indicates whether the customer subscribed to a
term deposit.

| Target | Meaning | Count |
|---|---|---:|
| yes | Subscribed | 4,640 |
| no | Not subscribed | 36,548 |

The target distribution is highly imbalanced, with approximately 11.27%
of observations representing successful subscriptions.

## Analysis Workflow

### 1. Data Inspection

- Examined dataset dimensions and structure
- Reviewed column names and data types
- Checked missing values
- Examined duplicate records
- Generated descriptive statistics
- Investigated categorical and numerical variables

### 2. Data Cleaning and Quality Assessment

- Identified duplicate records
- Reviewed unknown categorical values
- Investigated special values such as `pdays = 999`
- Checked numerical ranges and suspicious observations
- Prepared the data for subsequent analysis

### 3. Target Variable Analysis

- Examined subscription counts
- Calculated overall subscription rate
- Visualized target-class distribution
- Identified class imbalance

### 4. Customer Demographics Analysis

Analyzed customer characteristics including:

- Age
- Age groups
- Job
- Subscription rate by age group
- Subscription rate by job category

The analysis showed differences in subscription rates across customer
segments. For example, students and retired customers showed higher
observed subscription rates than several other job groups.

### 5. Campaign Analysis

The project examined:

- Contact method
- Campaign contact frequency
- Call duration
- Subscription outcomes

Customers contacted through cellular communication had an observed
subscription rate of approximately 14.74%, compared with approximately
5.23% for telephone contacts.

This represents an observed association and should not be interpreted as
causal evidence that the contact method itself caused the higher
subscription rate.

### 6. Numerical Correlation Analysis

A correlation matrix and heatmap were created to examine relationships
among numerical variables.

Strong relationships were observed among several economic indicators,
including:

- `emp.var.rate` and `euribor3m`
- `emp.var.rate` and `nr.employed`
- `euribor3m` and `nr.employed`

These relationships indicate substantial multicollinearity among some
economic variables.

### 7. Predictive Modeling

A Logistic Regression model was developed to classify whether a customer
subscribed to a term deposit.

The preprocessing pipeline included:

- Standardization of numerical variables
- One-hot encoding of categorical variables
- Train-test split with stratification
- Logistic Regression classification
- Probability prediction
- Feature coefficient analysis

## Model Performance

The model achieved the following results on the test set:

| Metric | Score |
|---|---:|
| Accuracy | 91.62% |
| Precision | 70.95% |
| Recall | 43.43% |
| F1 Score | 53.88% |
| ROC-AUC | 0.9425 |

The confusion matrix was:

| | Predicted No | Predicted Yes |
|---|---:|---:|
| Actual No | 7,145 | 165 |
| Actual Yes | 525 | 403 |

Accuracy should not be considered alone because the target variable is
imbalanced. Precision, recall, F1-score, and ROC-AUC provide additional
information about model performance.

## Important Model Findings

The Logistic Regression coefficients indicated that several variables
were strongly associated with the predicted subscription outcome.

Important features included:

- `emp.var.rate`
- `month_mar`
- `duration`
- `cons.price.idx`
- `poutcome_success`
- `month_aug`
- `euribor3m`
- `contact_telephone`

Categorical coefficients represent effects relative to their reference
categories, while standardized numerical variables represent the effect
of approximately one standard deviation of change.

## Key Insights

1. Term-deposit subscription is relatively uncommon in the dataset,
   representing approximately 11.27% of observations.

2. Subscription rates vary substantially across customer job categories
   and age groups.

3. Cellular contacts show a higher observed subscription rate than
   telephone contacts.

4. Customers who subscribed generally had longer call durations and
   fewer campaign contacts on average than customers who did not
   subscribe.

5. Several economic variables are strongly correlated, which can make
   individual regression coefficients less stable.

6. Logistic Regression provides useful predictive information about
   subscription outcomes.

## Important Limitations

### Target Imbalance

The dataset contains substantially more non-subscribers than subscribers.
Therefore, accuracy alone is not sufficient for evaluating model quality.

### Information Leakage Consideration

`duration` is highly predictive, but call duration is known during or after
the interaction. Therefore, it may not be appropriate for a real-world
pre-contact customer targeting model.

### Correlated Economic Variables

Several macroeconomic variables are strongly correlated. This may affect
the stability and interpretation of individual Logistic Regression
coefficients.

### Balance Analysis

The original analysis scope references balance/deposit trends, but the
provided dataset does not contain a `balance` column. Therefore, a
balance-based subscription relationship cannot be verified from this
dataset.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- GitHub

## Project Structure

```text
bank-marketing-analysis/
|
+-- data/
|   +-- bank_marketing.csv
|
+-- notebooks/
|   +-- 01_data_inspection_and_cleaning.ipynb
|   +-- 02_target_and_customer_analysis.ipynb
|   +-- 03_campaign_and_correlation_analysis.ipynb
|   +-- 04_logistic_regression.ipynb
|
+-- outputs/
|   +-- figures/
|   +-- tables/
|
+-- README.md
+-- requirements.txt
+-- LICENSE
+-- .gitignore


### 👤 Author

**Ravindra Pal**

M.Sc. Mathematics — IIT Hyderabad

Aspiring Data Analyst
