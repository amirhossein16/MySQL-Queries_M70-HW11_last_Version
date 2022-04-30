# MySQL-Queries_M70-HW11_last_Version
MySQL-Queries_M70-HW11_last_Version

## 1. Revising the Select Query I

```sql
SELECT NAME FROM CITY WHERE COUNTRYCODE = 'USA' AND POPULATION >= 120000;
```

<p align="center">
  <img width="460" height="300" src="https://github.com/amirhossein16/MySQL-Queries_M70-HW11_last_Version/blob/ce9b238a2119dcfc8a04d6c24cea6a55c91157ea/Section-1/revising-the-select-query-2-problem.png">
</p>

![Revising the Select Query I](Section-1/revising-the-select-query-2-problem.png)

## 2. Revising the Select Query II

```sql
SELECT * FROM CITY WHERE POPULATION > 100000 AND COUNTRYCODE = 'USA';
```

![Revising the Select Query II](Section-1/revising-the-select-query-problem.png)

## 3. Select All

```sql
SELECT * FROM CITY;
```

![Select All](Section-1/select-all-sql-problem.png)

## 4. Select By ID

```sql
SELECT * FROM CITY WHERE ID = 1661;
```

![Select By ID](Section-1/select-by-id-problem.png)

# Section 2

## 1. Weather Observation Station 3

```sql
SELECT NAME FROM EMPLOYEE
ORDER BY NAME;
```

![Weather Observation Station 3](Section-2/name-of-employees-problem.png)


## 2. Employee Names

```sql
SELECT NAME FROM EMPLOYEE
WHERE SALARY > 2000
AND MONTHS < 10
ORDER BY EMPLOYEE_ID;
```

![Employee Names](Section-2/salary-of-employees-problem.png)

## 3. Employee Salaries

```sql
SELECT DISTINCT(CITY) FROM STATION
WHERE (ID % 2 ) = 0;
```

![Employee Salaries](Section-2/weather-observation-station-3-problem.png)


# Section 3

## 1. Revising Aggregations - The Count Function

```sql
SELECT FLOOR(AVG(POPULATION)) FROM CITY;
```

![Revising Aggregations - The Count Function](Section-2/average-population-problem.png)

## 2. Revising Aggregations - The Sum Function

```sql
SELECT SUM(POPULATION) FROM CITY
WHERE DISTRICT = 'California';
```

![Revising Aggregations - The Sum Function](Section-3/revising-aggregations-sum-problem.png)


## 3. Revising Aggregations - Averages

```sql
SELECT AVG(POPULATION) FROM CITY
WHERE DISTRICT = 'California';
```

![Revising Aggregations - Averages](Section-1/revising-aggregations-the-average-function-problem.png)

## 4. Average Population

```sql
SELECT COUNT(*) FROM CITY
WHERE POPULATION > 100000;
```

![Average Population](Section-1/revising-aggregations-the-count-function-problem.png)

## 5. Population Density Difference

```sql
SELECT MAX(POPULATION) - MIN(POPULATION) FROM CITY;
```

![Population Density Difference](Section-1/population-density-difference-problem.png)


# Section 4

## 1. African Cities

```sql
SELECT CITY.NAME FROM CITY
INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Africa';
```

![African Cities](Section-4/african-cities-problem.png)

## 2. Population Census

```sql
SELECT SUM(CITY.POPUALTION) FROM CITY
INNER JOIN COUNTRY ON CITY.COUNTRYCODE = COUNTRY.CODE
WHERE COUNTRY.CONTINENT = 'Asia';
```

![Population Census](Section-4/asian-population-problem.png)

## 3. Average Population of Each Continent

```sql
SELECT COUNTRY.CONTINENT, FLOOR(AVG(CITY.POPULATION))
FROM COUNTRY, CITY
WHERE COUNTRY.CODE = CITY.COUNTRYCODE
GROUP BY COUNTRY.CONTINENT;
```

![Average Population of Each Continent](Section-4/average-population-of-each-continent-problem.png)
