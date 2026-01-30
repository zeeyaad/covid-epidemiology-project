# 🦠 COVID-19 Epidemiology Data Engineering & Analysis Project

A data engineering pipeline that cleans and processes global COVID-19 epidemiological data, engineers key public-health indicators, and produces an analysis-ready dataset for exploratory analysis of testing, recovery, and mortality trends.

---

## 📌 Objective

The objective of this project is to design and implement a structured **data engineering pipeline** that transforms raw COVID-19 epidemiological data into a **clean, reliable, and analysis-ready dataset**, and to derive meaningful health indicators for exploratory data analysis.

This project focuses on:
- Cleaning real-world noisy health data
- Engineering interpretable metrics (rates & ratios)
- Preparing datasets for analytical and visualization tasks

---

## 📂 Dataset Source

- **Source:** Global COVID-19 Epidemiology Dataset  
- **Format:** CSV  
- **Primary File:** `epidemiology.csv`

### Key Raw Columns
- `date`
- `location_key`
- `new_confirmed`
- `new_deceased`
- `new_recovered`
- `new_tested`
- `cumulative_confirmed`
- `cumulative_deceased`
- `cumulative_recovered`
- `cumulative_tested`

> ⚠️ The raw dataset contains missing values, reporting delays, and inconsistent daily updates, which are common in real-world epidemiological data.

---

## 🏗️ Data Pipeline Overview

The project follows a **three-stage data pipeline**:

### 1️⃣ Data Ingestion (Raw Layer)
- Load raw epidemiological data without modification
- Preserve original values
- Ensure correct data types, especially for dates and numeric fields

📁 File: `epidemiology.csv`

---

### 2️⃣ Data Cleaning & Preparation (Clean Layer)

Cleaning steps include:
- Handling missing values without blindly dropping rows
- Preserving time-series continuity
- Ensuring cumulative values remain logically consistent
- Removing invalid or negative computed values when detected

📁 File: `cleaned_covid_19.csv`

---

### 3️⃣ Feature Engineering & Enrichment (Analytics Layer)

The following analytical features were engineered:

- Percentage of Recovered per Day
- Percentage of Tested per Day
- Recovery Rate
- Case-to-Recovery Ratio
- Death-to-Confirmed Ratio

These indicators enable fair comparison across regions and improve interpretability beyond raw case counts. Missing values are preserved where calculations are not statistically valid.

---

## 📈 Analysis & Visualization

Exploratory analysis includes:
- Scatter plots examining testing rates versus recovery rates
- Time-series aware analysis using daily and cumulative metrics
- Identification of trends, outliers, and data gaps

The emphasis is on **data correctness and readiness**, not predictive modeling.

---

## ⚠️ Assumptions & Limitations

- Missing values represent unreported data, not data errors
- No data imputation was applied to avoid introducing artificial trends
- Analysis is exploratory and descriptive
- Country-level aggregation may require additional preprocessing

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook

---

## 📌 Project Structure

```

📦 covid-epidemiology-project
├── epidemiology.csv
├── cleaned_covid_19.csv
├── covid19_data_pipeline_and_analysis.ipynb
├── README.md

```

---

## 🎯 Intended Use

This project is suitable for:
- Data Engineering coursework
- Data Analyst portfolio projects
- ETL pipeline demonstrations
- Exploratory public-health data analysis

---

## 👤 Author

Zeyad Alaa  
Data Engineering / Data Analysis Student
