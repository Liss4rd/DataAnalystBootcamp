
This section covers Subqueries (in the SELECT, FROM, and WHERE Statement).

```
SELECT *
FROM EmployeeSalary;
```

Subquery in SELECT Example:

```
SELECT EmployeeID, Salary, (SELECT AVG(Salary) FROM EmployeeSalary) as AllAvgSalary
FROM EmployeeSalary;
```

How to Use Subqueries with PARTITION BY:

```
SELECT EmployeeID, Salary, AVG(Salary) OVER () AS AllAvgSalary
FROM EmployeeSalary;
```

Why GROUP BY doesn't work:
As I mentioned before, being forced to use GROUP BY with the other columns does get the data
we're looking for.
```
SELECT EmployeeID, Salary, AVG(Salary) OVER () AS AllAvgSalary
FROM EmployeeSalary
GROUP BY EmployeeID, Salary
ORDER BY 1, 2
```

Subquery in FROM:
```
SELECT a.EmployeeID, AllAvgSalary
FROM (SELECT EmployeeID, Salary, AVG(Salary) OVER () AS AllAvgSalary
      FROM EmployeeSalary) a
```

Subquery in WHERE:
```
SELECT EmployeeID, JobTitle, Salary
FROM EmployeeSalary
WHERE EmployeeID in (
        SELECT EmployeeID
        FROM EmployeeDemographics
        WHERE Age > 30)
```
