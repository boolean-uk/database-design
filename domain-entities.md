# Extracting user stories from the epic

1. As a customer, so I can receive my tickets, I want to provide my contact information.
2. As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
3. As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.
4. As a customer, so I can book tickets for a specific movie, I want to see the schedule of movies playing in a particular screen.
5. As a customer, so I can plan my visit, I want to know the available time slots for a specific movie.
6. As a customer, so I can reserve seats with my tickets, I want to view the seating arrangement for a particular screening.
7. As a customer, so I can attend with friends, I want to book multiple tickets in a single transaction.
8. As an admin, so I can track ticket sales, I want a record of each ticket purchase.
9. As a customer, so I can track my bookings, I want to see a history of my ticket purchases.
10. As a customer, so I can receive updates, I want to subscribe to a newsletter for upcoming movies and promotions.

# Extracting entities from user stories

1. Customers
   Attributes: id (PK), createdAt, updatedAt, name, email, phone

2. Contact
   Attributes: id (PK), createdAt, updatedAt, customerId (FK), address

3. Movies
   Attributes: id (PK), createdAt, updatedAt, title, genre, duration, releaseDate

4. Admin
   Attributes: id (PK), createdAt, updatedAt, name, email

5. Screen
   Attributes: id (PK), createdAt, updatedAt, name

6. Tickets
   Attributes: id (PK), createdAt, updatedAt, customerId (FK), movieId (FK), screenId (FK), scheduleId (FK), seatNumber

7. Schedule
   Attributes: id (PK), createdAt, updatedAt, movieId (FK), screenId (FK), timeSlotId (FK), date

8. Time Slot
   Attributes: id (PK), createdAt, updatedAt, startTime, endTime

9. Seating Arrangement
   Attributes: id (PK), createdAt, updatedAt, screenId (FK), seatNumber, isReserved

10. Transaction History
    Attributes: id (PK), createdAt, updatedAt, customerId (FK), ticketId (FK), transactionAmount, paymentMethod

11. Newsletter Subscription
    Attributes: id (PK), createdAt, updatedAt, customerId (FK), isSubscribed
