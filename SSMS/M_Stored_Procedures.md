
This section covers Stored Procedures.

A Stored Procedure is a prepared SQL code that you can save, so the code can be 
reused over and over again. This is often used if a developer believes they will 
be using the code again in the future and they can just call the procedure
instead of rewriting.

Creating Stored Procedure Example:
```
CREATE PROCEDURE TEST
AS
SELECT *
FROM EmployeeDemographics;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/a8f99afa-e23a-40b2-af7c-345551097cd0)

Executing Stored Procedure Example:
```
EXEC TEST;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/0987b0e6-dff0-40d6-a83d-0cb4ba178477)
