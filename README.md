# SQL-Cheat-Sheet
A super simple SQL cheatsheet.

## Basics
### CRUD
#### Insert
```
INSERT INTO table (column_1, column_2, column_3)
VALUES (value_1, value_2, value_3)
WHERE *condition*;
```


#### Select
```
SELECT column_1, column_2, column_3
FROM table_name
WHERE *condition*
AND *condition*;
```

#### Update
```
UPDATE table_name
SET column_1 = value_1, column_2 = value_2
WHERE *condition*
OR *condition*;
```

#### Delete
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
```
CREATE TABLE table_name
(
id INT PRIMARY KEY,
some_data VARCHAR(50),
column_name3 DATATYPE,
);
```
Data types: http://www.tutorialspoint.com/sql/sql-data-types.htm

#### Delete
`DROP TABLE table_name;`

#### Add Column
```
ALTER TABLE table_name
ADD COLUMN column_name datatype;
```

#### Delete Column
```
ALTER TABLE table_name
DROP COLUMN column_name;
```

#### Modify Datatype
```
ALTER TABLE table_name
MODIFY COLUMN column_name datatype;
```

#### Constraints
```
ALTER TABLE table_name
ADD CONSTRAINT constraintname CHECK (CONDITION);
```
```
ALTER TABLE table_name
ADD CONSTRAINT constraintname UNIQUE (column_1, column_2, column_3);
```
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
```
SELECT count(*)
FROM table_name;
```
*Note:* If you specify a column name instead of (*), the number returned is the amount of rows that do not contain a NULL value.

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
