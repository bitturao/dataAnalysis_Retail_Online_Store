# Retail Sales Analytics Dashboard

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Project-Production%20Ready-brightgreen)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-blueviolet)
![Made With Data](https://img.shields.io/badge/Made%20With-Real%20Retail%20Data-red)

An end-to-end **retail sales analytics dashboard** built using **Python, Pandas, and Matplotlib**.  
This project performs **e-commerce data analysis**, **RFM customer segmentation**, and **churn detection** on real-world retail transaction data to deliver actionable business insights for data analysts, BI teams, and e-commerce managers.


## Project Overview

This project analyzes real-world e-commerce transaction data to uncover **customer behavior, revenue drivers, and retention risks**. Using the UCI Online Retail dataset (541K+ transactions), it delivers a production-style analytics workflow—from raw Excel ingestion to strategic insights.

## Why This Project Matters

This project demonstrates the ability to:
- Translate raw business data into strategic insights
- Build production-style analytics pipelines
- Apply customer segmentation used in real companies
- Communicate insights through executive-ready visualizations


### Business Value
- Identify **high-value and at-risk customers**
- Understand **monthly sales trends and seasonality**
- Optimize **inventory and product strategy**
- Enable **data-driven marketing decisions**

**Real-world use case**:  
E-commerce managers and BI teams can use this analysis to prioritize retention campaigns, focus on profitable regions/products, and build scalable analytics foundations.

## Key Innovation

Unlike traditional retail dashboards that drop incomplete records, this solution implements **intelligent missing data imputation**, filling null product descriptions using the most frequent description per `StockCode`. This preserves dataset completeness while maintaining accuracy.

Additionally, the automated **RFM + churn framework** delivers immediate customer segmentation and inactivity detection—transforming raw sales data into **ready-to-act insights** with minimal manual intervention.

## Features

- 🔍 **Complete Data Pipeline** – Ingests, cleans, and processes 541K+ retail transactions
- 📊 **RFM Customer Segmentation** – 5×5×5 scoring with composite customer ranking
- 🚨 **Customer Churn Detection** – Flags customers inactive for 90+ days
- 📈 **Sales Analytics** – Monthly revenue trends and top-performing countries/products
- 🧹 **Intelligent Data Cleaning** – Handles nulls, refunds, negative values, and outliers
- 🎨 **Executive-Ready Visuals** – Clear, labeled charts for presentations and reports
- ⚡ **Scalable & Efficient** – Optimized pandas operations for large Excel datasets

## Tech Stack

- **Python 3.12**
- **Pandas** – Data manipulation
- **Matplotlib** – Data visualization
- **NumPy** – Numerical operations
- **OpenPyXL** – Excel processing
- **Jupyter / Google Colab** – Interactive analysis

## Architecture / How It Works

```

Raw Excel Data
↓
Data Cleaning & Validation
↓
Feature Engineering
(TotalPrice, Month)
↓
RFM Segmentation
(Recency, Frequency, Monetary)
↓
Churn Detection
↓
Business Visualizations

````

### Processing Steps
1. **Data Ingestion** – Reads raw Excel data with dtype safety
2. **Smart Cleaning** – Imputes missing descriptions using StockCode frequency
3. **Feature Engineering** – Revenue calculation and temporal extraction
4. **RFM Analysis** – 125 customer segments with composite scoring
5. **Churn Analysis** – Identifies inactive customers (>90 days)
6. **Visualization Layer** – Revenue trends and contribution analysis

## Installation & Setup

```bash
# Clone repository
git clone <your-repo-url>
cd retail-analytics

# Install dependencies
pip install pandas matplotlib openpyxl
````

### Google Colab (Zero Setup)

Open `online_retail_store.ipynb` directly in Colab and run all cells.

## Usage

```text
Run all notebook cells sequentially.

Generated outputs:
- Monthly sales trend line chart
- Top 5 countries by revenue (+ % contribution)
- Top 5 products by revenue
- RFM segmentation table
- Customer churn distribution & inactive count
```

**Quick Start**

1. Open the notebook
2. Run all cells (Ctrl + F9)
3. Review insights and visualizations

## Configuration

No external configuration required. Core parameters can be easily adjusted:

```python
CHURN_THRESHOLD = 90      # Days of inactivity
QUANTILE_OUTLIERS = 0.99  # Remove top 1% extreme values
RFM_QUANTILES = 5         # 5x5x5 RFM segmentation
```

## Future Improvements

* Interactive dashboards (Streamlit / Plotly Dash)
* ML-based churn & CLV prediction models
* Real-time analytics (Kafka / Spark)
* REST APIs (FastAPI / Flask)
* Database-backed warehouse (PostgreSQL + dbt)
* Automated reporting (PDF / Email scheduling)

## Who This Project is For

* Data Analysts & BI Professionals
* E-commerce & Retail Managers
* Marketing & Retention Teams
* Data Science Students
* Portfolio Developers showcasing analytics pipelines


