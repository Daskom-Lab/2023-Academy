# Constraints
Constaints are used to specify rules for data in the table. Constraints can be specified when the table is created with the `CREATE TABLE` statement, or after the table is created with the `ALTER TABLE` statement.

## Unique
The `UNIQUE` constraint ensures that all values in a column must be different.
<br>
<br>
If you want add unique constraint when you create a table, you can use this command:

```sql
CREATE TABLE students (
    id int,
    name varchar(255),
    student_id varchar(255),
    class varchar(255),
    UNIQUE (student_id)
);
```
To name a UNIQUE constraint, and to define a UNIQUE constraint on multiple columns, use the following command:
```sql
CREATE TABLE students (
    id int,
    name varchar(255),
    student_id varchar(255),
    class varchar(255),
    CONSTRAINT UC_students UNIQUE (id, student_id)
);
```

If you want add unique constraint when the table is already created, you can use this command:
```sql
ALTER TABLE students
ADD CONSTRAINT UC_students UNIQUE (id,student_id);
```
To drop a UNIQUE constraint, use the following command:
```sql
ALTER TABLE students
DROP INDEX UC_students;
```

## Primary Key
The `PRIMARY KEY` constraint uniquely identifies each record in a table. Primary keys must contain UNIQUE values, and cannot contain NULL values. Primary keys is usually initiated with `AUTO INCREMENT` constraint.
<br>
<br>
If you want create primary key when you create a new table, you can use this command:

```sql
CREATE TABLE students (
    id int NOT NULL AUTO INCREMENT,
    name varchar(255),
    student_id varchar(255) NOT NULL,
    class varchar(255),
    CONSTRAINT PK_students PRIMARY KEY (id)
);
```
If you want add primary key when the table is already created, you can use this command:
```sql
ALTER TABLE students
ADD CONSTRAINT PK_students PRIMARY KEY (id);
```
To drop a primary key, use the following command:
```sql
ALTER TABLE students
DROP PRIMARY KEY;
```

## Foreign Key
Foreign Keys are used to mark a table as connected to another table in the context of the parent and child tables. A table is said to be a child if it has a field which is a reference to a key in the parent table. This is used to maintain consistency and linkages between tables.
<br>
<br>
One of the characteristics that we can pay attention to is that if we delete one of the rows in the parent table, the related row will also be deleted, or fields embedded in the child row can be made NULL.
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
4  | Fluid Mechanics | 1102213062
5  | Soil Mechanics  | 1102213062

Notice that the `student_id` column in the `courses` table points to the `student_id` column in the `students` table. The `student_id` column in the `students` table is the PRIMARY KEY in the `students` table. The `student_id` column in the `courses` table is a FOREIGN KEY in the `courses` table.
<br>
<br>
If you want create foreign key when you create a new table, you can use this command:

```sql
CREATE TABLE courses (
    id int NOT NULL,
    course varchar(255),
    student_id varchar(255),
    PRIMARY KEY (id), 
    CONSTRAINT FK_courses FOREIGN KEY (student_id) 
    REFERENCES students(student_id) 
);
```
If you want add foreign key when the table is already created, you can use this command:
```sql
ALTER TABLE courses
ADD CONSTRAINT FK_courses FOREIGN KEY (student_id) REFERENCES students(student_id);
```
To drop a foreign key, use the following command:
```sql
ALTER TABLE courses
DROP FOREIGN KEY FK_courses;
```

And that's all for MySQL Constraint, next we are going to talk about MySQL Query.
<br>
GLHF!!!