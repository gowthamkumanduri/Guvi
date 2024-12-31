# Guvi
Guvi - Mini project assesment

**ETL Pipeline for Data Processing**

**Overview**

This project is an ETL (Extract, Transform, Load) pipeline implemented in Python. The pipeline processes data files from various formats, applies transformations, and saves the output to a CSV file. Logging is enabled to track the pipeline's operations.

**Features**

Extract: 

Reads data from CSV, JSON, and XML file formats.

Transform:

Converts heights from inches to meters.

Converts weights from pounds to kilograms.

Load:

Writes the transformed data to a CSV file.

Logging:

Logs all operations, including timestamps and performance metrics, to a log_file.txt file.

###Duplicate Removal: Removes duplicate records during the extraction phase.###

**Project Structure**

project/
├── ETL_using_python.ipynb      # Main ETL script
├── log_file.txt                # Log file (auto-generated during execution)
├── source/                     # Folder containing input data files
├── transformed_data.csv             # Output CSV file (auto-generated)

**Prerequisites**

Python 3.12.7

Install the required Python libraries:

pip install pandas

**How to Run**

Prepare Input Data: Place your data files (CSV, JSON, or XML) in the source directory.

Run the Script:

python ETL_using_python.ipynb

View Output: The transformed data will be saved in transformed_data.csv. Logs will be stored in log_file.txt.

**Configuration**

Input Folder: Update the folder_path in the script to point to your data folder.

Output File: Update the output_file variable to specify the desired output file location.

**Example Usage**

Here’s an example configuration in the script:

if __name__ == "__main__":
    etl_pipeline(
        folder_path="C:/path/to/source",  # Path to input folder
        output_file="C:/path/to/output_data.csv"  # Path to output file
    )

**Logging**

All operations are logged in log_file.txt.

Example log entry:

2024-12-31 15:46:37,530 - INFO - Starting ETL pipeline
2024-12-31 15:46:37,574 - INFO - Data successfully loaded into C:/Users/91798/Desktop/ME36/source/transformed_data.csv in 0:00:00.002515
2024-12-31 15:46:37,574 - INFO - ETL pipeline completed successfully


**Code Highlights**

###Removing Duplicates

Duplicates are removed using the drop_duplicates method from pandas:

combined_data = pd.DataFrame(combined_data).drop_duplicates().to_dict(orient='records')###


**Transformations**

Heights are converted to meters:

transformed_record[key] = float(value) * 0.0254  # Convert inches to meters

Weights are converted to kilograms:

transformed_record[key] = float(value) * 0.453592  # Convert pounds to kilograms

**Author**

[Gowtham Raghava K]

