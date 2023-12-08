# MySQL Joins

MySQL joining tables are used to combine rows two or more tables based on related column between them.
<br>
<br>
Look at the following to tables:

### students Table
id | name      | student_id | class
-- | --------- | ---------- | -----
1  | Hansen    | 1102213060 | 04
2  | Svendson  | 1102213061 | 05
3  | Pettersen | 1102213062 | 06

### courses Table
id | Course          | student_id
-- | --------------- | ----------
1  | Physics         | 1102213060
2  | Calculus        | 1102213060
3  | Linear Algebra  | 1102213061

For example, you want all the records that have matching values in both tables to be shown. You can execute following syntax:
```sql
SELECT students.name, students.class, courses.course 
FROM students 
INNER JOIN courses 
ON students.student_id = courses.student_id
```
The output will be like this:
name     | class | course
-------- | ----- | -----
Hansen   | 04    | Physics
Hansen   | 04    | Calculus
Svendson | 05    | Linear Algebra

## Supported Types of Joins in MySQL
There are the other types of joins in MySQL beside inner join:
- `INNER JOIN`: Returns records that have matching values in both tables
- `LEFT JOIN`: Returns all records from the left table, and the matched records from the right table
- `RIGHT JOIN`: Returns all records from the right table, and the matched records from the left table
- `CROSS JOIN`: Returns all records from both tables