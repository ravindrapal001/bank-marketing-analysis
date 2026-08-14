# 🏦 Bank Marketing Analysis

> Exploratory Data Analysis of a bank marketing campaign using Python.

## 📌 Project Overview

This project analyzes a bank marketing campaign dataset to understand customer characteristics and factors related to term-deposit subscriptions.

The analysis focuses on data quality, customer and campaign patterns, target-variable behavior, and relationships between numerical variables.

## 🎯 Business Objective

The objective is to identify useful patterns in customer and campaign data that can help understand marketing campaign outcomes.

**Key Question:**

> What customer and campaign characteristics are associated with term-deposit subscription?

## 📊 Dataset

- **Rows:** 41,188
- **Columns:** 21
- **Target:** `y`
- **Missing Values:** 0
- **Duplicate Rows:** 12

The target variable `y` indicates whether a customer subscribed to a term deposit.

| Target | Meaning | Count |
|---|---|---:|
| `yes` | Subscribed | 4,640 |
| `no` | Not subscribed | 36,548 |

The target variable is highly imbalanced, with significantly more customers who did not subscribe.

## 🔍 Analysis Performed

### 1. Data Inspection
- Examined dataset structure and dimensions
- Checked data types
- Reviewed missing values
- Generated summary statistics

### 2. Data Cleaning
- Identified duplicate records
- Performed data-quality checks
- Prepared the dataset for further analysis

### 3. Target Variable Analysis
- Analyzed subscription distribution
- Identified target-class imbalance
- Visualized subscription outcomes

### 4. Correlation Analysis
- Identified numerical variables
- Calculated the correlation matrix
- Identified strong positive and negative relationships
- Created a correlation heatmap

## 🛠️ Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- GitHub

## 📁 Project Structure

```text
bank-marketing-analysis/
│
├── data/
│   └── bankmarketing.csv
│
├── Day_01_Data_Inspection.ipynb
├── Day_02_Data_Cleaning.ipynb
├── Day_03_Target_Variable_Analysis.ipynb
├── Day_04_Numerical_Correlation_Analysis.ipynb
│
├── LICENSE
└── README.md

## 📚 Project Status

**Status: Completed**

This project covers the exploratory data analysis workflow from data inspection and cleaning through target-variable and numerical correlation analysis.

---

### 👤 Author

**Ravindra Pal**

M.Sc. Mathematics — IIT Hyderabad

Aspiring Data Analyst
