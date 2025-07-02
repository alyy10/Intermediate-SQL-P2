# 📊 A data analysis and reporting project over a normalized operational database schema.

This project demonstrates a simple data warehouse schema and analytical SQL queries for data exploration and reporting.  
It covers **Data Definition Language (DDL)** to set up tables and sequences, and **Data Analysis** using various SQL constructs.

## 🛠 DDL (Data Definition Language)

The `DDL.sql` script creates and populates the schema:

- **Tables**
  - `REGIONS` – Regions like Europe, Asia, etc.
  - `COUNTRIES` – Countries with foreign keys to regions.
  - `LOCATIONS` – Addresses, cities, linked to countries.
  - `DEPARTMENTS` – Company departments, linked to locations.
  - `JOBS` – Job roles with salary ranges.
  - `EMPLOYEES` – Employee records, linked to departments and jobs.
  - `JOB_HISTORY` – Records of past job assignments.

- **Views**
  - `EMP_DETAILS_VIEW` – Combines employee, job, department, location, and region details for easy reporting.

- **Sequences**
  - `LOCATIONS_SEQ`, `DEPARTMENTS_SEQ`, `EMPLOYEES_SEQ` – Auto-increment IDs.

---

## 🔍 Data Analysis

The `Data_Analysis_Part_3.sql` script focuses on analyzing employee and department data.  
It demonstrates:

### ✔ Sub-Queries
- Departments with employees.
- Employees filtered by roles, salary, and departments.

### 🪟 Inline Views
- Join employee data with department and city information.

### 🧮 Aggregate Functions
- `MIN`, `MAX`, `SUM`, `AVG`, `COUNT`.
- Examples: Highest salary, total payroll, average salary, department-wise metrics.

### 📊 Combined Aggregated Results
- Combine multiple metrics in single/multiple rows for reporting.

### 🏢 Department-level Analysis
- Number of employees, max salary, total salary per department.
- Number of departments per location.
- Employees per manager.

### 🧰 Filters and HAVING Clause
- Departments with resignations above a threshold.
- Departments with high salaries.

### ✅ EXISTS Clause
- Compare `EXISTS` vs `IN` and `NOT EXISTS` vs `NOT IN`.

---

## 🏛️ Schema Overview

![Architectural Diagram]

- The database design starts from **Data**, then uses **DDL** (`CREATE`, `ALTER`, `INSERT`) to define schema.
- Data analysis is then performed via:
  - Sub-queries
  - Inline views
  - Aggregate functions
  - Filters and `EXISTS` clauses

---

## 🚀 How to Use

1. Run `DDL.sql` to create tables, sequences, and populate data.
2. Use `Data_Analysis_Part_3.sql` to execute analysis queries.

---

## 📂 Files

| File                        | Purpose                                              |
| --------------------------- | ---------------------------------------------------- |
| `DDL.sql`                   | Create tables, insert initial data, create sequences |
| `Data_Analysis_Part_3.sql`  | Analytical queries for reporting and exploration     |
| `architecturalDiagram.png`  | Visual overview of the data flow & analysis process  |

---

## ✏️ Author

> Built for educational purposes to practice database design and data analysis.

---

## 📢 Note
All queries are tested on **Oracle SQL**; adjust data types or functions if using other databases.

