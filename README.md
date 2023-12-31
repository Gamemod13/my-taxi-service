
# taxi-service

<p1>This is a web application to show CRUD operation, authenticating, registration, and filtering, using MySQL and 
Servlets. Created following design principles SOLID. The application allows you to create a driver, car, manufacturer, 
or use a taxi service.</p1>
<h1>Functionality</h1>
<ul>
    <li>Register a driver</li>
    <li>Log in and log out</li>
    <li>CRUD operation with drivers</li>
    <li>CRUD operation with cars</li>
    <li>CRUD operation with the manufacturer</li>
    <li>Show all driver cars</li>
    <li>Show all drivers</li>
    <li>Show all manufacturer</li>
    <li>Show all cars</li>
</ul>
<h1>Project structure</h1>
<ul>
    <li>Data Access Object layer (DAO) - it is a design pattern that provides an abstraction layer between the
application/business logic and the data persistence layer (database in my case).</li>
    <li>Service layer - it is a design pattern that provides encapsulation of the application's business logic,
processing requests from the presentation layer, transformations, and invoking appropriate methods from the data access 
layer to retrieve or modify data.</li>
    <li>Controller layer - it is a part of the MVC (Model-View-Controller) design pattern, that provides receives 
requests from the user, authenticates the user, transfers requests to the service layer, gives back the response.</li>
</ul>
<h1>Technology</h1>
<ul>
    <li>Java 11</li>
    <li>Tomcat 9.0.75</li>
    <li>MySQL 8.0.22</li>
    <li>Maven 3.1.1</li>
    <li>Java Servlet 4.0.1</li>
    <li>JSTL 1.2</li>
    <li>JSP, CSS</li>
    <li>JDBC</li>
</ul>
<h1>Introduction for launching the project</h1>
<ol>
    <li>Clone this project from GitHub</li>
    <li>Install Apache Tomcat version 9.x.x. You can download it from the official Apache Tomcat website:
https://tomcat.apache.org/download-90.cgi. Choose the appropriate installation package for your operating system.</li>
    <li>Create a database using either a local MySQL installation or a remote database. Execute the schema provided in
the init_db.sql file to set up the necessary tables and structure for the project.</li>
    <li>Open the project in your preferred Integrated Development Environment.  Locate the ConnectionUtil class in the 
project. It should contain the database connection settings. Fill in the appropriate values for the following fields
(Fill the URL with your MySQL DB including port, name, localtimeZone, etc. Fill in your Username and password to connect
to DB and your JDBC Driver)

![screenshot1](/assets/images/img1.png)

</li>
    <li>Set up the configuration for Tomcat

![screenshot2](/assets/images/img2.png)

![screenshot3](/assets/images/img3.png)

</li>
</ol>

After these steps, you need to fix the tomcat. You need to select the artifact to deploy 'taxi-service: war exploded' 
and remove the Application context 'taxi_service_war' to leave only '/'

![screenshot4](/assets/images/img4.png)

