# Ticket-Booking-App

This project is a **backend system** for a train ticket booking service. It handles user registrations, login, searching for trains based on source and destination, booking tickets, and retrieving booked tickets. The backend uses **Java** and is structured with Gradle for dependency management and build automation.

## Features

1. **User Authentication**:
   - Signup with hashed passwords.
   - Login with password validation.

2. **Train Management**:
   - Search for available trains between a source and destination.
   - View details about trains such as seat availability, station times, and more.

3. **Ticket Booking**:
   - Book a seat on a train for registered users.
   - View previously booked tickets.

4. **Seat Management**:
   - Check seat availability for selected trains.
   - Book specific seats for a journey.


## Key Directories:

- **entities/**: Contains data model classes such as:
  - **Train**: Represents train information, including seat availability, stations, and timings.
  - **User**: Represents user information, including bookings and login credentials.
  - **Ticket**: Represents booking tickets for users, linked to train and user data.

- **localDB/**: Contains the following JSON files, acting as a local database:
  - **trains.json**: Stores information about trains, stations, and available seats.
  - **users.json**: Stores information about registered users and their booked tickets.

- **service/**: Contains business logic and services:
  - **TrainService**: Handles train search, seat availability, and booking.
  - **UserBookingService**: Manages user registration, login, and bookings.

- **test-ledger/**: Contains test files and utilities for running project tests.

- **util/**: Contains utility classes used across the project, including password hashing and helper methods.


## Dependencies

The project is built with **Gradle**. All dependencies are managed within the Gradle build configuration.

## How to Run the Project

### Prerequisites

- **Java Development Kit (JDK)**: You need to have JDK installed (preferably JDK 11 or higher).
- **Gradle**: This project uses Gradle for building and managing dependencies. You can either install Gradle globally or use the Gradle wrapper provided in the project.

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/LavishVaishnav/Ticket-Booking-App.git
   cd Ticket-Booking-App
   ```

2. **Build the Project**:
   You can build the project using Gradle. Run the following command to build it:
   ```bash
   ./gradlew build
   ```

3. **Run the Application**:
   Once the build is complete, you can run the application:
   ```bash
   ./gradlew run
   ```

4. **Testing**:
   To run the tests in the project, you can use the Gradle test task:
   ```bash
   ./gradlew test
   ```

### Gradle Wrapper

This project comes with a **Gradle wrapper** (`gradlew`) that allows you to run Gradle tasks even if Gradle is not installed on your machine. You can use `./gradlew build` and `./gradlew run` as mentioned above.

---

