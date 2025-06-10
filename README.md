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

This workflow is designed to manage and update a dataset of immigration records. It includes functionality to:

- Display the timestamp of the last recorded entry.
- Allow the user to add a new record interactively.
- Update a text file (last_extraction.txt) with the timestamp of the last record.

**Steps**
1. Load the Dataset
- The dataset is loaded from a CSV file located at K:\Code Projects\ETL_Extract_Justice_Chawanda_670444\Immigration_Data.csv.
- If the dataset is empty, a message is written to the last_extraction.txt file indicating that the dataset is empty.

3. Display the Last Recorded Timestamp
- If the dataset is not empty, the timestamp of the last record is retrieved and written to the last_extraction.txt file.
- This ensures that the file always reflects the most recent update.

5. Add a New Record
- The user is prompted to decide whether they want to add a new record.
- If the user chooses "yes":
    *The user is asked to input details for the new record, including:
          -Immigrant ID
          -Passport Number
          -Name
          -Country
          -Purpose of Visit
          -Contact
          -Payment Status
- The current timestamp is automatically added to the record.
- The new record is appended to the dataset.
- The updated dataset is saved back to the CSV file.
- The last_extraction.txt file is updated with the timestamp of the newly added record.

- If the user chooses "no":
    *A message "No new record added." is displayed.


**Files Used**
1. Immigration_Data.csv
- Stores the dataset of immigration records.
- Updated whenever a new record is added.
  
2. last_extraction.txt
- Stores the timestamp of the last recorded entry.
- Updated every time the workflow is executed, regardless of whether a new record is added.


**Key Features**
- Ensures the dataset and last_extraction.txt file are always in sync.
- Provides an interactive way to manage records.
- Handles empty datasets gracefully.
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
