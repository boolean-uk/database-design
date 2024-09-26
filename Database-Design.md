+-------------------+     +-------------------+     +-------------------+
|    Customers      |     |      Contact      |     |      Movies       |
+-------------------+     +-------------------+     +-------------------+
| id (PK)           |     | id (PK)           |     | id (PK)           |
| createdAt         |     | createdAt         |     | createdAt         |
| updatedAt         |     | updatedAt         |     | updatedAt         |
| name              |     | customerId (FK)   |     | title             |
| email             |     | address           |     | genre             |
| phone             |     +-------------------+     | duration          |
+-------------------+                               | releaseDate       |
                                                    +-------------------+
           |
           |
           V
+-------------------+
|       Admin       |
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| name              |
| email             |
+-------------------+

           |
           |
           V
+-------------------+
|      Screen       |
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| name              |
+-------------------+

           |
           |
           V
+-------------------+
|      Tickets      |
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| customerId (FK)   |
| movieId (FK)      |
| screenId (FK)     |
| scheduleId (FK)   |
| seatNumber        |
+-------------------+

           |
           |
           V
+-------------------+
|     Schedule      |
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| movieId (FK)      |
| screenId (FK)     |
| timeSlotId (FK)   |
| date              |
+-------------------+

           |
           |
           V
+-------------------+
|    Time Slot      |
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| startTime         |
| endTime           |
+-------------------+

           |
           |
           V
+-------------------+
|Seating Arrangement|
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| screenId (FK)     |
| seatNumber        |
| isReserved        |
+-------------------+

           |
           |
           V
+-------------------+
|Transaction History|
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| customerId (FK)   |
| ticketId (FK)     |
| transactionAmount |
| paymentMethod     |
+-------------------+

           |
           |
           V
+-------------------+
| Newsletter Sub.   |
+-------------------+
| id (PK)           |
| createdAt         |
| updatedAt         |
| customerId (FK)   |
| isSubscribed      |
+-------------------+
