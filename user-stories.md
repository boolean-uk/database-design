- As a customer, so I can receive my tickets, I want to provide my contact information.
- As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
- As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.

User Stories (Cinema)

As a cinema customer, I want to view a list of available movies so I can decide which movie I want to watch.

As a cinema customer, I want to view a list of screenings for a selected movie so I can choose an available screening time that suits me.

As a cinema customer, I want to see a list of available seats for a selected screening so I can decide on my preferred seat.

As a cinema customer, I want to provide my payment information online so I can purchase tickets for the selected movie and screening.

As a cinema customer, I want to provide my contact information so I can receive my purchased tickets via email.

As a cinema customer, I want the option to buy tickets for others and gift them to friends or family members, even if I am not attending the screening myself.

As a cinema admin, I want to be able to update the list of movies shown at the cinema.

As a cinema admin, I want to manage the screens and have a list of all available screens.

As a cinema admin, I want to keep track of the scheduled screenings at various cinema rooms, including movie information and screening times.

As a cinema admin, I want to maintain a list of registered customers for record-keeping and communication purposes.

As a cinema admin, I want to track the types of tickets sold, such as child or adult tickets.

As a cinema admin, I want to keep a record of ticket sales for tracking and reporting purposes.

As a cinema admin, I want to have a list of available seats in each screening to prevent overbookings and ensure proper seat allocation.

As a cinema admin, I want to know which seats are available in real-time to assist customers with ticket booking and seat selection.

- Cinema has 9 screens, each screen must have it's own table in the database example 

(Screen 1)

ID Number - INTI (PK)
CreatedAt - Date/Time
UpdatedAt - Date/time
Location -  String
Availability - Yes/No

However also need to take in to account that Screenings will have a list of movies
that are showing at the cinema so that table needs Movie 1 - 9 for example but each screen 
will show a number of diffrent movies or just a single movie at any given time / date.

Cinema table also required with again linking to the screen table 1 - 9 