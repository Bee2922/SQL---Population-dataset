SQL-Population-dataset
--View the entire table 
SELECT * FROM dbo.[World Population by country 2024]

--View the population of all countries in 2023 and 2024 and their growth rate
SELECT country, [population 2023], [Population 2024], [Growth Rate] FROM  dbo.[World Population by country 2024]

--DROP AREA COLUMN
ALTER TABLE dbo.[World Population by country 2024]
DROP COLUMN [Area (km2)]

SELECT * FROM dbo.[World Population by country 2024]

-- View country with growth rate greater than .022
SELECT Country, [population 2024], [World %] FROM dbo.[World Population by country 2024]
WHERE [Growth Rate] > 0.022

--Find the country with the highest population in 2023
SELECT MAX([population 2023]) FROM dbo.[World Population by country 2024]

--Find the country with the lowest population in 2024
SELECT MIN([population 2024]) FROM dbo.[World Population by country 2024]

--View countries with less than or equal to .002 growth rate in descending order
SELECT country FROM dbo.[World Population by country 2024]
WHERE [Growth Rate] <= .002
ORDER BY country DESC

--View countries whose names contains A in descending order
SELECT * FROM dbo.[World Population by country 2024]
WHERE country LIKE '%A%'
ORDER BY country DESC

--View countries whose names begins with B
SELECT * FROM dbo.[World Population by country 2024]
WHERE country LIKE 'B%'
ORDER BY country
