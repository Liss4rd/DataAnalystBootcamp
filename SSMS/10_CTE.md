
This section covers Common Table Expressions (CTEs).

CTEs store the data into basically 
an outer subquery that can be used to pull data. 
They're convenient when you might need to retrieve information
from multiple tables and want to make the code 
a bit easier to read.

```
WITH CTE_Employee AS
(
SELECT FirstName, LastName, Gender, Salary,
COUNT(Gender) OVER (PARTITION BY Gender) AS TotalGender,
AVG(Salary) OVER (PARTITION BY Gender) AS AvgSalary
FROM SQLTutorial.dbo.EmployeeSalary sal
JOIN SQLTutorial.dbo.EmployeeDemographics dem
  ON sal.EmployeeID = dem.EmployeeID
WHERE Salary > '45000'
)

SELECT FirstName, AvgSalary
FROM CTE_Employee;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/23881575-8fed-4c91-acf0-083f720c40c5)
