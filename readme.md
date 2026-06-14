Football Ticket Booking System – Database Design & SQL Project
 Project Overview

This project is a simplified Football Ticket Booking System designed to demonstrate database design principles, ERD relationships, and intermediate-to-advanced SQL skills. The system manages football fans, ticket bookings, matches, and receipts in a structured relational database.


 Database Overview

The system is built around three core entities:

1. Users Table

Stores information about football fans and ticket managers.

user_id (Primary Key)
full_name
email (Unique)
role (Football Fan / Ticket Manager)
phone_number
2. Matches Table

Stores details of football matches available for booking.

match_id (Primary Key)
team_a
team_b
match_date
venue
base_ticket_price
3. Bookings Table

Stores ticket booking information made by users.

booking_id (Primary Key)
user_id (Foreign Key → Users)
match_id (Foreign Key → Matches)
quantity
total_cost
booking_date

 Relationship

Users → Bookings
One user can make many bookings (1-to-Many)
Matches → Bookings
One match can have many bookings (1-to-Many)
Bookings → Users & Matches
Each booking belongs to exactly one user and one match (Many-to-1)

 ERD Summary
 
Users (1) ───────< Bookings >─────── (1) Matches