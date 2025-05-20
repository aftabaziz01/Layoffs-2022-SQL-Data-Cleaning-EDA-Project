# 💼 Layoffs 2022 - SQL Data Cleaning & Exploratory Data Analysis

This project focuses on cleaning and exploring a real-world dataset of global tech company layoffs during 2020–2023, sourced from [Kaggle](https://www.kaggle.com/datasets/swaptr/layoffs-2022). It demonstrates advanced SQL techniques for data cleaning, transformation, and trend analysis.

---

## 🧠 Objectives

- Clean messy real-world data using SQL best practices
- Identify and handle duplicates, nulls, and inconsistent formats
- Perform exploratory analysis to identify trends in layoffs over time, by company, industry, and country

---

## 🛠️ Tools Used

- **SQL (MySQL)** – Core tool for data cleaning and EDA
- **Window Functions** (`ROW_NUMBER()`, `DENSE_RANK()`)
- **Common Table Expressions (CTEs)**
- **Date Functions** & **String Manipulation**

---

## 📊 Key Tasks & Techniques

### 🔹 Data Cleaning

- Created a staging table to preserve original data
- Removed **~150+ duplicate rows** using `ROW_NUMBER()` + `CTE`
- Standardized inconsistent entries (e.g., `"CryptoCurrency"` → `"Crypto"`)
- Cleaned up country names (`"United States."` → `"United States"`)
- Converted string-based dates to proper `DATE` format using `STR_TO_DATE()`
- Populated missing values in the `industry` column using **self-JOIN**

### 🔹 Exploratory Data Analysis

- Identified companies with **100% staff layoffs**
- Ranked companies with the most layoffs per year using `DENSE_RANK()`
- Aggregated layoffs by:
  - **Company**
  - **Country**
  - **Industry**
  - **Location**
  - **Startup funding stage**
- Generated a **rolling total of layoffs per month** using a window function

---

## 📈 Sample Insights

- Startups like **Quibi** and **BritishVolt** laid off their entire workforce after raising **hundreds of millions in funding**
- **2022** had the highest total layoffs compared to other years
- **Crypto** and **Retail** industries were among the most affected sectors
- Companies in the **United States** contributed to the majority of total layoffs

---

## 📂 Dataset Source

- 📍 [Kaggle - Layoffs 2022](https://www.kaggle.com/datasets/swaptr/layoffs-2022)

---

## 🔍 File Structure

```text
├── sql_cleaning_script.sql       # Full data cleaning script
├── sql_eda_queries.sql           # EDA queries for trend exploration
├── README.md                     # Project documentation (this file)

## 👨‍💻 Author

Created by [aftabaziz01](https://github.com/aftabaziz01)

---

## 🙋‍♂️ What I Learned

- Designing a **reliable SQL-based cleaning pipeline**
- Solving **real-world issues** like text inconsistency, nulls, and formatting
- Using **window functions and CTEs** to perform advanced EDA
