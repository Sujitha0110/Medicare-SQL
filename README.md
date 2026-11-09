# Medicare Hospital Management Analytics

## Overview
Medicare is a **SQL/MySQL healthcare analytics project** focused on hospital network operations, doctor and department workload, patient admissions, treatments, pharmacy and laboratory activity, insurance, and billing and payment collection. The project creates a relational database, inserts hospital records, performs data profiling and cleaning, and uses SQL queries to generate business-focused insights.

## Objectives
- Understand the hospital network by location, type, and bed capacity
- Analyze doctor strength, specialization mix, experience, and consultation fees
- Evaluate department and hospital workload through appointments and admissions
- Study admission types, admission status, and average length of stay
- Analyze room distribution, treatment activity, and laboratory test volume
- Identify medicine categories that generate the highest pharmacy sales
- Compare billed amounts with successful payments
- Identify data-quality issues and clean inconsistent patient, doctor, and employee information

## Technology Stack
- **Database:** MySQL
- **Language:** SQL
- **Data Source:** Records inserted through SQL `INSERT` statements

## Database
**Database:** `Medicare`

The project contains **15 tables** covering hospitals, departments, doctors, patients, rooms, appointments, admissions, treatments, insurance, medicines, pharmacy sales, laboratory tests, employees, billing, and payments.

## Dataset
| Area | Records |
|---|---:|
| Hospitals | 30 |
| Departments | 40 |
| Doctors | 450 |
| Patients | 2,000 |
| Rooms | 800 |
| Appointments | 5,100 |
| Admissions | 2,500 |
| Treatments | 3,500 |
| Insurance | 1,500 |
| Medicines | 300 |
| Pharmacy | 2,500 |
| Laboratory | 3,000 |
| Employees | 1,200 |
| Billing | 5,000 |
| Payments | 5,000 |

*Record counts are based on the `INSERT` statements in the supplied SQL script.*

## Key KPIs and Measures
- Total Hospitals
- Total Doctors
- Total Departments
- Doctors with More Than 10 Years of Experience
- Total Bed Capacity
- Highest Hospital Bed Capacity
- Doctor Consultation Fee: Average and Minimum
- Doctors per Specialization and per Hospital
- Appointments per Doctor and per Department
- Admissions by Hospital, Admission Type, and Admission Status
- Average Patient Length of Stay
- Room Distribution by Type
- Treatment and Laboratory Test Volume
- Pharmacy Sales by Medicine Category
- Total Billed Amount
- Billing Component Contribution (Room, Doctor, Medicine, Lab, Other)
- Total Payment Collected
- Collection Gap (Billed vs Collected)

## Project Workflow
```text
SQL Data and INSERT Statements
          ↓
MySQL Database Creation
          ↓
15 Relational Tables
          ↓
Data Profiling
          ↓
Data Cleaning
          ↓
SQL Practice and Business Analysis
          ↓
KPI Queries
          ↓
Business Insights and Recommendations
```

## Data Profiling and Cleaning
The SQL script checks for the following data-quality issues:

- Missing `head_doctor_id` values in the `Departments` table
- Inconsistent gender values in the `Doctors`, `Patients`, and `Employees` tables
- Missing `department_id` and email values in the `Doctors` table
- Doctor and patient emails that do not follow the expected email pattern
- Leading and trailing spaces in `Patients` first names
- Missing email values in the `Patients` table
- Missing `department_id` and `discharge_date` values in the `Admissions` table
- Missing `admission_id` values in the `Treatments` table
- Missing `insurance_provider` values in the `Insurance` table
- Missing `department_id` values in the `Employees` table
- Missing `admission_id` and `appointment_id` values in the `Billing` table

Cleaning operations included:
- Standardizing gender values to `Male` and `Female` in `Doctors`, `Patients`, and `Employees`
- Correcting doctor and patient emails that were missing the `@` symbol or the `.com` ending
- Trimming extra spaces from patient first names

## SQL Analysis
The project includes SQL practice queries and presentation-focused analysis using:
- Aggregate functions: `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`, `ROUND()`
- Grouping and filtering: `GROUP BY`, `HAVING`, `ORDER BY`, `LIMIT`, `DISTINCT`
- Joins: `INNER JOIN`, `LEFT JOIN`
- Subqueries
- Conditional logic: `CASE`
- String functions: `LTRIM()`, `TRIM()`, `LOWER()`, `REPLACE()`, `CONCAT()`, `LIKE`, `REGEXP`
- Window functions: `ROW_NUMBER()`, `RANK()`, `LAG()`, `LEAD()`

## Business Analysis
The analysis queries investigate:
- Hospital, doctor, and department counts across the network
- Specializations with the most doctors
- Hospitals with the most doctors and the highest bed capacity
- Average consultation fee overall and by specialization
- Consultation fee ranking by specialization and by department
- Appointment workload by doctor and by department
- Hospitals with the highest number of admissions
- Admission type and admission status patterns
- Average patient length of stay
- Room distribution by type
- Treatments and laboratory tests with the highest activity
- Medicine categories with the highest sales
- Total billed value, billing component contribution, and payments collected
- Gap between billed and collected amounts

## Project Files
```text
Medicare/
└── Medicare.sql
```

The SQL file includes database creation, table creation, data insertion, data profiling, data cleaning, and SQL analysis and KPI queries.

## Outcome
The project transforms hospital records into **structured SQL analysis, operational KPIs, and business insights**. It supports understanding of doctor and department workload, admissions and patient stay, pharmacy and laboratory activity, and billing-to-payment performance.

**Project Type:** Academic / Data Analytics Project  
**Domain:** Healthcare Analytics  
**Database:** MySQL
