- As a customer, so I can receive my tickets, I want to provide my contact information.
- As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
- As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.

Epic
A local cinema wants to allow people to book tickets online to see movies that are being shown in its various screens. These tickets should be delivered to customers via email. The cinema wants to keep a record of their customers and the tickets they purchase, as well as offer a regularly updated list of movies for them to choose from. A single screen might show multiple movies a day, and even the same movie at multiple times. The cinema will expand its number of screens in the future, so the potential for growth needs to be accounted for.

Additional User Stories:
- As a customer, so I can select my preferred showtime, I want to see the schedule of movie timings for each screen.

- As a customer, so I can easily find information about a movie, I want to view details like genre, duration etc.

- As a customer, so I can choose the best seats, I want to see the seating layout for each screen.

- As a customer, so I can plan my visit, I want to view the cinema's location and available parking spaces.

- As a customer, so I can track my ticket purchases, I want to see a history of my past bookings.


Brainstorming: 

Domain Entities:
/*About individuals who book tickets.*/
Customer:
id
createdAt
updatedAt
Name
Email
Contact Number

/*Represents the movies being shown at the cinema.*/
Movie:
id
createdAt
updatedAt
Title
Genre
Duration

/*Represents the screens in the cinema where movies are   screened.*/

Screen:
id
createdAt
updatedAt
Screen Number

/*Represents the specific timing of a movie on a particular screen.*/

Showtime

id
createdAt
updatedAt
Date
Time
Movie (foreign key to Movie)
Screen (foreign key to Screen)

/*Represents the tickets purchased by customers for specific showtimes.*/
Ticket

id
createdAt
updatedAt
Customer (foreign key to Customer)
Showtime (foreign key to Showtime)
Seat Number

/*Represents the physical location of the cinema.*/
CinemaLocation

id
createdAt
updatedAt
Location Name
Address
Available Parking Spaces

Relationships:

Customer and Ticket: 
- relationship type:  One-to-Many
- Each customer can purchase multiple tickets, but each ticket belongs to only one customer.
- Foreign Key: CustomerId in the Ticket table references the id column in the Customer table.


Movie and Showtime:
- relationship Type: One-to-Many
- Each movie can have multiple showtimes, but each showtime belongs to only one movie.
- Foreign Key: MovieId in the Showtime table references the id column in the Movie table.

Screen and Showtime:
- relationship Type: One-to-Many
-  Each screen can have multiple showtimes, but each showtime belongs to only one screen.
- Foreign Key: ScreenId in the Showtime table references the id column in the Screen table.

Showtime and Ticket:
- relationship Type: One-to-Many
- Each showtime can have multiple tickets sold, but each ticket belongs to only one showtime.
- Foreign Key: ShowtimeId in the Ticket table references the id column in the Showtime table.

CinemaLocation and Screen:
- relationship Type: One-to-One (assuming each screen is located in a single cinema location)
- Each screen is located in one specific cinema location.
- Foreign Key: LocationId in the Screen table references the id column in the CinemaLocation table.
