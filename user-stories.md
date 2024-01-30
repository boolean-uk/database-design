A local cinema wants to allow people to book tickets online to see movies that are being shown in its various screens. These tickets should be delivered to customers via email. 
The cinema wants to keep a record of their customers and the tickets they purchase, as well as offer a regularly updated list of movies for them to choose from. 
A single screen might show multiple movies a day, and even the same movie at multiple times. 
The cinema will expand its number of screens in the future, so the potential for growth needs to be accounted for.

- As a customer, so I can receive my tickets, I want to provide contact information.
- As a customer, so I can surprise someone with tickets, I want to provide someone elses contact information.
- As a customer, so I can decide which screening I want to watch, I want to see a list of movies.
- As a customer, so that I can see where my screening is, I want to see which theater my move is playing in on my ticket.
- As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.
- As an admin, so I can understand what kind og movies pull customers and so that I can spam customers with recommendations, I want to keep record of what movies each customer watches.
- As an admin, so I can know when I need to expand, I want a record of how full each theater is at each screening.

Customer:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `ticket` one to many
    - `contactInfo`, one to one, copy from latest ticket
Ticket:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `screening`, one to one
    - `seat`, one to many
    - `contactInfo`, one to one
Contact information:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `name`, wich is a name
    - `email`, which is an email adress
Theater:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `screening`, one to many
    - `seat`, one to many, represents capacity
Screening:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `move`, one to one
    - `ticket`, one to many
    - `showTime`, which is the DateTime of sceening
Movie:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `name`, name of movie
    - `genre`, genere of movie
    - `duration`, int minutes of movie duration
Seat:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `rowNumber`, int 
    - `seatNumber`, int
    - `theater`, many to one
moveTable:
    - `id`, which is an auto-incrementing integer Primary Key
    - `createdAt`, which is a DateTime
    - `updatedAt`, which is a DateTime
    - `movie`, one to many





