# Workflow Explanation

## Overview
This workflow is designed to manage and update a dataset of immigration records. It includes functionality to:
1. Display the timestamp of the last recorded entry.
2. Allow the user to add a new record interactively.
3. Update a text file (`last_extraction.txt`) with the timestamp of the last record.

## Steps

### 1. Load the Dataset
- The dataset is loaded from a CSV file located at `K:\Code Projects\ETL_Extract_Justice_Chawanda_670444\Immigration_Data.csv`.
- If the dataset is empty, a message is written to the `last_extraction.txt` file indicating that the dataset is empty.

### 2. Display the Last Recorded Timestamp
- If the dataset is not empty, the timestamp of the last record is retrieved and written to the `last_extraction.txt` file.
- This ensures that the file always reflects the most recent update.

### 3. Add a New Record
- The user is prompted to decide whether they want to add a new record.
- If the user chooses "yes":
  - The user is asked to input details for the new record, including:
    - Immigrant ID
    - Passport Number
    - Name
    - Country
    - Purpose of Visit
    - Contact
    - Payment Status
  - The current timestamp is automatically added to the record.
  - The new record is appended to the dataset.
  - The updated dataset is saved back to the CSV file.
  - The `last_extraction.txt` file is updated with the timestamp of the newly added record.
- If the user chooses "no":
  - A message "No new record added." is displayed.

## Files Used

### 1. `Immigration_Data.csv`
- Stores the dataset of immigration records.
- Updated whenever a new record is added.

### 2. `last_extraction.txt`
- Stores the timestamp of the last recorded entry.
- Updated every time the workflow is executed, regardless of whether a new record is added.

## Key Features
- Ensures the dataset and `last_extraction.txt` file are always in sync.
- Provides an interactive way to manage records.
- Handles empty datasets gracefully.

## Future Improvements
- Add validation for user inputs to ensure data integrity.
- Implement logging to track changes to the dataset.
- Provide an option to delete or update existing records.