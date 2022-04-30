# MySQL-Queries_M70-HW11_last_Version
MySQL-Queries_M70-HW11_last_Version

## 1. Revising the Select Query I

```sql
SELECT NAME FROM CITY WHERE COUNTRYCODE = 'USA' AND POPULATION >= 120000;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/ce9b238a2119dcfc8a04d6c24cea6a55c91157ea/Section-1/revising-the-select-query-2-problem.png">
</p>

## 2. Revising the Select Query II

```sql
SELECT * FROM CITY WHERE POPULATION > 100000 AND COUNTRYCODE = 'USA';
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-1/revising-the-select-query-problem.png">
</p>

## 3. Select All

```sql
SELECT * FROM CITY;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-1/select-all-sql-problem.png">
</p>

## 4. Select By ID

```sql
SELECT * FROM CITY WHERE ID = 1661;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-1/select-by-id-problem.png">
</p>

# Section 2

## 1. Employee Names

```sql
SELECT NAME FROM EMPLOYEE
ORDER BY NAME;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-2/name-of-employees-problem.png">
</p>

## 2. Employee Salaries

```sql
SELECT NAME FROM EMPLOYEE
WHERE SALARY > 2000
AND MONTHS < 10
ORDER BY EMPLOYEE_ID;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-2/salary-of-employees-problem.png">
</p>

## 3. Weather Observation Station 3

```sql
SELECT DISTINCT(CITY) FROM STATION
WHERE (ID % 2 ) = 0;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-2/weather-observation-station-3-problem.png">
</p>


# Section 3

## 1. Average Population

```sql
SELECT FLOOR(AVG(POPULATION)) FROM CITY;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-3/average-population-problem.png">
</p>

## 2. Revising Aggregations - The Sum Function

```sql
SELECT SUM(POPULATION) FROM CITY
WHERE DISTRICT = 'California';
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-3/revising-aggregations-sum-problem.png">
</p>


## 3. Revising Aggregations - Averages

```sql
SELECT AVG(POPULATION) FROM CITY
WHERE DISTRICT = 'California';
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-3/revising-aggregations-the-average-function-problem.png">
</p>

## 4. Revising Aggregations - The Count Function

```sql
SELECT COUNT(*) FROM CITY
WHERE POPULATION > 100000;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-3/revising-aggregations-the-count-function-problem.png">
</p>

## 5. Population Density Difference

```sql
SELECT MAX(POPULATION) - MIN(POPULATION) FROM CITY;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-3/population-density-difference-problem.png">
</p>

# Section 4

## 1. African Cities

```sql
SELECT CITY.NAME FROM CITY
INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Africa';
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-4/african-cities-problem.png">
</p>

## 2. Population Census

```sql
SELECT SUM(CITY.POPUALTION) FROM CITY
INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Asia';
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-4/asian-population-problem.png">
</p>

## 3. Average Population of Each Continent

```sql
SELECT COUNTRY.CONTINENT, FLOOR(AVG(CITY.POPULATION))
FROM COUNTRY, CITY
WHERE COUNTRY.CODE = CITY.COUNTRYCODE
GROUP BY COUNTRY.CONTINENT;
```

<p align="center">
  <img width="100%" height="100%" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/a15e43f6a9b7c10eee4c2eb7a857804e88f900a3/Section-4/average-population-of-each-continent-problem.png">
</p>
