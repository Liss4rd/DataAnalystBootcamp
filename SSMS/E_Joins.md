
This section covers INNER and FULL/LEFT/RIGHT Outer Joins.

INNER JOIN Example:
```
SELECT *
FROM SQLTutorial.dbo.EmployeeDemographics
Join SQLTutorial.dbo.EmployeeSalary
ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/37b7fe6c-d1db-4ef2-b294-dc90abea9c0e)

FULL OUTER JOIN Example:
```
SELECT *
FROM SQLTutorial.dbo.EmployeeDemographics
Full Outer Join SQLTutorial.dbo.EmployeeSalary
ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/19a5d7de-3dfb-498f-a312-bb44a36f0e4e)

LEFT JOIN Example:
```
SELECT *
FROM SQLTutorial.dbo.EmployeeDemographics
Left Join SQLTutorial.dbo.EmployeeSalary
ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/d00e7d86-87e3-4520-8f78-f0b47cefb2c6)

RIGHT JOIN Example:
```
SELECT *
FROM SQLTutorial.dbo.EmployeeDemographics
Right Join SQLTutorial.dbo.EmployeeSalary
ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/dfdf70e1-e858-49e5-b4d6-43a618b963cf)
