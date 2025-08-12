# Hotel Reservation System

## Overview
The **Hotel Reservation System** is a console-based Java application that enables efficient management of hotel room bookings.  
It leverages **MySQL** for persistent storage and **JDBC** for seamless database connectivity.  
Designed with **Object-Oriented Programming** principles, the system offers a clean, modular, and maintainable codebase.

---

## Features
- **Room Reservation**: Add new bookings with guest name, room number, and contact details.
- **View All Reservations**: Display existing bookings in a structured tabular format.
- **Retrieve Room Information**: Find assigned room numbers using Reservation ID and guest name.
- **Update Bookings**: Modify guest details, room assignments, or contact numbers.
- **Delete Reservations**: Remove bookings from the system.
- **Graceful Exit**: Exit the system with a user-friendly countdown animation.

---

## Technology Stack
| Component           | Technology Used |
|---------------------|-----------------|
| Programming Language| Java 17+        |
| Database            | MySQL           |
| Connectivity        | JDBC            |
| Paradigm            | OOP (Object-Oriented Programming) |
| IDE                 | IntelliJ IDEA   |


## Database Schema
**Database Name:** `hotel_db`  
**Table Name:** `reservations`

```sql***
CREATE DATABASE hotel_db;
USE hotel_db;

CREATE TABLE reservations (
    reservation_id INT PRIMARY KEY AUTO_INCREMENT,
    guest_name VARCHAR(50) NOT NULL,
    room_number INT NOT NULL,
    contact_number VARCHAR(15) NOT NULL,
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


Setup & Installation
1. Prerequisites
Java 17 or higher installed

MySQL Server installed and running

MySQL Connector/J (JDBC driver)

2. JDBC Driver Setup in IntelliJ IDEA
Download MySQL Connector/J.

In IntelliJ IDEA:

Right-click project → Open Module Settings

Go to Libraries → Click + → Select Java

Add the downloaded JAR file.

3. Update Database Credentials
In HotelReservationSystem.java, update:

java

private static final String url = "jdbc:mysql://localhost:3306/hotel_db";
private static final String username = "root";
private static final String password = "your_password";

4. Run the Application
Compile and run HotelReservationSystem.java.

Follow the on-screen menu prompts.

Sample Output
HOTEL MANAGEMENT SYSTEM
1. Reserve a room
2. View Reservations
3. Get Room Number
4. Update Reservations
5. Delete Reservations
0. Exit
Choose an option:

Future Enhancements
Implement GUI using JavaFX or Swing

Add authentication system for admin/reception roles
Integrate room availability check before booking
Generate booking confirmation receipts in PDF

Author
Amol Shinde
Java Developer 
Email: shindeamol7674@gmail.com.com
GitHub: https://github.com/amolashinde
