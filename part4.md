# Exercises
___
The data in this part of the assignment uses the authors, articles, countries, provinces, cities, residences, and persons tables from earlier in the assignment.

Write SQL queries (in as many steps as necessary) to solve each of the following:

1. Find the author with the name 'Kara Melton' and then select all the articles she has written.
```
Select * from articles where author_id = (Select id from authors where name = 'Kara Melton');

OR (using join)

Select articles.title as "Article name", authors.name as "Author name" from articles, authors where articles.author_id = authors.id AND name = 'Kara Melton';
```
2. Find Ontario in the provinces table and then find all the cities in that province.
```
Select * from cities where province_id = (Select id from provinces where name = 'Ontario');
```
3. Who wrote the article called 'Coding Bootcamps and Emotional Labor'?
```
Select name from authors where id = (Select author_id from articles where title = 'Coding Bootcamps and Emotional Labor');
```
4. Write a series of SQL queries to find out how many provinces are in Canada.
```
Select COUNT(*) from provinces;
```
5. How many people live at 4740 McDermott Street?
```
Select COUNT(*) from persons where residence_id = (Select id from residences where address = '4740 McDermott Street');
```
6. What city is 4740 McDermott Street in?
```
Select name from cities where id = (Select city_id from residences where address = '4740 McDermott Street');
```
7. What province is 4740 McDermott Street in?
```
Select name from provinces where id =
(Select province_id from cities where id = (Select city_id from residences where address = '4740 McDermott Street'));

OR (using join)

Select provinces.name from provinces, cities, residences where residences.city_id = cities.id AND cities.province_id = provinces.id AND residences.address = '4740 McDermott Street';
```
8. What country is 4740 McDermott Street in?
```
Select countries.name from countries, provinces, cities, residences where residences.city_id = cities.id AND cities.province_id = provinces.id AND provinces.country_id = countries.id AND residences.address = '4740 McDermott Street';
```
9. Find the person named 'Destini Davis' and then use a series of SQL queries to find what country they live in.
```
Select countries.name as "Country", persons.name as "Person" From countries, provinces, cities, residences,  persons Where   persons.residence_id = residences.id AND residences.city_id = cities.id AND cities.province_id = provinces.id AND provinces.country_id = countries.id AND persons.name = 'Destini Davis';
```
10. How many articles has Aditya Mukerjee written?
```
Select COUNT(*) from articles where author_id = (Select id from authors where name = 'Aditya Mukerjee');
```
