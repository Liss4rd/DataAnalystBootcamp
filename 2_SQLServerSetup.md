## To download Microsoft SQL Server and SSMS, use these links:

Microsoft SQL Server Management Studio: [Microsoft SSMS Download](https://learn.microsoft.com/en-us/sql/ssms/download-sql-server-management-studio-ssms?view=sql-server-ver16)

SQL Server (Express) 2022: [SQL Server Download](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

***

After setting up SQL Server, make sure to "Trust the certificate" in the Login Options tab to gain access.

New Database Creation: Right-click Databases -> "New Database..." -> Create database name -> Ok

For this bootcamp, the chosen name is: "SQL Tutorial."

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/fb8e3938-8cb3-4fa3-823d-3efcd251a834)

New Table Creation: Right-click Table -> "New..." -> New Query

EmployeeDemographics Table:
```
  CREATE TABLE EmployeeDemographics (
  EmployeeID INT, 
  FirstName VARCHAR(50), 
  LastName VARCHAR(50), 
  Age INT, 
  Gender VARCHAR(50) 
  )
```

EmployeeSalary Table:
```
  CREATE TABLE EmployeeSalary (
  EmployeeID INT,
  JobTitle VARCHAR(50),
  Salary INT
  )
```

Insert Values into EmployeeDemographics Table:
```
  INSERT INTO EmployeeDemographics VALUES
  (1001, 'Jim', 'Halpert', 30, 'Male'),
  (1002, 'Pam', 'Beasley', 30, 'Female'),
  (1003, 'Dwight', 'Schrute', 29, 'Male'),
  (1004, 'Angela', 'Martin', 31, 'Female'),
  (1005, 'Toby', 'Flenderson', 32, 'Male'),
  (1006, 'Michael', 'Scott', 35, 'Male'),
  (1007, 'Meredith', 'Palmer', 32, 'Female'),
  (1008, 'Stanley', 'Hudson', 38, 'Male'),
  (1009, 'Kevin', 'Malone', 31, 'Male')
```
Insert Values into EmployeeSalary Table:
```
  INSERT INTO EmployeeSalary VALUES
  (1001, 'Salesman', 45000),
  (1002, 'Receptionist', 36000),
  (1003, 'Salesman', 63000),
  (1004, 'Accountant', 47000),
  (1005, 'HR', 50000),
  (1006, 'Regional Manager', 65000),
  (1007, 'Supplier Relations', 41000),
  (1008, 'Salesman', 48000),
  (1009, 'Accountant', 42000)
```

SSMS has a shortcut to view the Top 1000 Rows, here is the query behind it.
EmployeeDemographics Example:
```
SELECT TOP (1000) [EmployeeID]
      ,[FirstName]
      ,[LastName]
      ,[Age]
      ,[Gender]
FROM [SQLTutorial].[dbo].[EmployeeDemographics]
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/240dd88c-3aab-4321-9680-a5b87e484eb7)



EmployeeSalary Example:
```
SELECT TOP (1000) [EmployeeID]
      ,[JobTitle]
      ,[Salary]
FROM [SQLTutorial].[dbo].[EmployeeSalary]
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/280bb7cd-e743-4a57-9ee0-205ffc530e98)
