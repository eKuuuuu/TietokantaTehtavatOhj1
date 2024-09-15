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

