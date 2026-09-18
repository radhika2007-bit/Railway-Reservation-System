# 🚆 Core Java Rail Reservation System

## 📝 Project Overview

The **Rail Reservation System** is a terminal-based railway management application developed using **Core Java**. It provides basic reservation facilities for passengers and management features for administrators.

The application does not use MySQL or any external database. Instead, **Java File Handling** is used to store users, trains, passengers, and ticket information in text files. This allows the data to remain available even after the application is closed.

## 🎯 Project Objectives

The main objectives of this project are:

* To develop a practical railway reservation system using Core Java.
* To apply Object-Oriented Programming concepts in a real-world application.
* To provide separate functionalities for users and administrators.
* To allow users to search trains and book tickets.
* To automatically generate unique PNR numbers.
* To assign available seats during booking.
* To maintain records using text files.
* To handle railway-related errors using custom exceptions.

## 👤 User Functionalities

A registered user can perform the following operations:

* Register a new account.
* Log in using valid credentials.
* Search and view registered trains.
* Check seat availability.
* Book railway tickets.
* Receive an automatically generated PNR.
* Get an available seat number.
* Search ticket details using PNR.
* View previous booking records.
* Cancel an existing reservation.

## 👑 Administrator Functionalities

The administrator is responsible for managing train and reservation information.

The administrator can:

* Log in using administrator credentials.
* Add new trains.
* Update train information.
* Delete train records.
* View all registered trains.
* View booking and reservation records.

## 🧠 Java Concepts Used

The project implements several important Core Java concepts:

* Classes and Objects
* Encapsulation
* Inheritance
* Abstraction
* Polymorphism
* Interfaces
* Method Overriding
* Comparable Interface
* ArrayList
* Collections Framework
* File Input/Output
* Exception Handling
* User-Defined Exceptions
* User-Defined Packages

## 🚆 Train Management

The `Train` class stores important train information such as:

* Train Number
* Train Name
* Source
* Destination
* Total Seat Capacity
* Ticket Fare

The administrator can add, modify, delete, and view train records.

The `Train` class implements `Comparable<Train>`, allowing train objects to be sorted in ascending order according to their train numbers.

## 🎫 Ticket Reservation

During ticket booking, the system maintains the following information:

* PNR Number
* User ID
* Train Number
* Passenger ID
* Seat Number
* Fare
* Booking Status

For every successful booking, a unique PNR is generated automatically. The system searches for an available seat and assigns it to the passenger.

## 💺 Seat Management

Before confirming a reservation, the application checks the confirmed bookings of the selected train.

If all seats are occupied, a `SeatNotAvailableException` is generated and the booking is rejected.

When a ticket is cancelled, its seat becomes available again and can be assigned to another passenger.

## ⚠️ Exception Handling

The project uses custom exceptions for handling railway-specific errors.

The main exceptions are:

* `TrainNotFoundException`
* `SeatNotAvailableException`
* `TicketNotFoundException`

These exceptions are used when a requested train or ticket cannot be found or when no seat is available.

## 💾 Data Storage

Java File Handling is used to store application data without requiring an external database.

The project uses:

* `File`
* `FileReader`
* `FileWriter`
* `BufferedReader`
* `BufferedWriter`

All records are maintained inside the `data` directory using text files.

## 📂 Project Structure

```text
RailReservationSystem/

├── src/
│   ├── Main.java
│   ├── model/
│   │   ├── Person.java
│   │   ├── User.java
│   │   ├── Passenger.java
│   │   ├── Train.java
│   │   └── Ticket.java
│   │
│   ├── service/
│   │   ├── ReservationSystem.java
│   │   ├── TrainService.java
│   │   ├── TicketService.java
│   │   └── UserService.java
│   │
│   ├── exception/
│   │   ├── TrainNotFoundException.java
│   │   ├── SeatNotAvailableException.java
│   │   └── TicketNotFoundException.java
│   │
│   └── util/
│       ├── FileManager.java
│       ├── InputHelper.java
│       └── PNRGenerator.java
│
├── data/
│   ├── users.txt
│   ├── trains.txt
│   ├── tickets.txt
│   └── passengers.txt
│
└── README.md
```

## 📦 Package Organization

### `model`

Contains the main entities such as `Person`, `User`, `Passenger`, `Train`, and `Ticket`.

### `service`

Contains the main business logic for user management, train management, ticket booking, and reservations.

### `exception`

Contains custom exceptions used to handle railway-specific errors.

### `util`

Contains utility classes for file management, input handling, and PNR generation.

## 💻 Technologies Used

| Technology         | Purpose                   |
| ------------------ | ------------------------- |
| Core Java          | Main programming language |
| OOP                | Application design        |
| ArrayList          | Managing records          |
| Comparable         | Sorting trains            |
| File Handling      | Data persistence          |
| Exception Handling | Error management          |
| Terminal           | User interface            |

## 🚀 How to Run

Open the terminal inside the `src` directory and compile the project:

```text
javac Main.java model\*.java service\*.java exception\*.java util\*.java
```

Run the application using:

```text
java Main
```

## 🔐 Default Administrator Account

* **User ID:** `A001`
* **Username:** `admin`
* **Password:** `admin123`
* **Role:** `ADMIN`

## 📊 Data Files

* `users.txt` — stores user and administrator information.
* `trains.txt` — stores train details.
* `tickets.txt` — maintains ticket and reservation records.
* `passengers.txt` — stores passenger information.

## 🔮 Future Enhancements

The system can be improved in the future by adding:

* MySQL database integration.
* Graphical User Interface.
* Web-based railway reservation.
* Password encryption.
* Online payment facilities.
* Complete train timetable management.
* Different classes and seating categories.
* Email/SMS booking notifications.
* Multiple-passenger group booking.

## 📌 Conclusion

The **Rail Reservation System** demonstrates the practical use of Core Java in developing a real-world command-line application.

It combines **OOP, Collections, Comparable, File Handling, Exception Handling, Custom Exceptions, and User-Defined Packages** in a single project.

The modular structure makes the application easy to understand, maintain, and extend with additional railway reservation features.

## 👩‍💻 Author

**Name:** Radhika Rai

**Registration No.:** 25BAR10002

**Program:** B.Arch

**University:** VIT Bhopal University
