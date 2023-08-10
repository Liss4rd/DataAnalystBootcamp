
This section covers Partition By.

PARTITION BY is used to divide the resulting set into partitions and perform computations on each subset of partitioned data. PARTITION BY works with the OVER clause to specify the column on which we need to perform aggregation. For example, say you want to pull multiple columns from a table, but it wouldn't make sense to use GROUP BY with all of them. You can use PARTITION BY to avoid that requirement.

```
SELECT FirstName, LastName, Gender, Salary,
COUNT(Gender) OVER (PARTITION BY Gender) as TotalGender
FROM EmployeeDemographics dem
JOIN EmployeeSalary sal
ON dem.EmployeeID = sal.EmployeeID
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/2a8b6700-72dc-4b67-85f9-4648cb2b6e6b)

You can use PARTITION BY to avoid interacting with those other columns.
This also avoids the use of a CTE with the same table to retrieve aggregate data.

The OVER() clause uses a group result. 
For example, say we wanted to know the AVG(Salary) without differentiating between JobTitles. We could use:

```
SELECT DISTINCT Gender,
AVG(Salary) OVER () AS Average_Overall_Salary,
AVG(Salary) OVER (PARTITION BY Gender) Average_Salary_by_Gender
FROM SQLTutorial.dbo.EmployeeDemographics D
JOIN SQLTutorial.dbo.EmployeeSalary S
	ON S.EmployeeID = D.EmployeeID;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/55ac6984-9eaa-438d-9b9f-d98b38d655cd)

