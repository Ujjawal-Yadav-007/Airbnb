<img width="800" alt="Screenshot 2025-03-19 at 10 03 01 PM" src="https://github.com/user-attachments/assets/0907a621-77b1-499a-9274-631588270b39" />Booking Management System (Airbnb-like)
Project Overview

This Booking Management System is a web-based platform designed for managing hotel bookings, built with Java, Spring Boot, Hibernate, and PostgreSQL. The system follows the Model-View-Controller (MVC) architecture.

    Guests can search for available hotels and make bookings.
    Managers can create and manage hotel listings, set availability, and view booking information.

The system is designed with clean separation of concerns, following the MVC structure:

    Model: Manages the business logic and database interaction using Hibernate ORM with PostgreSQL as the database.
    View: Handles the presentation layer (e.g., user interface, templates).
    Controller: Manages the flow of data between the Model and View, handling user requests and responses.

Features
Guest Features:

    Search Hotels: Guests can search for hotels based on location, dates, and other filters (e.g., room Type).
    Hotel Booking: Guests can select rooms, provide booking details, and confirm the booking.

Manager Features:

    Create Hotel Listings: Managers can create and manage hotel listings by providing details like location, amenities, room types, and pricing.
    Set Availability: Managers can set room availability and configure pricing.
    Manage Bookings: Managers can view and manage the bookings made by guests (confirm, cancel, etc.).

Technologies Used

    Backend: Java, Spring Boot, Hibernate
    Database: PostgreSQL
    Frontend: [Insert frontend technology here, e.g., React, HTML, CSS]
    Authentication: JWT or OAuth for secure user login and session management
    MVC Framework: Spring MVC
    Build Tool: Maven

Folder Structure

/src
    /main
        /java
            /com/bookingapp
                /controller     # Contains controllers for handling HTTP requests
                /model          # Contains entity models mapped to database tables
                /repository     # Contains interfaces for CRUD operations with Hibernate
                /service        # Contains business logic services
                /config         # Configuration classes for database, security, etc.
                /dto            # Data Transfer Objects used for API responses
        /resources
            /static             # Static files like images, CSS, JavaScript
            /templates          # HTML templates (if using Thymeleaf)
            /application.properties # Contains database and application configurations
        /sql
            /migrations         # SQL scripts for database schema creation and migrations

How to Set Up the Project
1. Clone the repository

git clone <repository-url>

2. Install dependencies

The project uses Maven for dependency management. In the root directory of the project, run:

mvn clean install

3. Set up the database

    Create a new PostgreSQL database (e.g., booking_system).
    In application.properties (or application.yml), configure the database connection details:

spring.datasource.url=jdbc:postgresql://localhost:5432/booking_system
spring.datasource.username=<your-username>
spring.datasource.password=<your-password>
spring.jpa.hibernate.ddl-auto=update  # Automatically updates the schema if needed
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

4. Run the application

mvn spring-boot:run

Once the server is running, you can access the application through your browser (typically at http://localhost:8080).
Data Flow Diagram (DFD)

Here’s a high-level description of the Data Flow Diagram (DFD) for the system:
Level 1: Context Diagram

    External Entities:
        Guests (can make hotel bookings)
        Managers (can manage hotel listings and bookings)
    System: Booking Management System
        Processes:
            Hotel Search: Guests search for hotels based on specific filters.
            Hotel Booking: Guests book a hotel by selecting rooms and confirming the booking.
            Hotel Management: Managers create and manage hotel listings.
            Booking Management: Managers manage bookings, including confirmations and cancellations.
        Data Stores:
            Hotel Listings Database: Contains details about the hotels (name, location, rooms, pricing).
            Bookings Database: Contains information about guest bookings.
            User Accounts Database: Contains guest and manager account details.

Level 2: Detailed DFD

    Guests:
        Hotel Search: Sends search criteria (e.g., location, dates) and receives a list of available hotels.
        Hotel Booking: Sends booking details (hotel ID, room type, dates) and receives confirmation.
    Managers:
        Hotel Management: Creates and updates hotel listings and room availability.
        Booking Management: Views and manages guest bookings, including confirmation, modification, or cancellation.
<img width="800" alt="Screenshot 2025-03-19 at 10 04 06 PM" src="https://github.com/user-attachments/assets/a7825bab-9347-4317-8a9d-04ad63243ea2" />



Conclusion

This Booking Management System provides a seamless experience for both guests and managers in the hospitality industry. Guests can easily search and book rooms, while managers can efficiently manage hotel inventories and handle bookings.
