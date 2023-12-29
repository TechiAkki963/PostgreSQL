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

CREATE TABLE person (
    id BIGSERIAL NOT NULL PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    gender VARCHAR(7) NOT NULL,
    date_of_birth DATE NOT NULL,
);
