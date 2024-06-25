# EPIC -> USER STORIES

## EPIC

A local cinema wants to allow people to book tickets online to see movies that are being shown in its various screens. These tickets should be delivered to customers via email. The cinema wants to keep a record of their customers and the tickets they purchase, as well as offer a regularly updated list of movies for them to choose from. A single screen might show multiple movies a day, and even the same movie at multiple times. The cinema will expand its number of screens in the future, so the potential for growth needs to be accounted for.

## KEYWORDS

### entities

- tickets
- cinema
- screens
- movies
- email
- customers

### actions

- book
- see
- deliver
- keep a record
- update

## USER STORIES

### customer - making a booking

- As a customer, so I can receive my tickets, I want to provide my contact information.
- As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
- As a customer, so I pick a showing, I want see the dates and times at which each movie is shown.

### customer - going to the cinema

- As a customer, so I can go see a movie I have booked a seat for, I want to receive an email with my ticket.
- As a customer, so I know my booking has come through properly, I want my ticket to reference the title of the movie I picked.
- As a customer, so I can now to which room to go to, I want my ticket to reference the screen showing the movie I have booked.
- As a customer, so I can easily check when the movie is shown, I want my ticket to reference the date and time of the showing.
  
### admin - updating info

- As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.
- As an admin, so I can manage the cinema, I want to update the list of screens.

### admin - record keeping

- As an admin, so I can know how many people have used our services, I want to see a list of all the customers we have had.
- As an admin, so I can track customer behavior, I want to see a list of all tickets that we have sold grouped by customer.
- As an admin, so I can track sales, I want to see a list of all tickets that we have sold.
  