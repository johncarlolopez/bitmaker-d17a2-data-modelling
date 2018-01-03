Part 1
This part focuses on designing database structures to support 1* many relationships. Your task is to design (diagram) a database structure to store the data and relationships for each of the following data sets.

Think about what data type each column should be, as well as any additional columns you will need to store the relationships described.

If you use paper to do this assignment, you can take a photo of your drawing, upload that to github, and submit it.

If you prefer to use software, you can try http://asciiflow.com/.

1. Customers with orders customer_order
  * Customer
    * id(integer)
    * name(string)
    * mailing_address(string)
    * email(string)
  * Order
    * id(integer)
    * date(string)
    * customer_id(integer)(foreign key)
2. People with addresses
  * Person
    * id(integer)
    * name(string)
    * age(integer)
    * residence_id(integer)(foreign key)
  * Residence
    * id(integer)
    * address(string)
    * year(integer)
    * city_id(integer)(foreign key)
  * City
    * id(integer)
    * name(string)
    * year_founded(integer)
    * province_id(integer)(foreign key)
  * Province
    * id(integer)
    * name(string)
    * year_founded(integer)
    * country_id(integer)(foreign key)
  * Country
    * id(integer)
    * name(string)
    * year_founded(integer)
    * national_animal(string)
3. A library system library_system
  * Author
    * id(integer)
    * name(string)
  * Book
    * id(integer)
    * title(string)
    * isbn(integer)
    * author_id(integer)
  * Hold
    * id(integer)
    * date_placed(string)
    * book_id(integer)(foreign key)
    * patron_id(integer)(foreign key)
  * Patron
    * id(integer)
    * name(string)
    * card_number(integer)
    * email(string)
  * Loan
    * id(integer)
    * due_date(string)
    * renewed(boolean)
    * book_id(integer)(foreign key)
    * patron_id(integer)(foreign key)

Ask an instructor to look over your answers before moving on to Part 2 to make sure you're on the right track.*

WORK CHECKED BY Najwa Azer @ 3 PM
