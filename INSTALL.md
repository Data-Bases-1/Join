<p align="center">
  <img src="https://www.especial.gr/wp-content/uploads/2019/03/panepisthmio-dut-attikhs.png" alt="UNIWA" width="150"/>
</p>

<p align="center">
  <strong>UNIVERSITY OF WEST ATTICA</strong><br>
  SCHOOL OF ENGINEERING<br>
  DEPARTMENT OF COMPUTER ENGINEERING AND INFORMATICS
</p>

<p align="center">
  <a href="https://www.uniwa.gr" target="_blank">University of West Attica</a> ·
  <a href="https://ice.uniwa.gr" target="_blank">Department of Computer Engineering and Informatics</a>
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

<hr>

<p align="center">
  <strong>Supervision</strong>
</p>

<p align="center">
  Supervisor: Periklis Andritsos, Professor
</p>
<p align="center">
  <a href="https://ice.uniwa.gr/en/emd_person/periklis-andritsos/" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/periklisandritsos/" target="_blank">LinkedIn</a>
</p>

<p align="center">
  Co-supervisor: Anastasios Tsolakidis, Assistant Professor<br>
</p>

<p align="center">
  <a href="https://alis.uniwa.gr/en/profile/anastasios-tsolakidis" target="_blank">UNIWA Profile</a> ·
  <a href="https://www.linkedin.com/in/tasos-tsolakidis-35493930/" target="_blank">LinkedIn</a>
</p>

</hr>

---

<p align="center">
  Athens, June 2023
</p>

---

<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSnmdUOpxbVHjMmT1NOR5rpdDHOKK88HsRf6Q&s" width="250"/>
</p>

---

# INSTALL

## Classification and Suggestions - GROUP BY, AND, HAVING, JOIN

This guide describes how to install, initialize, and verify the database environment required to execute the laboratory tasks.  
You will need a **Relational Database Management System (RDBMS)** that supports SQL, such as **MySQL** or **MariaDB**.

---

## 1. Prerequisites

Before using this project, ensure you have the following installed:

### 1.1 Database Management System (DBMS)

- **MySQL** (recommended)
- Compatible alternatives:
  - MariaDB
  - PostgreSQL _(minor syntax adjustments may be required)_

### 1.2 SQL Client / Interface

Any SQL client capable of executing `.sql` scripts:

- MySQL Workbench _(recommended)_
- phpMyAdmin
- DBeaver
- Command-line MySQL client

Make sure your SQL client is properly connected to your database server.

---

## 2. Installation

### 2.1 Clone the Repository

Open a terminal/command prompt and run:

```bash
git clone https://github.com/Data-Bases-1/Join.git
```

### 2.2 Alternative (Without Git)

- Open the repository URL in your browser
- Click Code → Download ZIP
- Extract the ZIP file to a local directory

---

## 2.3 Database Initialization

First, remove any existing version of the database to avoid conflicts. Then create and select the new database.

```sql
DROP DATABASE IF EXISTS new_personnel;
CREATE DATABASE IF NOT EXISTS new_personnel;
USE new_personnel;
```

---

## 2.4 Table Creation

Tables must be created in a specific order to satisfy Foreign Key constraints.

### 2.4.1 Creation Order

1. `DEPT`
2. `EMP`
3. `PROJ`
4. `ASSIGN`

### 2.4.2 Table Descriptions

- `DEPT`

  Stores department information, including department number, name, and location.

- `EMP`

  Stores employee details and references the DEPT table through the DEPTNO foreign key.

- `PROJ`

  Contains project codes and project descriptions.

- `ASSIGN`

  A junction table that links employees to projects and records the time spent on each project.

---

## 3. Data Population

Insert the sample data provided in the laboratory task to populate the database.

### 3.1 Sample Data Categories

- `Departments`

  Add department records with locations such as ATHENS and LONDON.

- `Employees`

  Insert employee records including staff such as CODD, ELMASRI, and NAVATHE.

- `Projects`

  Define projects such as PAYROLL and PERSONNEL.

- `Assignments`

  Link employees to projects with assigned time
  (e.g., Employee 10 assigned to Project 100 for 40 hours).

---

## 4. Verification

Use the following SQL commands to verify that the database schema and data have been created successfully:

```sql
SELECT * FROM DEPT;
SELECT * FROM EMP;
SELECT * FROM PROJ;
SELECT * FROM ASSIGN;
```

---

## 5. Open the Documentation

1. Navigate to the `docs/` directory
2. Open the report corresponding to your preferred language:
   - English: `Classification-Join-Tables.pdf`
   - Greek: `Ταξινόμηση-Join-Συνδέσεις.pdf`
