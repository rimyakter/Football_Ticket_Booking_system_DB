# Football Ticket Booking System Database

## Overview

A PostgreSQL-based Football Ticket Booking System that manages users, football matches, and ticket bookings.

## Database

## Tables

### Users

Stores customer and admin information.

Columns:

- user_id (PK)
- full_name
- email (Unique)
- role
- phone_number

Roles:

- Football Fan
- Ticket Manager

### Matches

Stores football match and ticket information.

Columns:

- match_id (PK)
- fixture
- tournament_category
- base_ticket_price
- match_status

Status:

- Available
- Selling Fast
- Sold Out

### Bookings

Stores ticket purchase records.

Columns:

- booking_id (PK)
- user_id (FK)
- match_id (FK)
- seat_number
- payment_status
- total_cost

Payment Status:

- Confirmed
- Pending

## Relationships

- One User → Many Bookings
- One Match → Many Bookings

## SQL Concepts Used

- Primary Key & Foreign Key
- Constraints
- INNER JOIN
- LEFT JOIN
- Subqueries
- AVG()
- LIKE / ILIKE
- IS NULL
- COALESCE()
- ORDER BY
- OFFSET & LIMIT

## Queries Included

1. Retrieve available Champions League matches
2. Search users by name pattern
3. Handle missing payment status
4. Show booking details with user and match data
5. List all users including users without bookings
6. Find bookings above average cost
7. Retrieve second-highest ticket prices

## Technologies

- PostgreSQL
- SQL
- ERD Design (Lucidchart)
    Link: https://lucid.app/lucidchart/ca396db3-dd1c-4904-9862-0992dfca81fc/edit?viewport_loc=-2960%2C914%2C2437%2C1055%2C0_0&invitationId=inv_e0d60383-ac68-4763-a24d-b3ced240a3a6

## How to Run

1. Create the database
2. Execute the SQL file
3. Tables and sample data will be created automatically
