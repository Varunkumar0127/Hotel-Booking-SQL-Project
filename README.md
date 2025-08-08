# Hotel-Booking-SQL-Project
ER Diagram and SQL project for a hotel booking  
## 🏨 Hotel Booking ER Diagram

![ER Diagram](https://github.com/Varunkumar0127/Hotel-Booking-SQL-Project/blob/main/ERD_hotel_booking_system.png?raw=true)

In Task 1, I learned how to create a database, design relational tables with appropriate fields and data types, and define relationships using primary and foreign keys. I also created an ER diagram to visually represent the schema and connections between tables.


create database hotel;
use hotel;
show databases;
CREATE TABLE guests (
    GuestID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    Phone VARCHAR(15),
    Address TEXT
);
desc guests;

CREATE TABLE rooms (
    RoomID INT AUTO_INCREMENT PRIMARY KEY,
    RoomNumber VARCHAR(10) NOT NULL,
    RoomType VARCHAR(50),
    PricePerNight int,
    AvailabilityStatus VARCHAR(20)
);
desc rooms;

CREATE TABLE bookings (
    BookingID INT AUTO_INCREMENT PRIMARY KEY,
    GuestID INT,
    RoomID INT,
    CheckInDate DATE,
    CheckOutDate DATE,
    TotalAmount int,
	FOREIGN KEY (GuestID) REFERENCES guests(GuestID),
    FOREIGN KEY (RoomID) REFERENCES rooms(RoomID)
);
desc bookings;

CREATE TABLE payments (
    PaymentID INT AUTO_INCREMENT PRIMARY KEY,
    BookingID INT,
    PaymentDate DATE,
    PaymentMethod VARCHAR(50),
    AmountPaid DECIMAL(10,2),
    FOREIGN KEY (BookingID) REFERENCES bookings(BookingID)
);
desc payments;

CREATE TABLE services_used (
    ServiceID INT AUTO_INCREMENT PRIMARY KEY,
    BookingID INT,
    ServiceName VARCHAR(100),
    ServiceDate DATE,
    ServiceCost DECIMAL(10,2),
    FOREIGN KEY (BookingID) REFERENCES bookings(BookingID)
);
desc services_used;
