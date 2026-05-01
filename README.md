# 💰 SpendSense — Personal Expense Analysis & Budget Insights

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/Jupyter-Notebook-orange?style=for-the-badge&logo=jupyter&logoColor=white"/>
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge"/>
  <img src="https://img.shields.io/badge/ML-Scikit--learn%20%7C%20Prophet-blueviolet?style=for-the-badge"/>
</p>

<p align="center">
  A end-to-end data science project that analyses personal spending patterns, 
  forecasts future expenses using <strong>Prophet</strong>, and groups transactions 
  by behaviour using <strong>KMeans clustering</strong>.
</p>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Project Workflow](#-project-workflow)
- [Tech Stack](#-tech-stack)
- [Dataset](#-dataset)
- [Key Analyses](#-key-analyses)
- [Machine Learning](#-machine-learning)
- [Key Insights](#-key-insights)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Author](#-author)

---

## 🔍 Overview

**SpendSense** is a data-driven personal finance analysis tool built with Python. It processes daily transaction records to uncover spending patterns, identify high-expense categories, and predict future spending — helping individuals make smarter financial decisions.

---

## 🔄 Project Workflow

```
Data Loading → Data Cleaning → EDA → Visualization → ML Modelling → Forecasting → Insights
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| `Python 3.10+` | Core language |
| `Pandas` | Data loading, cleaning, aggregation |
| `NumPy` | Numerical operations |
| `Matplotlib & Seaborn` | Data visualization |
| `Scikit-learn` | Linear Regression, KMeans Clustering |
| `Prophet` | Time-series forecasting |
| `Jupyter Notebook` | Interactive development |

---

## 📂 Dataset

The dataset contains personal daily transaction records with the following fields:

| Column | Description |
|--------|-------------|
| `Date` | Transaction date |
| `Category` | Expense category (Food, Transport, etc.) |
| `Amount` | Transaction amount in INR |
| `Payment_Mode` | Payment method (UPI/Online, Cash, etc.) |
| `Description` | Short note on the transaction |

> The dataset is filtered to include **expense rows only** and missing descriptions are filled using the mode value.

---

## 📊 Key Analyses

### 1. Category-wise Expense Distribution (Pie Chart)
Shows the percentage share of each spending category — Food is the dominant category.
![Category Pie Chart](outputs/figures/category_pie_chart.png)

### 2. Monthly Spending Trend (Line Graph)
Tracks how total spending changes month-by-month to identify high-expense periods.

### 3. Category Comparison (Bar Chart)
Compares total spending across all categories side by side.

### 4. Payment Mode Analysis
Reveals that **UPI/Online** is the most used payment method, reflecting a digital-first spending habit.

### 5. Top 10 Highest Transactions
Lists the 10 largest individual expenses for quick anomaly spotting.

### 6. Average Expense per Category
Instead of totals, shows the average transaction size — useful to identify which categories have big one-off purchases.

### 7. Spending Heatmap (Category × Month)
A heatmap showing spending intensity per category per month. Darker = higher spending.

---

## 🤖 Machine Learning

### 📈 Linear Regression — Trend Detection
Fits a regression line on monthly totals to detect whether spending is trending up or down over time.

```
Metric        Value
──────────────────────
MAE           Rs X.XX
R² Score      X.XXXX
```

### 🔮 Prophet — 30-Day Forecasting
Facebook's open-source time-series model trained on daily transactions to forecast the next 30 days of spending, including trend and weekly seasonality components.

### 🔵 KMeans Clustering — Spending Behaviour Groups
Groups all transactions into 3 behavioural clusters:

| Cluster | Description |
|---------|-------------|
| 🟢 Low Spend | Small, routine purchases |
| 🟡 Medium Spend | Regular mid-size expenses |
| 🔴 High Spend | Large, infrequent transactions |

---

## 💡 Key Insights

- **Food** is the largest expense category, making up the majority of all spending
- **UPI/Online** is the dominant payment mode — strong shift to digital payments
- Monthly spending varies significantly — certain months show clear spikes
- The heatmap reveals **Transportation** is consistent while other categories spike seasonally
- Prophet captured the overall spending trend and weekly patterns in the 30-day forecast
- KMeans successfully separated transactions into Low, Medium, and High spend tiers

---

## 📁 Project Structure

```
SpendSense/
├── data/
│   └── expense_data_1.csv       # Raw transaction dataset
├── notebooks/
│   └── SpendSense_Code.ipynb    # Main analysis notebook
├── outputs/
│   └── figures/                 # Saved chart images
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

---

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/tyagirajat154/SpendSense.git
cd SpendSense
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch the notebook
```bash
jupyter notebook notebooks/SpendSense_Code.ipynb
```

> ⚠️ Make sure `expense_data_1.csv` is placed inside the `data/` folder before running.

---

## 👤 Author

**Rajat Tyagi**
B.Tech CSE — IILM University

[![GitHub](https://img.shields.io/badge/GitHub-tyagirajat154-181717?style=flat&logo=github)](https://github.com/tyagirajat154)

---

<p align="center">Made with ❤️ and Python</p>
