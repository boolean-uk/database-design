# Database Design

## Epic

A local cinema wants to allow people to book tickets online to see movies that are being shown in its various screens. These tickets should be delivered to customers via email. The cinema wants to keep a record of their customers and the tickets they purchase, as well as offer a regularly updated list of movies for them to choose from. A single screen might show multiple movies a day, and even the same movie at multiple times. The cinema will expand its number of screens in the future, so the potential for growth needs to be accounted for.

## Extracted user stories

1. As a customer, so I can receive my tickets, I want to provide my contact information.
2. As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
3. As a customer, so I can keep track of my movie I am planning to watch, I want to see information about my screening.
4. As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.
5. As an admin, so I can manage which movie is shown, I want each screen to have multiple movies available.
6. As an admin, so I can expand my number of screens, I want to keep a list of screens.

## Extracted entities

- screen
  - id
  - cinemaId
  - createdAt
  - updatedAt
  - 3dSupport
  - seatCapacity
- cinemaLocations
  - id
  - locationName
  - createdAt
  - updatedAt
  - address
  - phoneNr
  - screens
- seatAssignment
  - screenId
  - cinemaId
  - seatNumber
- screening
  - id
  - createdAt
  - updatedAt
  - startTime
  - endTime
  - movieId
  - screenId
  - cinemaId
  - ticketsSold
- ticket
  - id
  - createdAt
  - updatedAt
  - ticketPrice
  - seatNumber
  - screeningId
  - movieId
  - customerId
- movie
  - id
  - createdAt
  - updatedAt
  - playtime
  - description
  - ageRating
  - 3d
- customer
  - id
  - createdAt
  - updatedAt
  - name
  - email
  - phoneNr
- employee
  - id
  - createdAt
  - updatedAt
  - phoneNr
  - name
  