

# Extraction, Transformation, Loading Labs 3,4,5

**Justice Chawanda - 670444**

## Workflow & ETL Steps (Etraction) LAB 3

1. **Load the Dataset:** Reads `Raw_Data/Immigration_Data.csv`.
2. **Display Last Recorded Timestamp:** Updates `last_extraction.txt` with the latest timestamp.
3. **Add a New Record:** Prompts for new record data, adds timestamp, and updates the dataset.
4. **Display Results:** Shows the first rows of both full and incremental datasets.

---

### Load Phase

This section summarizes the **Load** phase of the ETL process as implemented in this project.

**Loading Method Used:**
- Data is loaded from pandas DataFrames into persistent storage after transformation.
- The project supports CSV output by default, and includes code for saving to SQLite databases (in `Loaded_Data/`) and Parquet files.

**Sample Code:**
```python
# Save to CSV (default)
git clone https://github.com/jpchawanda1/ETL_Extract_Justice_Chawanda_670444.git
cd ETL_Extract_Justice_Chawanda_670444
```

### 2. Install Requirements

```bash
pip install pandas jupyter tabulate
# For SQLite and Parquet support:
pip install pyarrow fastparquet
```

### 3. Run the Notebook

```bash
jupyter notebook etl_extract.ipynb
# For the load phase:

---

## Key Features

- Consistent data enrichment and formatting
- Supports both full and incremental ETL
- Interactive record management
- Outputs for both the full and latest incremental datasets
- Handles empty datasets gracefully

---

## Future Improvements

- Add validation for user inputs to ensure data integrity
- Implement logging to track changes to the dataset
- Enable deletion or updating of existing records

---

## License

This project is for educational purposes only.
jupyter notebook elt_load.ipynb
```

### 4. Data Source

- The file `Raw_Data/Immigration_Data.csv` is included and contains example records.
- You may replace it with your own data as long as it meets the minimum requirements (see notebook for columns).

---

### Tools Used

- **Python 3**
- **pandas**
- **Jupyter Notebook**
- **tabulate** (for table display)
- **sqlite3** (for optional database output)
- **pyarrow** or **fastparquet** (for Parquet output, optional)

---

## Workflow & ETL Steps (Transformation) LAB 4

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

## Workflow & ETL Steps (Load) LAB 5

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
- `Tranformed/Tranformed_Full.csv` and `Tranformed/Transformed_Incremental.csv` (CSV files, always produced)
- `Loaded_Data/full_transformed.db` and `Loaded_Data/incremental_transformed.db` (SQLite databases, recommended)
- `Tranformed/Tranformed_Full.csv` and `Tranformed/Transformed_Incremental.csv` (CSV files, always produced)

---

### Key Features

- Consistent data enrichment and formatting.
- Supports both full and incremental ETL.
- Interactive record management.
- Outputs for both the full and latest incremental datasets.
- Handles empty datasets gracefully.

---

### How to Run

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

### Future Improvements

- Add validation for user inputs to ensure data integrity.
- Implement logging to track changes to the dataset.
- Enable deletion or updating of existing records.

---

### Screenshots


---

## License

This project is for educational purposes only.

---
