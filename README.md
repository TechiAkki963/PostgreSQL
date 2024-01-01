# PostgreSQL
PostgreSQL
<ul>
<li>CREATE DATABASE databasename; -------- to create database
<li>\l (smallcase L)              -------- to view the list of all databases
<li>\c databasename               -------- to connect to a database
<li>DROP DATABASE databasename;   -------- to delete the database ****
<li>\! cls                        -------- to clear screen in SQL shell
<li>\d                            -------- to view/acess table 
<li>\d tablename                  -------- to acess the table by TableName
<li>DROP TABLE tablename;         -------- to delete table ***

</ul>
********************************************************************
If your password does not work, use 'postgres' for the username.  Your code should look like this " psql -h localhost -p 5432 -U postgres test"

In cmd : to change the username , we can use psql -U postgres and then the given password

********************************************************************
CREATE TABLE 
********************************************************************
**Without Email as every person may not have Email
CREATE TABLE person (
    id BIGSERIAL NOT NULL PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender VARCHAR(7) NOT NULL,
    date_of_birth DATE NOT NULL,
);

**With Email
CREATE TABLE person (     id BIGSERIAL NOT NULL PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender VARCHAR(7) NOT NULL,
    date_of_birth DATE NOT NULL,
    email VARCHAR(150)
);

// TO view the data table 
SELECT * FROM person


****************************************************************************
INSERT DATA in TABLE
***************************************************************************

INSERT INTO person (
first_name,
last_name,
gender,
date_of_birth,
email)
VALUES ('Anne','Smith','FEMALE',DATE '1998-05-01');

VALUES('JAKE','BROWN','MALE',DATE '1994-02-03','Jake@ymail.com');


***********************************************************************
to import SQL file 
*******************************************************************
\i /filepath/filename.sql



