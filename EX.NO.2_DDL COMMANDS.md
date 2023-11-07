# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
## DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### 1) Create a database studentdb
### SQL QUERY:
create database student_db;

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/afb1fb7d-977c-441f-a8ea-5c9e7d10e7cc)

### 2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
create table student(Regno int, Name varchar(20),Age int,Address varchar(50),Phonenumber varchar(10));

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/35ec9dce-e676-4dee-8fe9-b95e8db3c07e)


### 3) Alter the above student table by adding another attribute department

### SQL QUERY: 
alter table student add dept varchar(20);

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/fc795c4a-ff2d-4373-9d5e-29e0970b7e9f)


### 4) Rename the student table to mystudent

### SQL QUERY: 
rename table student to mystudent;

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/7b0162da-97de-4979-a38b-9f27ab267433)


### 5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
truncate table mystudent;
### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/6ac30209-4af2-47b5-88ba-4cf3d1c518ce)

### 4) Drop the mystudent table
 
### SQL QUERY: 
drop table mystudent;

### OUTPUT:

![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/ebb895b1-8b0c-4bb2-bbc5-81e7e9df2042)

## Result:
Thus the basic DDL commands in SQL are executed. 


