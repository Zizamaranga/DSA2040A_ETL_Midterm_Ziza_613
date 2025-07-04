﻿# DSA2040A_ETL_Midterm_Ziza_613
# ETL Midterm — Ziza Maranga (613)

##  Project Overview
This project is an ETL (Extract → Transform → Load) pipeline that:
- **Extracts** raw and incremental datasets
- **Transforms** the data to clean, enrich, and structure it
- **Loads** the cleaned data into both SQLite and Parquet formats for querying

---

## ETL Phases
- **etl_extract.ipynb**  
  - Loads and previews `raw_data.csv` and `incremental_data.csv`
  - Displays `.head()` and `.info()` to inspect data types, missing values
  - Observes anomalies and saves raw copies to `data/`

- **etl_transform.ipynb**  
  - Cleans missing values and drops duplicates
  - Creates new column `total_price = quantity * unit_price`
  - Converts dates into proper datetime types and extracts `year`, `month`
  - Filters out irrelevant columns
  - Saves cleaned files to `transformed/transformed_full.csv` and `transformed_incremental.csv`

- **etl_load.ipynb**  
  - Writes Parquet files (`full_data.parquet`, `incremental_data.parquet`)
  - Uses `pd.read_parquet()` to preview loaded data

---

## Tools Used
- **Python 3.x**
- **Pandas** for data manipulation
- **PyArrow** for Parquet file support
- **Jupyter Notebook** for pipeline implementation
- **Git/GitHub** for version control and hosting

---

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/DSA2040A_ETL_Midterm_Ziza_613.git
