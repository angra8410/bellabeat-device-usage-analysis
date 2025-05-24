# Data Cleaning & Manipulation Documentation

This document outlines the process and steps taken to clean, transform, and prepare the data for analysis in the Bellabeat smart device usage project.

---

## 1. Data Import & Database Creation

- **Source:**  
  The original data was provided as several Microsoft Excel (.xlsx) files, each containing different aspects of sma device usage.

- **Process:**  
  - A new SQL database named `bellabeat` was created.
  - All Excel files were imported into SQL, with each file forming a corresponding table in the database.
  - Table structures were reviewed for consistency and integrity.

---

## 2. Data Cleaning Steps

- **Handling Missing Values:**  
  - All tables were scanned for missing (NULL) values.
  - Rows with critical missing fields (e.g., user IDs, timestamps) were removed.
  - Non-critical missing values were imputed or left as-is, depending on relevance.

- **Removing Duplicates:**  
  - Duplicate rows were identified using primary key (or composite key) checks.
  - Duplicates were removed to ensure each record was unique.

- **Outlier Detection and Removal:**  
  - Extreme outliers in numeric fields (e.g., steps, calories) were identified using statistical summaries and boxplots.
  - Outliers deemed to be errors (e.g., implausible activity levels) were removed to prevent skewing analysis.

---

## 3. Data Transformation

- **Aggregation:**  
  - Where necessary, data was aggregated (e.g., hourly to daily totals) to facilitate seasonality and trend analyses.

- **Normalization/Standardization:**  
  - For user-level analyses, activity metrics were normalized as needed to enable fair comparisons.

- **Table Joins and Data Integration:**  
  - Relevant tables were joined on appropriate keys (e.g., user ID, date) to combine device usage, activity, and demographic information.

---

## 4. Stored Procedure Development

- Custom SQL stored procedures were developed (with AI assistance) to automate data summarization and segmentation:
  - `sp_Bellabeat_SeasonalityPatterns`
  - `sp_Bellabeat_Usage_Trends`
  - `sp_Bellabeat_UserActiveTimeOfDay`
  - `sp_Bellabeat_UserSegmentation`
- These procedures incorporated all necessary data cleaning logic to ensure reliable outputs.

---

## 5. Data Accuracy and Validation

- After cleaning, summary statistics were reviewed to confirm data integrity (e.g., no nulls in key fields, reasonable value ranges).
- Random samples of the cleaned data were checked against source files for accuracy.

---

**Summary:**  
The data cleaning and manipulation process ensured that the analysis was based on accurate, consistent, and relevant information, supporting trustworthy insights for Bellabeat’s business needs.
