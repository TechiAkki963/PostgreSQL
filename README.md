# PostgreSQL
PostgreSQL

CREATE DATABASE databasename; -------- to create database
\l                            -------- to view the list of all databases
\c databasename               -------- to connect to a database
DROP DATABASE databasename;   -------- to delete the database ****
\! cls                        -------- to clear screen in SQL shell
\d                            -------- to view/acess table 
\d tablename                  -------- to acess the table by TableName
DROP TABLE tablename;         -------- to delete table ***


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
