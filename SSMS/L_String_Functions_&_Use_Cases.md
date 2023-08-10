
This section covers String Functions including TRIM, LTRIM, RTRIM, REPLACE, 
SUBSTRING, UPPER, LOWER.

LTRIM = removes whitespace from the left side of a string
RTRIM = removes whitespace from the right side of a string
TRIM = removes whitespace from both sides of a string
REPLACE = replaces a value temporarily for a query (Syntax: REPLACE(column_name, value_to_be_replaced, replacement_value))

```
CREATE TABLE EmployeeErrors
(EmployeeID VARCHAR(50),
FirstName VARCHAR(50),
LastName VARCHAR(50)
)

INSERT INTO EmployeeErrors VALUES
('1001 ', 'Jimbo', 'Halbert'),
(' 1002', 'Pamela', 'Beasely'),
('1005', 'TOby', 'Flenderson - Fired')

SELECT EmployeeID, TRIM(EmployeeID) as ID_TRIM
FROM EmployeeErrors

--Using TRIM, LTRIM, RTRIM
```
TRIM Example:

![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/66d8c710-3e58-466c-850c-df2c9e3e18a7)

LTRIM Example:
```
SELECT EmployeeID, LTRIM(EmployeeID) as ID_TRIM
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/5080e810-13bb-48f9-983e-f6329ab61043)

RTRIM Example:
```
SELECT EmployeeID, RTRIM(EmployeeID) as ID_TRIM
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/18466799-db32-4c0d-99a3-83df688aa8f2)

REPLACE Example:
```
SELECT LastName, REPLACE(LastName, ' - Fired', '') AS LastNameFixed
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/f5739035-d9c3-4ae6-b9d7-9bf1e9db1273)

