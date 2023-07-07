# DOMAIN ENTITIES

## ENTITIES

Movie => Represents a movie being shown at the cinema
Screen => Represents a screen in the cinema where movies are shown
Seat => Represents a seat in a specific screen that can be selected by a customer
ShowTime => Represents a specific time slot when a movie is scheduled to be shown on a screen
Ticket => Represents a ticket booked by a customer for a specific movie and showtime
Customer => Represents an individual who books movie tickets
Admin => Represents an administrator or staff member who manages the cinema's operations
Booking => Represents the booking made by a customer for one or more tickets
Payment => Represents the payment details and transaction information for a customer's ticket purchase.
Email => Represents the email sent to customers containing their tickets

## RELATIONSHIP

A Customer can have multiple Tickets (1-to-many relationship).
A Customer can have multiple Bookings (1-to-many relationship).
A Movie can have multiple Tickets (1-to-many relationship).
A Screen can have multiple Tickets (1-to-many relationship)
The relationship between a Showtime and a Movie is a many-to-one relationship.
The relationship between a Ticket and a Showtime is a many-to-one relationship.
The relationship between Showtime and Screen is a many-to-one relationship.
A Seat is associated with one Screen (many-to-one relationship).
An Admin can manage multiple Movies (1-to-many relationship).
A Payment is associated with one Movie and one Showtime (many-to-one relationships).
An Email is associated with one Customer (many-to-one relationship).

```js
Customer(id, created_at, updated_at, name, email_address, contact_information);

Movie(
  id,
  created_at,
  updated_at,
  title,
  genre,
  release_date,
  rating,
  running_time,
  description,
);

Screen(id, created_at, updated_at, name, capacity, seating_arrangement);

Ticket(
  id,
  created_at,
  updated_at,
  customer_id,
  movie_id,
  screen_id,
  showtime_id,
  seat_id,
  price
);

Showtime(
  id,
  created_at,
  updated_at,
  movie_id,
  screen_id,
  showtime_details,
  date,
  time
);

Seat(id, created_at, updated_at, screen_id, row, number);

Admin(id, created_at, updated_at, Name, email_address, contact_information);

Payment(
  id,
  created_at,
  updated_at,
  booking_id,
  amount,
  payment_method,
  transaction_id
);

Email(id, created_at, updated_at, customer_id, subject, body);
```
