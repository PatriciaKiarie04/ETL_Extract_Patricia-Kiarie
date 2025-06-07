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

Jupyter notebook - Interactive development & testing

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