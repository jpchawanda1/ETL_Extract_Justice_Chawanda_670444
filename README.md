
# ETL Extract Lab

**Student Name:** Justice Chawanda  
**Student ID:** 670444

---

## Table of Contents

- [Project Overview](#project-overview)
- [Files Included](#files-included)
- [Tools Used](#tools-used)
- [Workflow & ETL Steps](#workflow--etl-steps)
- [Lab 5 – Load](#lab-5--load)
- [Key Features](#key-features)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)
- [Screenshots](#screenshots)
- [License](#license)

---

## Project Overview

This repository demonstrates **Full Extraction** and **Incremental Extraction** concepts in ETL (Extract, Transform, Load) processes using Python and pandas. Implemented as a Jupyter Notebook, it manages interactive data entry, transformation, and saving of both full and incremental datasets.

---

## Files Included

```
├── etl_extract.ipynb         # Jupyter notebook with extraction and transformation logic
├── Immigration_Data.csv      # The dataset of immigration records
├── last_extraction.txt       # Stores the last extraction timestamp for incremental extraction
├── .gitignore                # Excludes unnecessary files from version control
├── README.md                 # Project documentation (this file)
```

---

## Tools Used

- **Python 3**
- **pandas**
- **Jupyter Notebook**
- **tabulate** (for table display)
- **sqlite3** (for optional database output)
- **pyarrow** or **fastparquet** (for Parquet output, optional)

---

## Workflow & ETL Steps

### 1. Load the Dataset
- Loads `Immigration_Data.csv`.
- If empty, notes this in `last_extraction.txt`.

### 2. Display Last Recorded Timestamp
- Writes the last record’s timestamp to `last_extraction.txt`.

### 3. Add a New Record
- Prompts the user for new immigration record data.
- Automatically adds the current timestamp and updates the dataset.

### 4. Transform Full Data
- **Enrichment:** Calculates `age` from `date_of_birth`.
- **Structural:** Standardizes `timestamp` to `%Y-%m-%d %H:%M:%S`.
- **Categorization:** Groups `country` into regions (Africa, Europe, Asia, North America, South America, Oceania, Other).
- Saves the result as `transformed_full.csv`.

### 5. Transform Incremental Data
- Applies the above transformations only to the newest record(s).
- Saves as `transformed_incremental.csv`.

### 6. Display Results
- Shows the first 10 rows of both full and incremental transformed datasets.

---

## Lab 5 – Load

This section summarizes the **Load** phase of the ETL process as implemented in this project.

**Loading Method Used:**  
- Data is loaded from pandas DataFrames into persistent storage after transformation.
- The project supports CSV output by default, and includes sample code for saving to SQLite databases and Parquet files.

**Sample Code:**
```python
# Save to CSV (default)
df_transformed.to_csv('transformed_full.csv', index=False)

# Save to SQLite database (optional)
import sqlite3
conn = sqlite3.connect('etl_output.db')
df_transformed.to_sql('immigration_data', conn, if_exists='replace', index=False)
conn.close()

# Save to Parquet (optional)
df_transformed.to_parquet('transformed_full.parquet', index=False)
```

**Output Locations:**
- `transformed_full.csv` and `transformed_incremental.csv` (CSV files, always produced)
- `etl_output.db` (SQLite database, optional)
- `transformed_full.parquet` (Parquet file, optional)

*Note: To enable SQLite or Parquet output, uncomment or add the relevant code snippets in the notebook.*

---

## Key Features

- Consistent data enrichment and formatting.
- Supports both full and incremental ETL.
- Interactive record management.
- Outputs for both the full and latest incremental datasets.
- Handles empty datasets gracefully.

---

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/jpchawanda1/ETL_Extract_Justice_Chawanda_670444.git
cd ETL_Extract_Justice_Chawanda_670444
```

### 2. Install Requirements

Install Jupyter and pandas if needed:

```bash
pip install pandas jupyter
```
For optional database and Parquet output:
```bash
pip install pyarrow sqlite3
# or, for Parquet with fastparquet
pip install fastparquet
```

### 3. Run the Notebook

```bash
jupyter notebook etl_extract.ipynb
```

### 4. Dataset

- The file `Immigration_Data.csv` is included and contains 100 example records.
- You may replace it with your own data as long as it meets the minimum requirements.

---

## Future Improvements

- Add validation for user inputs to ensure data integrity.
- Implement logging to track changes to the dataset.
- Enable deletion or updating of existing records.

---

## Screenshots


---

## License

This project is for educational purposes only.

---
