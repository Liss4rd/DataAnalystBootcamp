
This section covers Temp Tables.

Temp tables are a collection of rows stored on data pages in tempdb. The data pages may reside 
partially or entirely in memory. This aspect of temp tables makes it impossible with my
job because we have a limited amount of memory in the coding environment provided to my team.

Temp tables may be indexed and have column statistics.

Temp Employee Table Example:
```
CREATE TABLE #temp_Employee
(
EmployeeID INT,
JobTitle VARCHAR(100),
Salary INT
)

INSERT INTO #temp_Employee
SELECT * 
FROM SQLTutorial..EmployeeSalary

SELECT *
FROM #temp_Employee

--DROP TABLE #temp_Employee
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/cb26ac65-0bf1-4c86-bc68-4b5d6e91dc60)

If the temp table already exists, you might run into an error when you try to create it 
a second time. To avoid this, use: "DROP TABLE IF EXISTS TABLE_NAME".

Temp Employee2 Table Example:
```
DROP TABLE IF EXISTS #temp_Employee2
CREATE TABLE #temp_Employee2
(
JobTitle VARCHAR(50),
EmployeesPerJob INT,
AvgAge INT,
AvgSalary INT
)

INSERT INTO #temp_Employee2
SELECT JobTitle, COUNT(JobTitle), Avg(Age), AVG(Salary)
FROM SQLTutorial..EmployeeDemographics dem
JOIN SQLTutorial..EmployeeSalary sal
	ON dem.EmployeeID = sal.EmployeeID
GROUP BY JobTitle

SELECT *
FROM #temp_Employee2
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/1040fd70-d392-4244-af6a-72c1a6136005)

