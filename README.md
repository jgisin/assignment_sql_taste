# assignment_sql_taste
A delicious appetizer of SQL-ey goodness

Jeff's Assignment

## Queries

### Example

```
SELECT *
  FROM tutorial.us_housing_units
  WHERE month = 1
```

#tutorial.us_housing_units

##1
```
SELECT *
  FROM tutorial.us_housing_units 
LIMIT 10
```
##2
```
SELECT midwest
FROM tutorial.us_housing_units 
```
##3
```
SELECT *
FROM tutorial.us_housing_units
WHERE year >= 1985
```
##4
```
SELECT *
FROM tutorial.us_housing_units
WHERE year >= 1990 AND month > 6
```
##5
```
SELECT south
FROM tutorial.us_housing_units
WHERE south > 30
```
##6
```
SELECT south + west + midwest + northeast AS "SUM"
FROM tutorial.us_housing_units
```
##7
```
SELECT south + west + midwest + northeast AS sum
FROM tutorial.us_housing_units
WHERE south + west + midwest + northeast > 70
```
##8
```
SELECT south + west + midwest + northeast AS sum
FROM tutorial.us_housing_units
WHERE south + west + midwest + northeast BETWEEN 50 AND 80
```
##9
```
SELECT (south + west + midwest + northeast) / 4 AS "AVG"
FROM tutorial.us_housing_units
```
##10
```
SELECT south,
       west + midwest + northeast AS "Other Sum"
FROM tutorial.us_housing_units
WHERE west + midwest + northeast < south
```
##11
```
SELECT south / (south + west + midwest + northeast) * 100 AS "SOUTH PERC",
       west / (south + west + midwest + northeast) * 100 AS "WEST PERC",
       midwest / (south + west + midwest + northeast) * 100 AS "MIDWEST PERC",
       northeast / (south + west + midwest + northeast) * 100 AS "NORTHEAST PERC"
FROM tutorial.us_housing_units
WHERE year >= 1990
```