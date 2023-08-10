
This section covers String Functions including TRIM, LTRIM, RTRIM, REPLACE, 
SUBSTRING, UPPER, LOWER.

LTRIM = removes whitespace from the left side of a string
RTRIM = removes whitespace from the right side of a string
TRIM = removes whitespace from both sides of a string
REPLACE = replaces a value temporarily for a query (Syntax: REPLACE(column_name, value_to_be_replaced, replacement_value))
SUBSTRING = creates a partition of a string (SYNTAX: SUBSTRING(string_value, start, end))

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
```
TRIM Example:
```
SELECT EmployeeID, TRIM(EmployeeID) as ID_TRIM
FROM EmployeeErrors
```
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

SUBSTRING Examples:
```
SELECT SUBSTRING(FirstName, 1, 3)
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/b120437d-718f-40c0-8c41-61fca70527ea)

```
SELECT SUBSTRING(FirstName, 3, 3)
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/19e973fb-eef7-4804-bca0-987a70553ae3)

```
SELECT err.FirstName, dem.FirstName
FROM EmployeeErrors err
JOIN EmployeeDemographics dem
  ON err.FirstName = dem.FirstName
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/d317a05f-7b64-4400-bc6a-20c5e496aea8)

Fuzzy Match with SUBSTRING Example:
```
SELECT err.FirstName, SUBSTRING(err.FirstName, 1, 3), dem.FirstName, SUBSTRING(dem.FirstName, 1, 3)
FROM EmployeeErrors err
JOIN EmployeeDemographics dem
  ON SUBSTRING(err.FirstName, 1, 3) = SUBSTRING(dem.FirstName, 1, 3)
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/5ff76497-ced8-4f3a-bb55-63865c224416)

LOWER Example:
```
SELECT FirstName, LOWER(FirstName)
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/f5e1a4c6-0da5-4cd7-b4fd-c7245e6e71ba)

UPPER Example:
```
SELECT FirstName, UPPER(FirstName)
FROM EmployeeErrors
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/9e310ca2-3d9c-4dc7-b985-3db7441b8834)
