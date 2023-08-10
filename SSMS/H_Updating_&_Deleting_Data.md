
This section covers Updating/Deleting data.

UPDATE Statement Example:
```
UPDATE EmployeeDemographics
SET EmployeeID = 1012, Age = 31, Gender = 'Female'
WHERE FirstName = 'Holly'
AND LastName = 'Flux'

SELECT * FROM EmployeeDemographics;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/2ed81436-1571-4f72-86c8-2e1a2174b841)

DELETE Statement Example:
```
DELETE FROM SQLTutorial.dbo.EmployeeDemographics
WHERE EmployeeID = 1004

SELECT * FROM EmployeeDemographics;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/12c2fd83-d2c4-46b5-a052-ef5dae516a29)
