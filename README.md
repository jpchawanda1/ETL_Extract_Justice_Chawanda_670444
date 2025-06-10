# ETL_Extract_Justice_Chawanda_670444

# ETL Extract Lab

Student Name:   Justice Chawanda  
Student ID:     [670444]

---

## Project Overview

This repository demonstrates the concepts of **Full Extraction** and **Incremental Extraction** in ETL (Extract, Transform, Load) processes using Python and pandas. The project is implemented in a Jupyter Notebook and works with a realistic generated sample dataset called "Immigration_Data" with 100 rows and 8 columns.

---

## Files Included

```
├── etl_extract.ipynb         # Jupyter notebook with extraction logic and explanations
├── Immigration_Data.csv      # The sample dataset (initially has 100 records)
├── last_extraction.txt       # Stores the last extraction timestamp for incremental extraction
├── .gitignore                # Excludes unnecessary files from version control
├── README.md                 # Project documentation (this file)
```

---

## Tools Used

- **Python 3**
- **pandas**
- **Jupyter Notebook**

---

## What the Notebook Does

- **Section 1: Full Extraction**
  - Loads the entire dataset from `Immigration_Data.csv`
  - Displays basic statistics (row count, column count, data sample)
  - Prints a message like: “Extracted X rows fully.”

- **Section 2: Incremental Extraction**
  - Reads the last extraction timestamp from `last_extraction.txt`
  - Extracts only the new or updated records since the last extraction
  - Prints a message like: “Extracted Y rows incrementally since last check.”

- **Section 3: Save New Timestamp**
  - Updates `last_extraction.txt` with the latest extraction timestamp

---

## How to Reproduce

### 1. Clone the Repository

```bash
git clone https://github.com/jpchawanda1/ETL_Extract_JPChawanda_<YourStudentID>.git
cd ETL_Extract_JPChawanda_<YourStudentID>
```

### 2. Install Requirements

This project uses standard Python libraries. If you need to install Jupyter and pandas:

```bash
pip install pandas jupyter
```

### 3. Run the Notebook

```bash
jupyter notebook etl_extract.ipynb
```

### 4. Dataset

- The file `Immigration_Data.csv` is provided and initially contains 100 records of realistic immigration data.
- You can replace this file with your own dataset if you wish, as long as it meets the minimum requirements.

---

## License

This project is for educational purposes only.
