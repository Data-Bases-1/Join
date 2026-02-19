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

# README

## Classification and Suggestions - GROUP BY, AND, HAVING, JOIN

The objective of this task is to strengthen practical skills in **SQL querying**, focusing on data classification, aggregation, and relational joins using a structured personnel database.

---

## Table of Contents

| Section | Folder / File                         | Description                                        |
| ------: | ------------------------------------- | -------------------------------------------------- |
|       1 | `assign/`                             | Assignment material                                |
|     1.1 | `assign/assignment_03.pdf`            | Assignment description (English)                   |
|     1.2 | `assign/εργασία_03.pdf`               | Assignment description (Greek)                     |
|       2 | `docs/`                               | Theoretical documentation                          |
|     2.1 | `docs/Classification-Join-Tables.pdf` | Table classification and JOIN operations (English) |
|     2.2 | `docs/Ταξινόμηση-Join-Συνδέσεις.pdf`  | Table classification and JOIN operations (Greek)   |
|       3 | `README.md`                           | Project documentation                              |
|       4 | `INSTALL.md`                          | Usage instructions                                 |

---

## 1. Database Schema

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

## 2. Key SQL Operations Included

The assignment covers a wide range of essential SQL functionalities:

### 2.1 Data Selection & Sorting

- Use of `ORDER BY` to organize employee lists based on:
  - Commission
  - Job position
  - Salary

---

## 3. Aggregation

- Application of `GROUP BY` and `HAVING` to:
  - Calculate average salaries per department
  - Filter results based on employee count conditions

---

## 4. Date Functions

- Calculation of employee service years using:
  - `DATEDIFF`
  - `FORMAT`
- Reference date used: **2020-04-15**

---

## 5. Table Joins

- **Equi-Joins**  
  Linking employees to their respective departments and projects.

- **Self-Joins**  
  Joining the `EMP` table to itself to identify employee–manager relationships.

- **Multiple Joins**  
  Connecting `EMP`, `ASSIGN`, and `PROJ` tables to identify employees working **more than 50 hours** on specific projects.

---

## 6. Sample Result Set

As an example, the self-join operation that maps employees to their managers produces the following structure:

| Department | Manager | Employee |
| ---------- | ------- | -------- |
| ACCOUNTING | ELMASRI | CODD     |
| ACCOUNTING | ELMASRI | DATE     |
| ACCOUNTING | ELMASRI | ELMASRI  |
| SALES      | NAVATHE | NAVATHE  |
