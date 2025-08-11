🎯 Hotel-Task1 – Hotel Booking System in MySQL

SQL database and ER diagram for a Hotel Booking System.



🏨 Hotel Booking System – MySQL Project

📌 Description

This is a relational database project built using MySQL to manage hotel operations. It maintains records for guests, rooms, bookings, payments, and additional services, enabling efficient tracking, billing, and reporting for hotel management.

---

 📁 Database Structure

✅ **Tables:**

1. **Guests** – Stores guest personal details and contact information.
2. **Rooms** – Stores room details, types, pricing, and availability status.
3. **Bookings** – Stores booking records, linking guests to rooms with check-in/out dates and total amount.
4. **Payments** – Stores payment transactions related to bookings.
5. **Services\_Used** – Stores details of extra services (e.g., spa, laundry) availed by guests during their stay.

---

### 🔁 Relationships:

* A **guest** can have multiple bookings.
* A **room** can be booked many times (at different periods).
* A **booking** can have multiple payments.
* A **booking** can include multiple additional services.
* Each service record links to one booking.

---

### 🛠️ Technologies Used

* **MySQL 8.x** – Relational database engine
* **MySQL Workbench** – Database design & ER diagram creation
* **SQL** – DDL for structure creation, DML for inserting and managing data

---

Do you want me to also prepare the **Task 2 version** in the same format for your DML (INSERT, UPDATE, DELETE) practice? That way your GitHub will look uniform.


In Task 1, I learned how to create a database, design relational tables with appropriate fields and data types, and define relationships using primary and foreign keys. I also created an ER diagram to visually represent the schema and connections between tables.



