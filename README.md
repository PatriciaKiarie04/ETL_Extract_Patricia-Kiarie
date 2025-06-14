# ETL_Extract_Patricia-Kiarie
School Attendance ETL Pipeline
This jupyter notebook implements a robust ETL (Extract, Transform, Load) pipeline for processing school attendance data with a focus on efficient incremental extraction. The system is designed to handle daily attendance records while minimizing redundant data processing.
## Key features:
 Incremental Data Loading – Processes only new records using timestamps
 Batch Processing – Extracts data in fixed chunks (default: 50 records per run)
 Automatic Setup – Generates sample data if none exists
 Progress Tracking – Uses last_extraction.txt to remember where it left off
 Error Handling – Gracefully manages missing files or corrupt data

## Tools used:
python (with pandasfor Data manipulation and analysis, datetime libraries for The datetime and timedelta libraries in Python are essential for handling dates, times, and time-based operations in ETL (Extract, Transform, Load) workflows.)

pandas - for data cleaning, enrichment and transformation

datetime - for timestamp comparison and date parsing

Jupyter notebook - Interactive development, testing and visualization

Vs code - Editing and debugging

## How to run the notebook
pip install pandas
git clone the repository
launch the jupyter notebook
run all the cells in order

## where the data comes from
The notebook generates synthetic data (school_attendance.csv)

Simulates 5 schools' daily attendance for 3 months excluding weekends

Realistic daily variations in enrollment/absences

**School Attendance ETL Pipeline Lab 4: Transform in ETL**  
This Jupyter notebook implements a robust ETL (Extract, Transform, Load) pipeline for processing school attendance data, with a focus on **incremental extraction**, **data transformation**, and **structured output**. It simulates daily attendance records for multiple schools and supports scalable, clean data workflows suitable for analysis or reporting.

## Features include:
**Incremental Data Loading**: Processes only *new* records using `last_updated` timestamps.
- **Batch Processing**: Extracts data in manageable chunks (default: 50 records per run).
- **Auto Data Generation**: Creates synthetic attendance data if the source file is missing.
- **Progress Tracking**: Uses `last_extraction.txt` to record the last extracted timestamp.
- **Error Handling**: Gracefully handles missing or malformed files.

## Project structure
├── school_attendance.csv # Raw generated data
├── transformed_full.csv # Transformed full dataset
├── transformed_incremental.csv # Transformed incremental dataset
├── latest_extracted_records.csv # Output from latest incremental run
├── last_extraction.txt # Tracks last processed timestamp
├── school_attendance_etl.py # Python ETL script
├── etl_extract.ipynb # Notebook with full ETL logic
└── README.md # Project documentation


### Transformations Performed

1. **Cleaning**
   - Removed duplicate records
   - Replaced missing values with default values (e.g., `0` for absent and present)

2. **Enrichment**
   - Calculated `Attendance_Rate`:
    Attendance_Rate = (Present / Enrolled) * 100


3. **Structural**
   - Standardized `Date` column to `YYYY-MM-DD` format using `pd.to_datetime`
   - Converted `School DBN` to uppercase for consistency
