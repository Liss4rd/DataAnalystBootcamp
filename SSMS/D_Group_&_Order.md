
This section covers GROUP BY and ORDER BY clauses.

```
SELECT Gender
FROM EmployeeDemographics
GROUP BY Gender
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/8fba6305-2569-4262-8571-5c512b023c46)


```
SELECT Gender, COUNT(Gender)
FROM EmployeeDemographics
GROUP BY Gender
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/726e2775-9ada-450b-a564-f40f8596a0d1)

The below example is not ideal for a COUNT, but shows the functionality of the GROUP BY clause:
```
SELECT Gender, Age, COUNT(Gender)
FROM EmployeeDemographics
GROUP BY Gender, Age
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/8105538c-5ebb-4af6-a7da-c74e2555948b)

```
SELECT Gender, COUNT(Gender) AS CountGender
FROM EmployeeDemographics
WHERE Age > 31
GROUP BY Gender
ORDER BY CountGender ASC
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/c589e287-a336-4b3b-a1c3-b62d7fc90cf3)

```
SELECT Gender, COUNT(Gender) AS CountGender
FROM EmployeeDemographics
WHERE Age > 31
GROUP BY Gender
ORDER BY CountGender DESC;
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/174455d4-c6e1-4224-9777-4c0e599be52e)

```
SELECT *
FROM EmployeeDemographics
ORDER BY Age ASC
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/2d2e0366-5fa9-4e95-8a66-7d1f25381c8e)

```
SELECT *
FROM EmployeeDemographics
ORDER BY Age, Gender DESC
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/3758beca-cd0e-4365-9af1-99dff91652f9)

ORDER BY with a following digit refers to the column number:
```
SELECT *
FROM EmployeeDemographics
ORDER BY 2 ASC
```
![image](https://github.com/Liss4rd/DataAnalystBootcamp/assets/66858250/8bd05111-465f-4e66-960a-ac3dab9e4ebb)
