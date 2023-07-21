# Data Splitting Project

## Introduction

This project is a Python script designed to split a CSV file containing data into three parts: JSON, a database, and CSV. The script provides flexibility to customize the distribution percentages for each destination. The primary goal of this script is to help users efficiently split large datasets into various formats for different purposes.

## Features

- Randomly shuffles the data for even distribution among the output files.
- Supports custom distribution percentages for JSON, database, and CSV.
- Saves the data into a JSON file, a CSV file, and a specified database table.
- Displays statistics after data insertion, such as the number of rows in each output file and the percentage of data retained.

## Requirements

- Python 3.x
- pandas
- numpy
- sqlalchemy

## How to Use

1. Ensure you have Python 3.x installed.
2. Install the required libraries by running the following command:
pip install pandas numpy sqlalchemy

3. Prepare your CSV file and place it in the same directory as the Python script.

4. Update the script variables according to your configuration:
- `csv_file_path`: The filename of the CSV file to be split.
- `json_file_path`: The filename for the JSON output file.
- `db_server`: The server name or address of your SQL Server.
- `db_name`: The name of the database where the table will be created.
- `db_driver`: The ODBC driver for the SQL Server.
- `db_table`: The name of the table in the database.
- `trusted_connection`: Set to "yes" if using trusted connection; otherwise, set to "no".
- `distribution`: A tuple representing the distribution percentages for JSON, database, and CSV, respectively.
- `header`: Set to `True` if the CSV file has a header; otherwise, set to `False`.

5. Run the Python script:
python script_name.py


## Example

Suppose you have a large CSV file named `cleaned_repositoriesV2.csv` that contains data on repositories. You can use this script to split the data into JSON, CSV (without header), and insert a portion into a database table.

## Notes

- Make sure the CSV file has a header in the first row.
- Before running the script, ensure that your SQL Server is running and accessible from your Python environment.
