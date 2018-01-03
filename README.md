![Bitmaker](https://github.com/johncarlolopez/bitmaker-reference/blob/master/bitmakerlogo.svg)
# 02 - Data Modelling: 1 to Many
### Wednesday, Jan 3rd

Part 1
This part focuses on designing database structures to support 1-many relationships. Your task is to design (diagram) a database structure to store the data and relationships for each of the following data sets.

Think about what data type each column should be, as well as any additional columns you will need to store the relationships described.

If you use paper to do this assignment, you can take a photo of your drawing, upload that to github, and submit it.

If you prefer to use software, you can try http://asciiflow.com/.

Customers with orders customer_order
People with addresses person_residence_city_province_country
A library system library_system
Ask an instructor to look over your answers before moving on to Part 2 to make sure you're on the right track.*
Part 2
This part is about identifying 1-many relationships between classes.

For each of the following:

create a relationship diagram between the given set of classes similar to the diagrams provided in Part 1
design the database structure to support them like you did in Part 1
You can choose to use either paper or software for these tasks.

1.

actor
role
play
director
2.

breed
pet
veterinarian appointment
veterinarian
animal clinic
pet owner
3.

restaurant
review
food critic
publication
chef

Ask an instructor to look over your answers before moving on to Part 3 to make sure you're on the right track.*
Part 3
In this part you will be given just the concept of an app and you will have to design the classes, relationships, and database structure for it. You can keep things relatively simple and aim for somewhere around 2-5 classes per app.

A forum where people can post messages on different threads.

An app for a dentist office to keep track of appointments.

An Eventbrite-style app where people can sell tickets to events they're hosting, or buy tickets to other people's events.

Now would be a good time to discuss your solutions with an instructor.

Part 4
This part will give you practice writing SQL queries to retrieve data according to "one to many" relationships that exist in the schema.

Getting started
Fork this repository and cd into the directory.
Create an empty database:
createdb one_to_many_assignment
Load the data from data.sql into the database you just made:
psql one_to_many_assignment < data.sql
Open the psql console fo this database:
psql one_to_many_assignment
Exercises
The data in this part of the assignment uses the authors, articles, countries, provinces, cities, residences, and persons tables from earlier in the assignment.

Write SQL queries (in as many steps as necessary) to solve each of the following:

Find the author with the name 'Kara Melton' and then select all the articles she has written.
Find Ontario in the provinces table and then find all the cities in that province.
Who wrote the article called 'Coding Bootcamps and Emotional Labor'?
Write a series of SQL queries to find out how many provinces are in Canada.
How many people live at 4740 McDermott Street?
What city is 4740 McDermott Street in?
What province is 4740 McDermott Street in?
What country is 4740 McDermott Street in?
Find the person named 'Destini Davis' and then use a series of SQL queries to find what country they live in.
How many articles has Aditya Mukerjee written?
