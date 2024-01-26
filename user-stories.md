# Epic
A local cinema wants to allow people to book tickets online to see movies that are being shown in its various screens. These tickets should be delivered to customers via email. The cinema wants to keep a record of their customers and the tickets they purchase, as well as offer a regularly updated list of movies for them to choose from. A single screen might show multiple movies a day, and even the same movie at multiple times. The cinema will expand its number of screens in the future, so the potential for growth needs to be accounted for.

## User stories
- As a customer, so I can attend a movie, I want to purchase tickets online.

- As a customer, so I can keep a record of my booking, I want to receive a confirmation email with my ticket details.
    - As a customer, so I can receive my tickets, I want to provide my contact information.

- As a cinema employee, so I can keep track of sales, I want to record customer purchases and the tickets they buy.

- As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
    - As a customer, so I can choose a convenient time, I want to see different showtimes for each movie.
    - As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.

- As an admin, so I can accommodate more customers in the future, I want the system to support additional screens as they are added to the cinema.

## Domain etities
| Entity       | Attributes |
|-|-|
| Customer     | Customer ID, Ticket IDs, Email |
| Ticket       | Ticket ID, Showtime ID, Customer ID |
| Showtime     | Showtime ID, Movie ID, Screen ID, Start Time |
| Movie        | Movie ID, Public Movie ID |
| Screen       | Screen ID, Screen Name |
| Admin | Admin ID, email |