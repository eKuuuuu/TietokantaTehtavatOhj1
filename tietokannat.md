### Tehtävä 1, 1
SHOW TABLES;
### Näyttää "5 rows"


### Tehtävä 1, 2
SHOW columns FROM country;
### Näyttää "5 rows"

### Tehtävä 1, 3
SHOW columns FROM airport;
### Nähdään että ident key paikassa on "PRI"

### Yhteen tauluun kohdistuvien kyselyiden harjoitukset
### Tajusin vasta siis täällä miten nämä screenshotit toimivat
### Tehtävä 1
SELECT * FROM goal;
![img_1.png](img_1.png)

### Tehtävä 2
SELECT name airport_type from airport where iso_country = "FI";
![img_2.png](img_2.png)

### Tehtävä 3
SELECT name FROM airport WHERE iso_country = "FI" ORDER BY name;
![img_3.png](img_3.png)

### Tehtävä 4
SELECT name, TYPE FROM airport WHERE iso_country = "FI" ORDER BY TYPE, name;
![img_4.png](img_4.png)

### Tehtävä 5
SELECT name FROM country WHERE name like "F%";
![img_5.png](img_5.png)

### Tehtävä 6
SELECT name FROM country WHERE name like "%F%";
![img_6.png](img_6.png)

### Tehtävä 7
SELECT location FROM game WHERE screen_name = "Vesa";
![img_7.png](img_7.png)

### Tehtävä 8
SELECT co2_consumed FROM game WHERE screen_name = "Ilkka";
![img_8.png](img_8.png)

### Tehtävä 9
SELECT distinct co2_budget FROM game;
![img_9.png](img_9.png)

### Where-osan liitosehto harjoitukset

### Tehtävä 1
SELECT country.name AS "country name", airport.name AS "airport name" FROM airport, country WHERE airport.iso_country = country.iso_country and country.name = "Iceland";
![img_10.png](img_10.png)

### Tehtävä 2
SELECT airport.name as "airport name" FROM airport, country WHERE airport.iso_country = country.iso_country AND country.name = "France" AND airport.type = "large_airport";
![img_11.png](img_11.png)

### Tehtävä 3
select country.name as country_name, airport.name as airport_name from airport, country where airport.iso_country = country.iso_country and country.continent = "AN";
![img_12.png](img_12.png)

### Tehtävä 4
SELECT elevation_FT from airport, game where location = ident and screen_name = "Heini";
![img_13.png](img_13.png)

### Tehtävä 5
SELECT elevation_FT * 0.3048 as elevation_m from airport, game where location = ident and screen_name = "Heini";
![img_14.png](img_14.png)

### Tehtävä 6
SELECT name from airport, game where location = ident and screen_name = "Ilkka";
![img_15.png](img_15.png)

### Tehtävä 7
select country.name from airport, game, country where location = ident and airport.iso_country = country.iso_country  and screen_name = "Ilkka";
![img_16.png](img_16.png)

### Join osio

### Tehtävä 1
SELECT country.name AS "country name", airport.name AS "airport.name" FROM country inner JOIN airport ON airport.iso_country = country.iso_country WHERE country.name = "Finland" and scheduled_service = "yes";
![img_17.png](img_17.png)

### Tehtävä 2
SELECT screen_name, airport.name FROM game inner JOIN airport on location = ident;
![img_18.png](img_18.png)

### Tehtävä 3
SELECT screen_name, country.name FROM game inner JOIN airport on location = ident inner JOIN country ON airport.iso_country = country.iso_country;
![img_19.png](img_19.png)

### Tehtävä 4
SELECT airport.name, screen_name FROM airport left JOIN game on ident = location where name like "%Hels%";
![img_20.png](img_20.png)

### Tehtävä 5
SELECT name, screen_name FROM goal LEFT JOIN goal_reached ON goal.id = goal_id LEFT JOIN game ON game.id = game_id;
![img_21.png](img_21.png)

