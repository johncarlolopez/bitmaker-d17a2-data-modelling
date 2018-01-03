In this part you will be given just the concept of an app and you will have to design the classes, relationships, and database structure for it. You can keep things relatively simple and aim for somewhere around 2-5 classes per app.

1. A forum where people can post messages on different threads.
  * User
    * id(integer)
    * name(string)
  * Thread
    * id(integer)
    * name(string)
    * message(text)
    * user_id(foreign key)
  * Message
    * id(integer)
    * message(text)
    * thread_id(integer)(foreign key)
    * user_id(integer)(foreign key)

User (one) - (many) Threads
User (one) - (many) Messages
Thread (one) - (many) Messages

each database will require it's own class

2. An app for a dentist office to keep track of appointments.

  * Dentist
    * id(integer)
    * name(string)
    * clinic_id(integer)(foreign key)
  * Patient
    * id(integer)
    * name(string)
    * clinic_id(integer)(foreign key)
  * Work
    * id(integer)
    * name(string)
    * patient_id(integer)(foreign key)
    * dentist_id(integer)(foreign key)
    * clinic_id(integer)(foreign key)
    * date(string)
    * time(string)
  * Clinic
    * id(integer)
    * name(string)

Dentist (one) - (many) work
Clinic (one) - (many) dentists
Clinic (one) - (many) patients
Clinic (one) - (many) work
Patient (one) - (many) work

each database will require it's own class

3. An Eventbrite-style app where people can sell tickets to events they're hosting, or buy tickets to other people's events.

  * User
    * id(integer)
    * name(string)
  * Ticket
    * id(integer)
    * buyer_id(integer)(foreign key)
    * event_id(integer)(foreign key)
    * price(float)
  * Event
    * id(integer)
    * name(string)
    * user_id "organizer" (integer)(foreign key)

Users (many) - (many) Tickets  // buying
User (one) - (many) Tickets // selling
User (one) - (many) Events // one user can hold many events
Event (one) - (many) Tickets

Now would be a good time to discuss your solutions with an instructor.
