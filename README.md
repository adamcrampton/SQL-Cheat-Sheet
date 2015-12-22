# SQL-Cheat-Sheet
A super simple SQL cheatsheet.

## Basics
### CRUD
#### Insert
```
INSERT INTO table (column_1, column_2, column_3)
VALUES (value_1, value_2, value_3);
```
#### Select
**Example with WHERE and AND condition.**
```
SELECT column_1, column_2, column_3
FROM table_name
WHERE *condition*
AND *condition*;
```
#### Update
**Example with WHERE and OR condition.**
```
UPDATE table_name
SET column_1 = value_1, column_2 = value_2
WHERE *condition*
OR *condition*;
```

#### Delete
**Example with WHERE condition.**
```
DELETE FROM table_name
WHERE *condition*;
```
---
### Databases
```
CREATE DATABASE db_name;

DROP DATABASE db_name;
```
---
### Tables
#### Create
**Example with PRIMARY KEY, VARCHAR and INT datatypes, and NOT NULL constraint.**
```
CREATE TABLE table_name
(
id INT PRIMARY KEY,
column_name_1 VARCHAR(50) NOT NULL,
column_name_2 INT,
);
```
Data types: http://www.tutorialspoint.com/sql/sql-data-types.htm

#### Delete
`DROP TABLE table_name;`

#### Add Column
```
ALTER TABLE table_name
ADD COLUMN column_name *datatype*;
```

#### Delete Column
```
ALTER TABLE table_name
DROP COLUMN column_name;
```

#### Modify Datatype
```
ALTER TABLE table_name
MODIFY COLUMN column_name *datatype*;
```

#### Constraints
**Example using condition check.**
```
ALTER TABLE table_name
ADD CONSTRAINT constraintname CHECK column_1 < 50;
```
**Example with UNIQUE value constraint**
```
ALTER TABLE table_name
ADD CONSTRAINT constraintname UNIQUE (column_1, column_2, column_3);
```
**Example with PRIMARY KEY constraint**
```
ALTER TABLE table_name
ADD CONSTRAINT primarykeyname PRIMARY KEY (column_1);
```
```
ALTER TABLE table_name
DROP CONSTRAINT constraintname;
```
```
ALTER TABLE table_name
DROP CONSTRAINT constraintname;
```

##### MySQL exceptions
**To drop a constraint:**
```
ALTER TABLE table_name
DROP INDEX constraintname;
```

**To drop the primary key:**
```
ALTER TABLE table_name
DROP PRIMARY KEY;
```
---
## Aggregate Functions
### Basic Selects
```
SELECT count(*)
FROM table_name;
```
**Note:** If you specify a column name instead of (*), the number returned is the amount of rows that do not contain a NULL value.

For columns containing numbers:
```
SELECT sum(column_name)
FROM table_name;
```
```
SELECT avg(column_name)
FROM table_name;
```
```
SELECT max(column_name)
FROM table_name;
```
```
SELECT min(column_name)
FROM table_name;
```
### Using GROUP BY
```
SELECT column_1, sum(column_2)
FROM table_name
GROUP BY column_1
```
### Filtering using HAVING
```
SELECT column_1, sum(column_2)
FROM table_name
GROUP BY column_1
HAVING count(*) > 1;
```
### Using a WHERE clause
```
SELECT column_1, sum(column_2)
FROM table_name
WHERE column_2 > 10000
GROUP BY column_1
HAVING count(*) > 1;
```
