
More Queries 

## Task 0: My privileges!

```   
# Script to list privileges of MySQL users user_0d_1 and user_0d_2
mysql -u root -p -e "SHOW GRANTS FOR 'user_0d_1'@'localhost'; SHOW GRANTS FOR 'user_0d_2'@'localhost';"
Task 1: Root user
     
# Script to create MySQL server user user_0d_1
mysql -u root -p -e "CREATE USER 'user_0d_1'@'localhost' IDENTIFIED BY 'user_0d_1_pwd'; GRANT ALL PRIVILEGES ON *.* TO 'user_0d_1'@'localhost' WITH GRANT OPTION;"
Task 2: Read user
   
# Script to create database hbtn_0d_2 and user user_0d_2
mysql -u root -p -e "CREATE DATABASE IF NOT EXISTS hbtn_0d_2; CREATE USER IF NOT EXISTS 'user_0d_2'@'localhost' IDENTIFIED BY 'user_0d_2_pwd'; GRANT SELECT ON hbtn_0d_2.* TO 'user_0d_2'@'localhost';"
Task 3: Always a name
   
     
# Script to create table force_name
mysql -u root -p -e "USE <database_name>; CREATE TABLE IF NOT EXISTS force_name (id INT, name VARCHAR(256) NOT NULL);"
Task 4: ID can't be null
   
     
# Script to create table id_not_null
mysql -u root -p -e "USE <database_name>; CREATE TABLE IF NOT EXISTS id_not_null (id INT DEFAULT 1, name VARCHAR(256));"
Task 5: Unique ID     
# Script to create table unique_id
mysql -u root -p -e "USE <database_name>; CREATE TABLE IF NOT EXISTS unique_id (id INT DEFAULT 1 UNIQUE, name VARCHAR(256));"
Task 6: States table     
# Script to create database hbtn_0d_usa and table states
mysql -u root -p -e "CREATE DATABASE IF NOT EXISTS hbtn_0d_usa; USE hbtn_0d_usa; CREATE TABLE IF NOT EXISTS states (id INT PRIMARY KEY AUTO_INCREMENT NOT NULL, name VARCHAR(256) NOT NULL);"
Task 7: Cities table
   
     
# Script to create database hbtn_0d_usa and table cities
mysql -u root -p -e "CREATE DATABASE IF NOT EXISTS hbtn_0d_usa; USE hbtn_0d_usa; CREATE TABLE IF NOT EXISTS cities (id INT PRIMARY KEY AUTO_INCREMENT NOT NULL, state_id INT NOT NULL, name VARCHAR(256) NOT NULL, FOREIGN KEY (state_id) REFERENCES states(id));"
Task 8: Cities of California     
# Script to list all cities of California
mysql -u root -p -e "USE hbtn_0d_usa; SELECT cities.id, cities.name FROM cities, states WHERE cities.state_id = states.id AND states.name = 'California' ORDER BY cities.id;"
Task 9: Cities by States    
# Script to list all cities by states
mysql -u root -p -e "USE hbtn_0d_usa; SELECT cities.id, cities.name, states.name FROM cities, states WHERE cities.state_id = states.id ORDER BY cities.id;"
Task 11: Genre ID for all shows    
# Import the database dump before running this script
# Script to list all shows and their genre IDs
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_shows.title, tv_show_genres.genre_id FROM tv_shows LEFT JOIN tv_show_genres ON tv_shows.id = tv_show_genres.show_id ORDER BY tv_shows.title, tv_show_genres.genre_id;"
Task 12: No genre  
# Import the database dump before running this script
# Script to list shows without a genre linked
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_shows.title, tv_show_genres.genre_id FROM tv_shows LEFT JOIN tv_show_genres ON tv_shows.id = tv_show_genres.show_id WHERE tv_show_genres.genre_id IS NULL ORDER BY tv_shows.title, tv_show_genres.genre_id;"
Task 13: Number of shows by genre    
# Import the database dump before running this script
# Script to list genres and the number of shows linked to each
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_genres.name AS genre, COUNT(tv_show_genres.show_id) AS number_of_shows FROM tv_genres LEFT JOIN tv_show_genres ON tv_genres.id = tv_show_genres.genre_id GROUP BY tv_genres.id ORDER BY number_of_shows DESC;"
Task 14: My genres    
# Import the database dump before running this script
# Script to list all genres of the show Dexter
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_genres.name FROM tv_shows LEFT JOIN tv_show_genres ON tv_shows.id = tv_show_genres.show_id LEFT JOIN tv_genres ON tv_show_genres.genre_id = tv_genres.id WHERE tv_shows.title = 'Dexter' ORDER BY tv_genres.name;"
Task 15: Only Comedy   
# Import the database dump before running this script
# Script to list all Comedy shows
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_shows.title FROM tv_genres, tv_shows LEFT JOIN tv_show_genres ON tv_shows.id = tv_show_genres.show_id WHERE tv_genres.name = 'Comedy' AND tv_show_genres.genre_id = tv_genres.id ORDER BY tv_shows.title;"
Task 16: List shows and genres    
# Import the database dump before running this script
# Script to list all shows and linked genres
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_shows.title, tv_genres.name FROM tv_shows LEFT JOIN tv_show_genres ON tv_shows.id = tv_show_genres.show_id LEFT JOIN tv_genres ON tv_show_genres.genre_id = tv_genres.id ORDER BY tv_shows.title, tv_genres.name;"
Task 17: Not my genre (Advanced)    
# Import the database dump before running this script
# Script to list genres not linked to the show Dexter
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_genres.name FROM tv_genres WHERE tv_genres.id NOT IN (SELECT tv_show_genres.genre_id FROM tv_shows LEFT JOIN tv_show_genres ON tv_shows.id = tv_show_genres.show_id WHERE tv_shows.title = 'Dexter') ORDER BY tv_genres.name;"
Task 18: No Comedy tonight! (Advanced)    
# Import the database dump before running this script
# Script to list shows without the Comedy genre
mysql -u root -p -e "USE hbtn_0d_tvshows; SELECT tv_shows.title FROM tv_shows WHERE tv_shows.id NOT IN (SELECT tv_show_genres.show_id FROM tv_genres, tv_show_genres WHERE tv_genres.name = 'Comedy' AND tv_show_genres.genre_id = tv_genres.id) ORDER BY tv_shows.title;"
Task 19: Rotten tomatoes (Advanced)
# Import the database dump before running this script
# Script to list shows by their rating
mysql -u root -p -e "USE hbtn_0d_tvshows_rate; SELECT tv_shows.title, SUM(tv_shows_rate.rating) AS rating_sum FROM tv_shows LEFT JOIN tv_shows_rate ON tv_shows.id = tv_shows_rate.show_id GROUP BY tv_shows.id ORDER BY rating_sum DESC;"
Task 20: Best genre (Advanced)
      
    
# Import the database dump before running this script
# Script to list genres by their average rating
mysql -u root -p -e "USE hbtn_0d_tvshows_rate; SELECT tv_genres.name, AVG(tv_shows_rate.rating) AS rating_avg FROM tv_genres LEFT JOIN tv_show_genres ON tv_genres.id = tv_show_genres.genre_id LEFT JOIN tv_shows_rate ON tv_show_genres.show_id = tv_shows_rate.show_id GROUP BY tv_genres.id ORDER BY rating_avg DESC;"

