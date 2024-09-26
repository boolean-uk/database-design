# Entities
## Films

| attribute | type |
|---|---|
| id | PK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| title | TEXT, NOT NULL |
| release_year | INT, NOT NULL |
| director | TEXT, NOT NULL |
| studio | TEXT, NOT NULL |
| format | ENUM: “2D” / “3D” |
| genre | ENUM, (some list of valid values), NOT NULL |

## License

| attribute | type |
|---|---|
| id | PK |
| screen_id | FK |
| created_by | FK (employee_id) |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| start_date | DATETIME, MANDATORY |
| end_date | DATETIME, MANDATORY |
| price | FLOAT, MANDATORY |
| details | TEXT, NOT NULL |

## Screen (aka room)

| attribute | type |
|---|---|
| id | PK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| room_number | TEXT, NOT NULL, UNIQUE |
| has_3d | BOOLEAN, NOT NULL |
| active | BOOLEAN, NOT NULL |

## Seating Area

| attribute | type |
|---|---|
| id | PK |
| name | TEXT, NOT NULL, UNIQUE |

## Seats

| attribute | type |
|---|---|
| id | PK |
| screen_id | FK |
| seating_area_id | FK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |

## Ticket categories

| attribute | type |
|---|---|
| id | PK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| name | TEXT, NOT NULL |
| price | FLOAT |
| age_group_min | INT, NOT NULL |
| age_group_max | INT, NOT NULL |
| description | TEXT |

## Screening

| attribute |  |
|---|---|
| id | PK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| film_id | FK |
| screen_id | FK |
| start_timestamp | DATETIME, NOT NULL |
| is_booked | BOOLEAN, NOT NULL |

## Ticket

| attribute | type |
|---|---|
| id | PK |
| screening_id | FK |
| ticket_category_id | FK |
| customer_id | FK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| is_valid | BOOLEAN, NOT NULL |
| digital | BOOLEAN, NOT NULL |

## Ticket Validation

| attribute | type |
|---|---|
| id | PK |
| ticket_id | FK, UNIQUE |
| personell_id | FK |
| seat_id | FK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |

## employee

| attribute | type |
|---|---|
| id | PK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| role | ENUM, NOT NULL (manager / clerk) |
| active | BOOLEAN, NOT NULL |
| username | TEXT, MANDATORY, UNIQUE |
| password | TEXT, MANDATORY |

## customer

| attribute | type |
|---|---|
| id | PK |
| created_at | DATETIME, NOT NULL |
| updated_at | DATETIME |
| username | TEXT, MANDATORY, UNIQUE |
| password | TEXT, MANDATORY |
| name | TEXT, NOT NULL |
| birthday | DATE, NOT NULL |
| email | TEXT, NOT NULL, MANDATORY, UNIQUE |
| phone | TEXT |