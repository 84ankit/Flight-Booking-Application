✈️ Automated Flight Reservation System🌟 

Project OverviewThis project is a functional, web-based Flight Booking Application designed to automate the process of collecting and managing flight reservation requests. It serves as a full-stack proof-of-concept, integrating a user-friendly HTML/CSS frontend with a robust PHP/MySQL backend, all containerized using Docker for reliable system deployment.

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

Full CRUD Capability (Implied): Successfully demonstrated the Create function (Data Capture) and the Read function (by displaying the SELECT * FROM bookings results).⚙️ System Implementation & Architecture1. Database Schema (bookings Table)The project centers around the core data model, the bookings table, which was created with the following structure to ensure data integrity:Field NameData Type (MySQL)PurposeidINT (PK, AUTO_INCREMENT)Unique identifier for each booking.fullnameVARCHAR(100)Full name of the passenger.emailVARCHAR(100)Contact email address.fromcityVARCHAR(100)Origin/Departure city.tocityVARCHAR(100)Destination city.departureDateDATEDate of the outbound flight.returnDateDATEDate of the return flight.classTypeVARCHAR(50)Cabin class (e.g., first, economy).2. Data FlowThe system follows a clear transactional path:Input: Customer enters booking data into the HTML Web Form.Submission: Data is sent via HTTP POST request to the PHP application.Processing: The save.php script retrieves inputs using $_POST, establishes a connection with the MySQL container, and prepares the SQL query.Storage: The script executes the INSERT INTO bookings SQL query, storing the record and ensuring Data Persistence.3. DevOps & Environment SetupThe application is deployed using Docker, defining two main services:myfrontend (Application Container): Hosts the HTML/PHP application layer.mydb (Database Container): Hosts the MySQL data layer.These containers communicate securely over a dedicated flightnet Docker network, demonstrating expertise in System Integration and DevOps principles.👤 My Role & ResponsibilitiesAs the lead for System Development and Implementation, I was responsible for the full lifecycle of the application:Back-End Development: Coded the save.php logic for secure data mapping and database interaction.Database Administration: Defined the optimal CREATE TABLE structure and managed data integrity within MySQL.Front-End Development: Developed the basic form structure using HTML/CSS.DevOps/System Integration: Architected and deployed the application using Docker Compose to manage the multi-container environment and networking.📖 How to Run the Project (Local Setup)To replicate the project locally, you would need Docker and Docker Compose installed.Clone the Repository:Bashgit clone [your-repo-link]
cd automated-flight-reservation
Build and Run Containers:Bashdocker-compose up -d
Access the Application:Navigate to http://localhost:[Your_Mapped_Port] in your web browser.
