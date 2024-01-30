# PostgreSQL

### PostgreSQL

---

> to create database

```postgres
CREATE DATABASE databasename;
```

---

---

> to view the list of all databases

```
 \l (smallcase L)
```

---

---

> to connect to a database

```
\c databasename
```

---

> to delete the database \*\*\*

```
DROP DATABASE databasename; --------
```

---

> to clear screen in SQL shell

```
\! cls or \!clear --------
```

---

---

> to view/acess table

```
\d
```

---

---

> to acess the table by TableName

```
 \d tablename
```

---

---

> to delete table \*\*\*

```
DROP TABLE tablename;
```

---

### Switch User

> Ubuntu

```
sudo -i -u postgres
```

If your password does not work, use 'postgres' for the username. Your code should look like this ` psql -h localhost -p 5432 -U postgres test`

In cmd : to change the username , we can use `psql -U` postgres and then the given password

---

CREATE TABLE

---

> Without Email as every person may not have Email

```
CREATE TABLE person (
id BIGSERIAL NOT NULL PRIMARY KEY,
first_name VARCHAR(50) NOT NULL,
last_name VARCHAR(50) NOT NULL,
gender VARCHAR(7) NOT NULL,
date_of_birth DATE NOT NULL,
);
```

> With Email

```
CREATE TABLE person ( id BIGSERIAL NOT NULL PRIMARY KEY,
first_name VARCHAR(50) NOT NULL,
last_name VARCHAR(50) NOT NULL,
gender VARCHAR(7) NOT NULL,
date_of_birth DATE NOT NULL,
email VARCHAR(150)
);
```

> To view the data table

```
SELECT * FROM person;
```

---

INSERT DATA in TABLE

```
INSERT INTO person (
first_name,
last_name,
gender,
date_of_birth,
email)
VALUES ('Anne','Smith','FEMALE',DATE '1998-05-01');
yyyy-mm-dd
```

```
VALUES('JAKE','BROWN','MALE',DATE '1994-02-03','Jake@ymail.com');
```

---

> FOR DUMMY DATA --- Mockaroo
> <a>https://www.mockaroo.com/</a>

---

---

> To import SQL file

```
\i /filepath/filename.sql
```

---

> ORDER BY -- IT is used to SORT the list in ASCENDING or DESCENDING Order

```
SELECT \* FROM person ORDER BY country;
```

```
for ASCENDING ORDER
SELECT \* FROM person ORDER BY first_name ASC;
```

```
for DESCENDING ORDER
SELECT \* FROM person ORDER BY country DESC;
```

```
We can SORT by id ORDER -- Serial no.
SELECT \* FROM person ORDER BY id email;
```

---

> TO DISPLAY DUPLICATE DATA at ONCE

```
SELECT DISTINCT country FROM person ORDER BY person;
```

---

> WHERE , AND

```
SELECT \* FROM person WHERE gender = 'Male';
```

```
SELECT \* FROM person WHERE gender = 'Female' AND country = 'Poland';
```

```
SELECT \* FROM person WHERE gender = 'Female' AND (country = 'Poland' OR country = 'China');
```

```
SELECT \* FROM person WHERE gender = 'Female' AND (country = 'Poland' OR country = 'China') AND last_name = 'Downs';
```
