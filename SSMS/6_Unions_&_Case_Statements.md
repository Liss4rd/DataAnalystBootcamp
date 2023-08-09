
This section covers Union, Union All and Union Operator.

UNION Example:
```
SELECT * 
FROM SQLTutorial.dbo.EmployeeDemographics
WHERE EmployeeID <= 1004

UNION

SELECT *
FROM SQLTutorial.dbo.EmployeeDemographics
WHERE EmployeeID >= 1006;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/59b86f4e-4a38-4d07-aa2c-12dbd2172b0e)

UNION ALL Example:
```
SELECT * 
FROM SQLTutorial.dbo.EmployeeDemographics
WHERE EmployeeID <= 1006

UNION ALL

SELECT *
FROM SQLTutorial.dbo.EmployeeDemographics
WHERE EmployeeID >= 1006;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/1038bcce-eac8-4f93-8719-63f1a583ea5a)

CASE Statement Example:
```
SELECT FirstName, LastName, Age,
CASE 
	WHEN Age > 30 THEN 'Old'
  WHEN Age BETWEEN 27 AND 30 THEN 'Young'
	ELSE 'Baby'
END
FROM SQLTutorial.dbo.EmployeeDemographics
WHERE Age IS NOT NULL
ORDER BY Age;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/d878f4d4-32d7-4d63-9d7f-2636c875a971)

Another CASE Statement Example:
```
ELECT FirstName, LastName, JobTitle, Salary,
CASE 
	WHEN JobTitle = 'Salesman' THEN Salary + (Salary * 0.10)
	WHEN JobTitle = 'Accountant' THEN Salary + (Salary * 0.05)
	WHEN JobTitle = 'HR' THEN Salary + (Salary * 0.000001)
	ELSE Salary + (Salary * .03)
END AS SalaryAfterRaise
FROM SQLTutorial.dbo.EmployeeDemographics
JOIN SQLTutorial.dbo.EmployeeSalary
ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/9c6b46ee-36bc-4dc3-bb0d-8f26529c67f9)
