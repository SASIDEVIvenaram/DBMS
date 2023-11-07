# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

## Create the table as given below:
```sql
create table manager(enumber int,ename varchar,salary int,commission int,annualsalary int,Hiredate varchar,designation vachar,deptno int,reporting varchar);
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:

update manager set salary=salary+(salary*0.10);


### OUTPUT:'
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/05a37c0e-a6da-43d2-91c8-88ceeee8448f)



### Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
delete from manager where salary<2750;


### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/fc282edd-1c38-479d-a032-5179e38b686c)


### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
select ename as "Name",salary*12 as "Annual salary" from manager;

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/b7fe2085-486e-430a-8061-6e7232c2143d)


### Q4)	List the names of Clerks from emp table.


### QUERY:
select ename from manager where designation='clerk';


### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/4ef98158-9ca7-4489-9191-b7ec33c40858)

### Q5)	List the names of employee who are not Managers.

### QUERY:
select ename from manager where designation <> 'manager';

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/0464eced-a962-4239-8a26-0955f7d621a8)



### Q6)	List the names of employees not eligible for commission.


### QUERY:
select ename from manager where commission=0;


### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/e75c20b1-18d3-42e8-bddb-bd284a5f7f77)



### Q7)	List employees whose name either start or end with ‘s’.


### QUERY:
select ename from manager where ename like '%s' or ename like 's%';

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/d1beae0d-6feb-4919-8c1d-2ded2bf20a5d)


### Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.


### QUERY:
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;


### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/22d643d9-88fb-4e71-93cf-31d5c963c9ee)


### Q9) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/f4fa653f-2463-4180-a5be-2db3b02e0a50)


### Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
 select ename,deptno,salary from manager order by deptno asc,salary desc;


### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/d648feda-5f03-4bc4-9c27-e9fa17a1f84b)


### Q11) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
select ename from manager where deptno not in (30,40,10);

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/aeb20207-0520-40de-a2cd-21cdce341715)

### Q12) Find number of rows in the table EMP

### QUERY:
select count(*) from manager;
### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/aba95e8b-198b-4fc1-a563-59648d96f941)


### Q13) Find maximum, minimum and average salary in EMP table.
### MAXIMUM
### QUERY:
select max(salary) from manager;

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/161961c6-9223-4d4e-8f94-cb1deaa69509)
### MAXIMUM
### QUERY:
select min(salary) from manager;
### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/87197178-e5b6-4665-a065-0a3aa0f49626)
### AVERAGE:
### QUERY:
select avg(salary) from manager;
### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/386c64eb-c820-4096-abc3-099d6fd9fa43)

### Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;

### OUTPUT:
![image](https://github.com/SASIDEVIvenaram/DBMS/assets/118707332/eb8d1370-c455-4a2b-9401-501d832e0c31)


## RESULT :
Thus the basic DML commands are executed successfully.
