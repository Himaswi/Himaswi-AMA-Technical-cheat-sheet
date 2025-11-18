## SQL & Linux Concepts 
---
## 1. What are Joins?
Joins in SQL are used to **combine rows from two or more tables** based on a related column.  
They help fetch meaningful data spread across multiple tables.
Common types:
- INNER JOIN  
- LEFT JOIN  
- RIGHT JOIN  
- FULL JOIN  
- CROSS JOIN  
- SELF JOIN  
---

## 2. Use of HAVING keyword in SQL
- `HAVING` is used to **filter grouped data** after applying `GROUP BY`.  
- It works with **aggregate functions** like COUNT(), SUM(), AVG().

Example:
```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```
---
## 3. What is GROUP BY?
GROUP BY groups rows that have the same values in specified columns.
It is used with aggregation functions to create summarized reports.
###Example:
```sql
SELECT department, AVG(salary)
FROM employees
GROUP BY department;
```
---
## 4. Explain grep command
grep is a Linux command used to search text patterns inside files.
### Examples:
```
grep "error" logfile.txt
grep -i "hello" file.txt   # case-insensitive search
grep -r "main" src/     
```
---
## 5. Difference Between LEFT JOIN and INNER JOIN
| Feature | INNER JOIN | LEFT JOIN |
|---------|-------------|-----------|
| Matching Rows | Returns only rows that have matching values in both tables | Returns all rows from the left table and matching rows from the right table |
| Non-Matching Rows | Excluded | Returned as NULL for columns from the right table |

### Example:
- **INNER JOIN** → strict match (only matching rows)
- **LEFT JOIN** → keeps all left-side rows (non-matches become NULL)
---
## 6. Real World Use Case of SQL
SQL is used wherever structured data needs to be stored and accessed. Common real-world use cases include:
- **E-commerce:** Managing products, orders, users, and payments  
- **Banking:** Handling accounts, transactions, transfers  
- **Healthcare:** Storing patient records, prescriptions, appointments  
- **Social Media:** Posts, comments, likes, user profiles  
- **Education:** Students, results, attendance, course management  
SQL helps in efficient data storage, retrieval, and analysis in almost every industry.

---
## 7. Explain DELETE command in SQL
The `DELETE` command removes **specific rows** from a table based on a condition.
### Example:
```sql
     DELETE FROM employees WHERE id = 5;
```
---
## 8. Explain LIMIT and OFFSET
Used to control how many rows are returned in a query.
### **LIMIT:**
Limits the number of rows returned.
### Example:
```sql
SELECT * FROM employees LIMIT 5;
```
### **OFFSET:** 
Skips a given number of rows before returning results.
### Example:
```sql
SELECT * FROM employees LIMIT 5 OFFSET 10;
```
---
## 9. Explain PRIMARY KEY and UNIQUE Keyword
### **PRIMARY KEY:**
- Uniquely identifies each row
- Cannot be NULL
- Only one primary key per table
### **UNIQUE :**
- Ensures all values in a column are unique
- Allows NULL values
- Multiple UNIQUE constraints can exist in a table
### Example:
```sql
CREATE TABLE users (
    id INT PRIMARY KEY,
    email VARCHAR(100) UNIQUE
);
```
---
## 10. How to display a full table?
```sql
SELECT * FROM table_name;
```
---
## 11. Difference Between TRUNCATE, DELETE, and DROP

| Command  | What It Does | Removes Rows? | Removes Table Structure? | Can Use WHERE? | Rollback Possible? | Speed |
|----------|--------------|----------------|----------------------------|----------------|----------------------|--------|
| **DELETE** | Deletes specific rows | Yes | No | Yes | Yes | Slow (row-by-row) |
| **TRUNCATE** | Removes all rows instantly | Yes (all rows) | No | No | No (mostly) | Fast |
| **DROP** | Deletes the entire table | Yes | Yes | No | No | Fastest |
### Summary:
- **DELETE** → removes selected rows, can be rolled back  
- **TRUNCATE** → removes all rows, resets table (cannot use WHERE)  
- **DROP** → removes the entire table from the database  
---
## 12. Difference Between WHERE and HAVING in SQL
### **WHERE Clause**
- Filters **rows before** grouping or aggregation.
- Cannot be used with aggregate functions (`COUNT`, `SUM`, `AVG`).
- This filters individual rows before any grouping happens.
### Example (WHERE):
```sql
SELECT *
FROM employees
WHERE salary > 30000;
```
### **HAVING Clause**
- Filters groups after aggregation.
- Used with GROUP BY.
- Supports aggregate functions.
- This filters groups after GROUP BY has aggregated the rows.
### Example (HAVING):
```sql
SELECT department, COUNT(*)
FROM employees
GROUP BY department
HAVING COUNT(*) > 5;
```
### Combined Example
```sql
SELECT department, AVG(salary)
FROM employees
WHERE salary > 30000      -- filters rows
GROUP BY department
HAVING AVG(salary) > 50000;   -- filters groups
```
### Summary Table
| Feature | WHERE | HAVING |
|---------|--------|---------|
| Filters | Before grouping | After grouping |
| Works on | Individual rows | Grouped data |
| Aggregate functions |  Not allowed |  Allowed |
| Used with GROUP BY | Optional | Usually used |




