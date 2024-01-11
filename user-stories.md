### Here is my user stories 

# As a customer, so I can receive my tickets, I want to provide my contact information.
# As a customer, so I can decide which movie I want to watch, I want to see a list of movies.
# As an admin, so I can manage the movies shown at the cinema, I want to update the list of movies.
# As a customer, so I can book tickets for a specific movie and time, I want to view the available movie showtimes.
# As a customer, so I can confirm my booking, I want to receive an email with my ticket details.
# As a cinema admin, so I can track customer bookings, I want a record of all ticket purchases.
### The Domain Entities will contains : 

- Customer 
- Movie
- BookingRecord
- Ticket
- Show - time
- Admin 
 Each entity will have relationships between each entity. 
 The relation between them is:-
A Showtime is associated with a specific Movie through the movie_id foreign key.
A Ticket is associated with a specific Customer through the customer_id foreign key.
A Ticket is associated with a specific Showtime through the showtime_id foreign key.
A BookingRecord is associated with a specific Customer through the customer_id foreign key.
A BookingRecord is associated with a specific Ticket through the ticket_id foreign key.
FK - represnt Foreign Key to ensure referential integrity between the tables.
PK - reprenst Primary Key

In the Ticket entity, on the diagram I will attach you will  attributes like customer_id and showtime_id. These attributes are foreign keys. Customer_id is a foreign key that refers to the primary key (id) of the Customer entity.
showtime_id is a foreign key that refers to the primary key (id) of the Showtime entity. This means that the values in the customer_id and showtime_id fields in the Ticket table must correspond to existing values in the id field of the Customer and Showtime tables, respectively. It establishes a relationship between the Ticket table and the Customer and Showtime tables.

# updatedAt 
is another commonly used attribute in databases, representing the timestamp indicating when a record was last updated or modified. This attribute is useful for tracking changes to records over time and is crucial for maintaining an audit trail or understanding when the latest modifications occurred.

In the provided Entity Relationship Diagram (ERD), 
# updatedAt
 is included as an attribute for each entity. This allows for recording the timestamp whenever a record is modified or updated in the database. Like createdAt, the actual implementation of updatedAt may depend on the specific data type used for timestamps in the database management system (DBMS) being employed.

Having both createdAt and updatedAt timestamps is a good practice in database design as it provides a comprehensive view of the history of changes to each record. The updatedAt attribute is particularly useful for scenarios where you need to know when the most recent modification to a record took place.

Please for more detail see the diagram i will attach. I use diffrent colurs in order to indicate the relationships between each entity. Thanks!
