✈️ Automated Flight Reservation System🌟 

Project OverviewThis project is a functional, web-based Flight Booking Application designed to automate the process of collecting and managing flight reservation requests. It serves as a full-stack proof-of-concept, integrating a user-friendly HTML/CSS frontend with a robust PHP/MySQL backend, all containerized using Docker for reliable system deployment.

<img width="1920" height="1080" alt="Screenshot 2025-11-15 021437" src="https://github.com/user-attachments/assets/8dd6734f-9633-44db-9558-2dbda8828808" />

The core objective was to replace manual data entry with a digital, accessible, and database-driven system, ensuring secure data persistence and system integration.


🛠️ Technology Stack

Component,Technology,Role
Frontend,"HTML5, CSS3",User Interface (Flight Booking Form)
Backend/App,PHP (save.php),"Server-side logic, form processing, and database interaction."
Database,MySQL,Persistent storage for booking records (the bookings table).
Deployment,"Docker, Docker Compose",Containerization for consistent and isolated application (myfrontend) and database (mydb) environments.
Networking,Docker Network (flightnet),"Enables secure, container-to-container communication."

🚀 Key Features and Deliverables

=> User-Friendly GUI: Implemented a simple and accessible Graphical User Interface for customers    to enter and submit flight booking details.

=> Secure Data Capture: Developed a PHP backend script (save.php) to handle POST requests, validate form data, and securely map inputs to the database schema.

=> Data Persistence & Integrity: Designed and managed a MySQL database schema (bookings table)  to reliably store critical passenger and flight information.

=> Containerized Environment: Utilized Docker to create a reproducible, multi-container environment, ensuring seamless communication between the application and database tiers.

⚙️ System Implementation & Architecture1. 

  1. Database Schema (bookings Table)The project centers around the core data model, the bookings table, which was created with the following structure to ensure data integrity:
     
    Field Name,Data Type (MySQL),Purpose
    id,"INT (PK, AUTO_INCREMENT)",Unique identifier for each booking.
    fullname,VARCHAR(100),Full name of the passenger.
    email,VARCHAR(100),Contact email address.
    fromcity,VARCHAR(100),Origin/Departure city.
    tocity,VARCHAR(100),Destination city.
    departureDate,DATE,Date of the outbound flight.
    returnDate,DATE,Date of the return flight.
    classType,VARCHAR(50),"Cabin class (e.g., first, economy)."


<img width="1920" height="1080" alt="Screenshot 2025-11-10 124406" src="https://github.com/user-attachments/assets/493b16d6-3e7a-4b93-94b0-4d555b0c8212" />

  2. Data Flow
  The system follows a clear transactional path:

  1.  Input: Customer enters booking data into the HTML Web Form.
    
  2.  Submission: Data is sent via HTTP POST request to the PHP application.
    
  3.  Processing: The save.php script retrieves inputs using $_POST, establishes a connection with the MySQL container, and prepares the SQL query.
    
  4.  Storage: The script executes the INSERT INTO bookings SQL query, storing the record and ensuring Data Persistence.

3. DevOps & Environment Setup
The application is deployed using Docker, defining two main services:

   .myfrontend (Application Container): Hosts the HTML/PHP application layer.
      
   .mydb (Database Container): Hosts the MySQL data layer.

These containers communicate securely over a dedicated flightnet Docker network, demonstrating expertise in System Integration and DevOps principles.

👤 My Role & Responsibilities
As the lead for System Development and Implementation, I was responsible for the full lifecycle of the application:

    . Back-End Development: Coded the save.php logic for secure data mapping and database interaction.
    
    . Database Administration: Defined the optimal CREATE TABLE structure and managed data integrity within MySQL.
    
    . Front-End Development: Developed the basic form structure using HTML/CSS.

    . DevOps/System Integration: Architected and deployed the application using Docker Compose to manage the multi-container environment and networking.

Clone the Repository:
Bashgit clone [your-repo-link]
