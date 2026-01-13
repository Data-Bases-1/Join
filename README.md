<p align="center">
  <img src="https://www.especial.gr/wp-content/uploads/2019/03/panepisthmio-dut-attikhs.png" alt="UNIWA" width="150"/>
</p>

<p align="center">
  <strong>UNIVERSITY OF WEST ATTICA</strong><br>
  SCHOOL OF ENGINEERING<br>
  DEPARTMENT OF COMPUTER ENGINEERING AND INFORMATICS
</p>

---

<p align="center">
  <strong>Databases I</strong>
</p>

<h1 align="center">
  Classification and Suggestions - GROUP BY, AND, HAVING, JOIN
</h1>

<p align="center">
  <strong>Vasileios Evangelos Athanasiou</strong><br>
  Student ID: 19390005
</p>

<p align="center">
  <a href="https://github.com/Ath21" target="_blank">GitHub</a> ·
  <a href="https://www.linkedin.com/in/vasilis-athanasiou-7036b53a4/" target="_blank">LinkedIn</a>
</p>

<p align="center">
  Supervisor: Anastasios Tsolakidis, Assistant Professor<br>
</p>

<p align="center">
  <a href="https://alis.uniwa.gr/en/profile/anastasios-tsolakidis" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/tasos-tsolakidis-35493930/" target="_blank">LinkedIn</a>
</p>

<p align="center">
  Athens, June 2023
</p>

---

# Project Overview

The objective of this task is to strengthen practical skills in **SQL querying**, focusing on data classification, aggregation, and relational joins using a structured personnel database.

---

## Table of Contents


| Section | Folder / File | Description |
|------:|---------------|-------------|
| 1 | `assign/` | Assignment material |
| 1.1 | `assign/assignment_03.pdf` | Assignment description (English) |
| 1.2 | `assign/εργασία_03.pdf` | Assignment description (Greek) |
| 2 | `docs/` | Theoretical documentation |
| 2.1 | `docs/Classification-Join-Tables.pdf` | Table classification and JOIN operations (English) |
| 2.2 | `docs/Ταξινόμηση-Join-Συνδέσεις.pdf` | Table classification and JOIN operations (Greek) |
| 3 | `README.md` | Repository overview and instructions |

---


## Database Schema

The project utilizes a database named **`new_personnel`**, which consists of four primary tables:

- **DEPT**  
  Stores department information, including department number, name, and location.

- **EMP**  
  Contains employee records such as job titles, hire dates, salaries, commissions, and manager IDs.

- **PROJ**  
  Holds project codes and project descriptions.

- **ASSIGN**  
  A junction table linking employees to projects, including the time spent on each project.

---

## Key SQL Operations Included

The assignment covers a wide range of essential SQL functionalities:

### Data Selection & Sorting
- Use of `ORDER BY` to organize employee lists based on:
  - Commission
  - Job position
  - Salary

---

### Aggregation
- Application of `GROUP BY` and `HAVING` to:
  - Calculate average salaries per department
  - Filter results based on employee count conditions

---

### Date Functions
- Calculation of employee service years using:
  - `DATEDIFF`
  - `FORMAT`
- Reference date used: **2020-04-15**

---

### Table Joins

- **Equi-Joins**  
  Linking employees to their respective departments and projects.

- **Self-Joins**  
  Joining the `EMP` table to itself to identify employee–manager relationships.

- **Multiple Joins**  
  Connecting `EMP`, `ASSIGN`, and `PROJ` tables to identify employees working **more than 50 hours** on specific projects.

---

## Sample Result Set

As an example, the self-join operation that maps employees to their managers produces the following structure:

| Department   | Manager  | Employee |
|-------------|----------|----------|
| ACCOUNTING  | ELMASRI  | CODD     |
| ACCOUNTING  | ELMASRI  | DATE     |
| ACCOUNTING  | ELMASRI  | ELMASRI  |
| SALES       | NAVATHE  | NAVATHE  |

---

# Installation & Setup Guide

This guide describes how to install, initialize, and verify the database environment required to execute the laboratory tasks.  
You will need a **Relational Database Management System (RDBMS)** that supports SQL, such as **MySQL** or **MariaDB**.

---

## Prerequisites

Before using this project, ensure you have the following installed:

### 1. Database Management System (DBMS)
- **MySQL** (recommended)
- Compatible alternatives:
  - MariaDB
  - PostgreSQL *(minor syntax adjustments may be required)*

### 2. SQL Client / Interface
Any SQL client capable of executing `.sql` scripts:
- MySQL Workbench *(recommended)*
- phpMyAdmin
- DBeaver
- Command-line MySQL client

Make sure your SQL client is properly connected to your database server.

---

## Installation

### 1. Clone the Repository

Open a terminal/command prompt and run:

```bash
git clone https://github.com/Data-Bases-1/Join.git
```

#### Alternative (Without Git)

- Open the repository URL in your browser
- Click Code → Download ZIP
- Extract the ZIP file to a local directory

---

## 1. Database Initialization

First, remove any existing version of the database to avoid conflicts. Then create and select the new database.

```sql
DROP DATABASE IF EXISTS new_personnel;
CREATE DATABASE IF NOT EXISTS new_personnel;
USE new_personnel;
```

## 2. Table Creation
Tables must be created in a specific order to satisfy Foreign Key constraints.

### Creation Order
1. `DEPT`
2. `EMP`
3. `PROJ`
4. `ASSIGN`

### Table Descriptions
- `DEPT`

  Stores department information, including department number, name, and location.

- `EMP`

  Stores employee details and references the DEPT table through the DEPTNO foreign key.

- `PROJ`

  Contains project codes and project descriptions.

- `ASSIGN`

  A junction table that links employees to projects and records the time spent on each project.

## 3. Data Population
Insert the sample data provided in the laboratory task to populate the database.

### Sample Data Categories
- `Departments`

  Add department records with locations such as ATHENS and LONDON.

- `Employees`

  Insert employee records including staff such as CODD, ELMASRI, and NAVATHE.

- `Projects`

  Define projects such as PAYROLL and PERSONNEL.

- `Assignments`

  Link employees to projects with assigned time
  (e.g., Employee 10 assigned to Project 100 for 40 hours).

## 4. Verification
Use the following SQL commands to verify that the database schema and data have been created successfully:
```sql
SELECT * FROM DEPT;
SELECT * FROM EMP;
SELECT * FROM PROJ;
SELECT * FROM ASSIGN;
```

---

## Open the Documentation
1. Navigate to the `docs/` directory
2. Open the report corresponding to your preferred language:
    - English: `Classification-Join-Tables.pdf`
    - Greek: `Ταξινόμηση-Join-Συνδέσεις.pdf`