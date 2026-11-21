# Medical Data History – SQL Project

A SQL project built on a medical database of patients, admissions, doctors and provinces. It sets up a MySQL environment with Docker and answers 35 questions using SQL queries.

## Project Tasks
1. **Task 1:** Pull and run a Docker image with a SQL environment.
2. **Task 2:** Write and run 35 SQL queries on the project database.
3. Write a report on the challenges faced.

## Database Tables
| Table | Description |
|---|---|
| `patients` | Patient details such as name, gender, birth date, city, allergies, height, weight and province |
| `admissions` | Admission and discharge dates, diagnosis and attending doctor |
| `doctors` | Doctor names and specialty |
| `province_names` | Province IDs and full province names |

## Files in this Repository
| File | Purpose |
|---|---|
| `Dockerfile` | Builds the MySQL 8.0 environment |
| `queries.sql` | All 35 SQL queries |
| `Medical_Data_History_SQL_Commands_Final.docx` | Word document of the SQL commands |
| `Report_on_Challenges_Faced.docx` | Report on challenges and solutions |

## How to Run the Docker Environment
```bash
docker build -t medical-sql-env .
docker run -d --name medical-mysql -p 3308:3306 medical-sql-env
docker ps
```
The container starts MySQL 8.0 with a default database named `medical_data_history`. The host port 3308 is used because port 3306 may already be occupied on the local machine.

## SQL Concepts Covered
- `SELECT`, `WHERE`, `ORDER BY`, `LIMIT`
- `GROUP BY` and `HAVING`
- `JOIN` across two and three tables
- Aggregate functions: `COUNT`, `SUM`, `MAX`, `MIN`
- String functions: `CONCAT`, `UPPER`, `LOWER`, `LENGTH`
- Date functions: `YEAR`, `DAY`
- `CASE` expressions, subqueries and `UNION ALL`

## Note on Question 5
The project database account had read-only access, so the `UPDATE` in Question 5 was denied (error 1142). An equivalent `SELECT` with `IFNULL(allergies, 'NKA')` is used instead.

## Author
Boopal – Final-year B.E. Electronics and computer Engineering, data engineering ,ai developer 
