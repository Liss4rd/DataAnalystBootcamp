
This section includes WHERE Statements, =. <>, <, >, AND, OR, LIKE, NULL, NOT NULL, IN.

WHERE Clause narrows the search with a condition:
```
SELECT * 
FROM EmployeeDemographics
WHERE FirstName = 'Jim'
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/ea47ef59-5a37-4cd2-8b7c-0374cb3c116e)

```
SELECT * 
FROM EmployeeDemographics
WHERE FirstName <> 'Jim'
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/22f31281-0cd8-448b-aece-b0466cc2bb6d)

```
SELECT * 
FROM EmployeeDemographics
WHERE Age > 30
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/519c26d8-da12-47f3-8923-e3e6ce872013)

```
SELECT *
FROM EmployeeDemographics
WHERE Age < 32
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/320096e5-535f-41cb-ae91-598584f2b546)

```
SELECT *
FROM EmployeeDemographics
WHERE Age <= 32
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/46765d37-1de0-4008-96dd-b95a35bbb0ee)

```
SELECT *
FROM EmployeeDemographics
WHERE Age <= 32
AND Gender = 'Male'
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/6050c0a5-cd84-4937-905e-8e10f5970c26)

```
SELECT *
FROM EmployeeDemographics
WHERE Age <= 32
OR Gender = 'Male'
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/6e37eae7-14eb-4c08-b7b0-0026dbc24ddf)

```
SELECT *
FROM EmployeeDemographics
WHERE LastName LIKE 'S%'
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/1a77110f-fb75-419d-a92e-f7c9e2fd4210)

```
SELECT *
FROM EmployeeDemographics
WHERE LastName LIKE '%S%'
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/3999c5a7-35c6-4702-9425-700fed0dedf0)

```
SELECT *
FROM EmployeeDemographics
WHERE FirstName IS NULL
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/313f0d13-2f6d-4960-9e8e-f88a79a395f6)

```
SELECT *
FROM EmployeeDemographics
WHERE FirstName IS NOT NULL
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/e77049ef-c6ab-4aa3-818c-601d11c1d0d5)

```
SELECT *
FROM EmployeeDemographics
WHERE FirstName IN ('Jim', 'Michael')
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/c8e4e2ea-f34f-4df9-a157-70f97844e846)
