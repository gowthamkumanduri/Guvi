# Server Log Data Extraction and User History Database Update

## **Project Description**
This project is designed to extract email addresses and corresponding dates from a server log file, clean and transform the data, and store it in both MongoDB and SQLite databases. The stored data is ready for further analysis and historical tracking.

---

## **Features**
1. Extract email addresses and their associated dates from a server log file using regex.
2. Transform dates into a standardized format (YYYY-MM-DD HH:MM:SS).
3. Save the cleaned data to MongoDB.
4. Upload the data from MongoDB into an SQLite database.

---

## **Technologies Used**
- **Programming Language**: Python
- **Databases**: MongoDB, SQLite
- **Libraries**:
  - 're' for regex operations.
  - 'pymongo' for MongoDB interactions.
  - 'sqlite3' for SQLite operations.
  - 'datetime' for date transformations.

---

## **Setup and Usage**

### **Prerequisites**
1. Python 3.x installed on your system.
2. MongoDB installed and running locally or accessible remotely.
3. Install required Python libraries:
   '''bash
   pip install pymongo
   '''

---

### **Steps to Run the Script**

1. **Prepare the Log File**:
   - Ensure the log file containing email addresses and dates is available.
   - Default file name: 'mbox.txt'. Replace this name in the script if your file is named differently.

2. **Run the Script**:
   - Save the script in a Python file, e.g., 'Server_log_data_ETL_pipeline.py'.
   - Execute the script:
     '''bash
     python Server_log_data_ETL_pipeline.py
     '''

3. **Output**:
   - Extracted and transformed data is saved into:
     - MongoDB in a database named 'server_logs' and a collection named 'user_history'.
     - SQLite database file named 'user_history.db' in a table named 'user_history'.

---

## **File Descriptions**

### **Script File**
- **'Server_log_data_ETL_pipeline.py'**: Contains the main logic for data extraction, transformation, and database operations.

### **Generated Files**
- **'user_history.db'**: SQLite database file containing the processed data.

---

## **Functions in the Script**

### **Task 1: Extract Emails and Dates**
- **Function**: 'extract_emails_and_dates(log_file_path)'
- **Description**: Extracts email addresses and dates from the log file using regex.

### **Task 2: Data Transformation**
- **Function**: 'transform_data(data)'
- **Description**: Converts extracted dates into a standardized format.

### **Task 3: Save Data to MongoDB**
- **Function**: 'save_to_mongodb(data, mongo_uri, db_name, collection_name)'
- **Description**: Saves the cleaned data into MongoDB.

### **Task 4: Save Data to SQLite**
- **Function**: 'save_to_sqlite(mongo_uri, db_name, collection_name, sqlite_db_path)'
- **Description**: Fetches data from MongoDB and saves it into an SQLite database.

---

## **Error Handling**
- Ensure the log file exists at the specified path.
- Ensure MongoDB is running before executing the script.

---

## **Contact**
For any issues or further assistance, please reach out at k.gowthamraghava@gmail.com.
