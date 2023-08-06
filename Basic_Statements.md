Commands covered in this video include SELECT, TOP, DISTINCT, COUNT, AS, MAX, MIN, AVG.

SELECT statements retrieve rows from either a single or multiple tables. \
This is the most common data manipulation language (DML) command. \
By using '*', you can query all columns in one table or more. 

Returns all the records in EmployeeDemographics table:
```
SELECT *
FROM EmployeeDemographics 
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/1a615627-74af-45e3-b491-486408162069)


Returns the top 5 records in EmployeeDemographics table:
```
SELEC TOP 5 *
FROM EmployeeDemographics
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/2a716c81-0d3e-45d4-b7c8-f9c1262ded9c)

Returns distinct/unique values ONLY in EmployeeDemographics table:
```
SELECT DISTINCT(EmployeeID)
FROM EmployeeDemographics
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/e1bd991a-650d-487b-ba50-67a0daaacf09)

Returns the result of a count of how many last names exist in the EmployeeDemographics table:
```
SELECT COUNT(LastName)
FROM EmployeeDemographics
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/9d3d2742-1c11-44dc-bcd7-ddfd86b9d6fd)

Renames the count value from the previous query:
```
SELECT COUNT(LastName) AS LastNameCount
FROM EmployeeDemographics
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/5030d401-1790-4c13-ac29-238ad85a1bac)

You can actually simply add the name after the unnamed count.
AS is the formal command, but you can omit it as well.

Returns the MAX salary value from the EmployeeSalary table:
```
SELECT MAX(Salary) AS MaxSalary
FROM EmployeeSalary
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/2dfb2de5-972e-4e1c-ba78-b99709ea8d07)

Returns the MIN salary value from the EmployeeSalary table:
```
SELECT MIN(Salary) AS MinSalary
FROM EmployeeSalary
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/f4558b78-1a43-4add-a1b3-f52b68caf0f5)

Returns the AVG salary value from the EmployeeSalary table:
```
SELECT AVG(Salary) AS AverageSalary
FROM EmployeeSalary
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/4d382bd3-3a7c-4dcb-bc0d-87823d3fedee)

Please note, I goofed a little and added space between SQLTutorial so the database name is: "SQL Tutorial."
It's not ideal, but you can use quotations to reference the database for the examples below.
Normally, you would not want to add a space in tables, columns, or database names.


```
SELECT *
FROM "SQL Tutorial".dbo.EmployeeSalary
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/1c084dd5-323e-4e38-8843-d0fc3f069640)







