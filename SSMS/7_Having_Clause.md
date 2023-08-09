
This section covers the HAVING clause.

HAVING Clause Example:
```
SELECT JobTitle, COUNT(JobTitle)
FROM SQLTutorial.dbo.EmployeeDemographics
JOIN SQLTutorial.dbo.EmployeeSalary
	ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID
GROUP BY JobTitle
HAVING COUNT(JobTitle) > 1;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/255d71e0-07f6-4ded-8cff-ceda462a67b0)

Another HAVING Clause Example:
```
SELECT JobTitle, AVG(Salary)
FROM SQLTutorial.dbo.EmployeeDemographics
JOIN SQLTutorial.dbo.EmployeeSalary
	ON EmployeeDemographics.EmployeeID = EmployeeSalary.EmployeeID
GROUP BY JobTitle
HAVING AVG(Salary) > 45000
ORDER BY AVG(Salary);
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/f9f57848-308f-4226-807f-2a827558d5d1)
