# MySQL Queries

MySQL Queries is SQL commands to insert, read, update, or delete the data to/from the table. 
There are some queries that are frequently used.

## SELECT
`SELECT` statement used to show the data that selected in the statement. The table with certain columns will be shown as you execute the statement.
<br>
<br>
For example, assume the `students` table has some data:
id | name      | student_id | class
-- | --------- | ---------- | -----
1  | Hansen    | 1102213060 | 04
2  | Svendson  | 1102213061 | 05
3  | Pettersen | 1102213062 | 06

You want `name` and `student_id` columns in the `students` table to be shown, you can execute the following syntax:

```sql
SELECT name, student_id FROM students;
```
The output will be like this:
name      | student_id 
--------- | ---------- 
Hansen    | 1102213060 
Svendson  | 1102213061 
Pettersen | 1102213062 

If you want all the columns to be shown, you can execute the following syntax:
```sql
SELECT * FROM students;
```

## WHERE
The `WHERE` clause is used to filter the records. It will show the records that fulfill a specified conditions.
<br>
For example, you want the student that registered in 04 class to be shown, you can execute the following syntax:

```sql
SELECT * FROM students WHERE class = '05';
```
The output will be like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
2  | Svendson  | 1102213061 | 05

You can use the other operators besides `=`, you find them at external resources. Just check it out and you'll find it. Good luck, lads.

## UPDATE
The `UPDATE` statement is used to modify the existing records in a table.
<br>
For example, you want Hansen to be moved to class 05, you can execute the following syntax:

```sql
UPDATE students SET class = '05' WHERE name = 'Hansen';
```
The `students` table now will look like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
1  | Hansen    | 1102213060 | 05
2  | Svendson  | 1102213061 | 05
3  | Pettersen | 1102213062 | 06

<strong>
    Be careful when updating records. If you don't use the WHERE clause, ALL records will be updated!
</strong>

## DELETE
The `DELETE` statement is used to delete existing records in a table.
<br>
For example, you want Hansen to be deleted from the table, you can execute the following syntax:

```sql
DELETE FROM students WHERE name = 'Pettersen';
```
The `students` table now will look like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
2  | Svendson  | 1102213061 | 05
3  | Pettersen | 1102213062 | 06

If you want all the records to be deleted without interfere the table structure, you can use the following syntax:
```sql
DELETE FROM students;
```

## INSERT INTO
The `INSERT INTO` statement is used to insert new records in a table.
<br>
For example, you want insert new row with the `name` is Vincent, the `student_id` is 1102211234, and the `class` is 04, you can execute the following syntax:

```sql
INSERT INTO students (name, student_id, class) VALUES ('Vincent', '1102211234', '04')
```
The output will be like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
2  | Svendson  | 1102213061 | 05
3  | Pettersen | 1102213062 | 06
4  | Vincent   | 1102211234 | 04

Notice that the `id` automatically increse to 4 without you set it manually. It's because you add `AUTO INCREMENT` constraint in the previous section.

## ORDER BY
The `ORDER BY` keyword is used to sort the table in ascending or descending order.
<br>
For example, you want the table sorted by the `class` column, you can execute the following syntax:

```sql
SELECT * FROM students ORDER BY class;
```
The output will be like this:
id | name      | student_id | class
-- | --------- | ---------- | -----
4  | Vincent   | 1102211234 | 04
2  | Svendson  | 1102213061 | 05
3  | Pettersen | 1102213062 | 06

If you want the table sorted descending by the `class` column, you can execute the following syntax:
```sql
SELECT * FROM students ORDER BY class DESC;
```

And that's all for MySQL Queries, next we are going to talk about MySQL Operators.
<br>
GLHF!!!