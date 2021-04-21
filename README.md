# MySQL-database-querying1

Task 1: 
SELECT movies.title from movies

Task2: 
select movies.title, movies.year_released
from movies order by year_released desc

Task 3:
select directors.director_id, directors.first_name, directors.last_name, directors.country
from directors order by country asc

Task 4 :
select directors.director_id, directors.first_name, directors.last_name, directors.country
from directors order by last_name, country asc

Task 5:
insert into directors (director_id, first_name, last_name, country)
value(11, "Rob", "Reiner", "USA")

Task 6:
select directors.director_id, directors.last_name
from directors where director_id = 11 and last_name = "Reiner"

Task 7 :
insert into movies ( title, year_released, director_id)
value("Princess Bride", 1987, 11)

Task 8:
select movies.title, movies.year_released, directors.last_name
from movies inner join directors on movies.director_id = directors.director_id

Task 9 :
select movies.title, movies.year_released, directors.first_name, directors.last_name
from movies inner join directors on movies.director_id = directors.director_id
order by last_name asc

Task 10 :
select directors.first_name, directors.last_name
from movies inner join directors on movies.director_id = directors.director_id
where title = "The Incredibles"

Task 11 :
select directors.last_name, directors.country
from movies inner join directors on movies.director_id = directors.director_id
where title = "Roma"

Task 12:
delete from movies
where movies_id = 6

Task 13:
delete from directors
where director_id = 4
result =  cannot delete or update a parent row : a foreign key constraint fails

Task 14 :
select movies.movies_id as movies_items, movies.title as movies_name, directors.country as nation
from movies inner join directors on movies.director_id = directors.director_id

Task 15:
select movies.movies_id, movies.title, movies.year_released, directors.last_name 
from movies inner join directors on movies.director_id = directors.director_id
where directors.director_id = 7

Task 16 :
alter table movies
add earnings integer

update movies
set earnings = 76000 
where movies.movies_id = 1
set earnings = 32070 
where movies.movies_id = 2
set earnings = 445000 
where movies.movies_id = 3
set earnings = 95000 
where movies.movies_id = 4
set earnings = 5000 
where movies.movies_id = 5
set earnings = 12540 
where movies.movies_id = 6
set earnings = 40900 
where movies.movies_id = 7
set earnings = 102300 
where movies.movies_id = 8 
set earnings = 29300 
where movies.movies_id = 9
set earnings = 12100 
where movies.movies_id = 10
set earnings = 76500 
where movies.movies_id = 11
set earnings = 215700 
where movies.movies_id = 12
set earnings = 97000 
where movies.movies_id = 13
set earnings = 30740 
where movies.movies_id = 14
set earnings = 285700 
where movies.movies_id = 15
set earnings = 184000 
where movies.movies_id = 16
set earnings = 15090 
where movies.movies_id = 17

select movies.title
from movies inner join directors on movies.director_id = directors.director_id
order by earnings asc

select movies.title, movies.earnings
from movies inner join directors on movies.director_id = directors.director_id
where earnings >= 100000
