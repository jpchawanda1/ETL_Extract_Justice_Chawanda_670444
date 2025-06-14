Here’s a clean, well-structured, and formatted README.md for your repository, following best practices and combining all key details from your content:

---

# ETL Extract Lab

**Student Name:** Justice Chawanda  
**Student ID:** 670444

---

## Project Overview

This repository demonstrates **Full Extraction** and **Incremental Extraction** concepts in ETL (Extract, Transform, Load) processes using Python and pandas. Implemented as a Jupyter Notebook, it manages a dataset of immigration records, enabling you to add, transform, and track records and their updates.

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

---

## Workflow & Features

- Display the timestamp of the last recorded entry.
- Add a new record interactively.
- Update `last_extraction.txt` with the timestamp of the last record.
- Transform the data (enrichment, formatting, categorization).
- Output both full and incremental transformed datasets.

### ETL Steps

1. **Load the Dataset**
    - Loads `Immigration_Data.csv`.
    - If empty, notes this in `last_extraction.txt`.

2. **Display Last Recorded Timestamp**
    - Writes the last record’s timestamp to `last_extraction.txt`.

3. **Add a New Record**
    - Prompts the user for new immigration record data.
    - Automatically adds the current timestamp and updates the dataset.

4. **Transform Full Data**
    - **Enrichment:** Calculates `age` from `date_of_birth`.
    - **Structural:** Standardizes `timestamp` to `%Y-%m-%d %H:%M:%S`.
    - **Categorization:** Groups `country` into regions (Africa, Europe, Asia, North America, South America, Oceania, Other).
    - Saves the result as `transformed_full.csv`.

5. **Transform Incremental Data**
    - Applies the above transformations only to the newest record(s).
    - Saves as `transformed_incremental.csv`.

6. **Display Results**
    - Shows the first 10 rows of both full and incremental transformed datasets.

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

![Screenshot 2025-06-10 222540](https://github.com/user-attachments/assets/03a06fcc-3a8a-4fec-92ad-80d064a540eb)  
![Screenshot 2025-06-10 222927](https://github.com/user-attachments/assets/8bc45cdd-5bea-4dd0-8b29-78058d13cb80)  
![Screenshot 2025-06-10 223049](https://github.com/user-attachments/assets/26a8462e-b6c2-4163-88a9-7a1f0038cb8e)

---

## License

This project is for educational purposes only.

---

Copy and paste this into your README.md file for a clean, professional, and organized repository overview! If you want any section customized or expanded, just let me know.Here’s a clean, well-structured, and formatted README.md for your repository, following best practices and combining all key details from your content:

---

# ETL Extract Lab

**Student Name:** Justice Chawanda  
**Student ID:** 670444

---

## Project Overview

This repository demonstrates **Full Extraction** and **Incremental Extraction** concepts in ETL (Extract, Transform, Load) processes using Python and pandas. Implemented as a Jupyter Notebook, it manages a dataset of immigration records, enabling you to add, transform, and track records and their updates.

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

---

## Workflow & Features

- Display the timestamp of the last recorded entry.
- Add a new record interactively.
- Update `last_extraction.txt` with the timestamp of the last record.
- Transform the data (enrichment, formatting, categorization).
- Output both full and incremental transformed datasets.

### ETL Steps

1. **Load the Dataset**
    - Loads `Immigration_Data.csv`.
    - If empty, notes this in `last_extraction.txt`.

2. **Display Last Recorded Timestamp**
    - Writes the last record’s timestamp to `last_extraction.txt`.

3. **Add a New Record**
    - Prompts the user for new immigration record data.
    - Automatically adds the current timestamp and updates the dataset.

4. **Transform Full Data**
    - **Enrichment:** Calculates `age` from `date_of_birth`.
    - **Structural:** Standardizes `timestamp` to `%Y-%m-%d %H:%M:%S`.
    - **Categorization:** Groups `country` into regions (Africa, Europe, Asia, North America, South America, Oceania, Other).
    - Saves the result as `transformed_full.csv`.

5. **Transform Incremental Data**
    - Applies the above transformations only to the newest record(s).
    - Saves as `transformed_incremental.csv`.

6. **Display Results**
    - Shows the first 10 rows of both full and incremental transformed datasets.

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

![Screenshot 2025-06-10 222540](https://github.com/user-attachments/assets/03a06fcc-3a8a-4fec-92ad-80d064a540eb)  
![Screenshot 2025-06-10 222927](https://github.com/user-attachments/assets/8bc45cdd-5bea-4dd0-8b29-78058d13cb80)  
![Screenshot 2025-06-10 223049](https://github.com/user-attachments/assets/26a8462e-b6c2-4163-88a9-7a1f0038cb8e)

---

## License

This project is for educational purposes only.

---

