# REST API for Bus Booking System 

* Used a REST API for a Bus Booking System Application. This API performs all the fundamental CRUD operations of any Bus Reservation Application platform with user validation at every step.
 
## Tech Stack

* Java
* Spring Framework
* Spring Boot
* Spring Data JPA
* Hibernate
* MySQL

## Modules

* Login, Logout Module
* Admin Module
* User Module
* Route Module
* Bus Module
* Reservation Module
* Feedback Module

## Features

* User and Admin authentication & validation with session uuid.
* Admin Features:
    * Administrator Role of the entire application
    * Only registered admins with valid session token can add/update/delete route and bus from main database
    * Admin can access the details of different users and reservations.
* User Features:
    * Registering themselves with application, and logging in to get the valid session token
    * Viewing list of available buses and booking a reservation
    * Only logged in user can access his reservations, profile updation and other features.


## Installation & Run

* Before running the API server, you should update the database. 
* Update the port number, username and password as per your local database config.

```
    server.port=8080

    spring.datasource.url=jdbc:mysql://localhost:3306/busBooking
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    spring.datasource.username=your_db_username
    spring.datasource.password=your_db_password

```

## API Root Endpoint

`https://localhost:8080/`

`http://localhost:8080/swagger-ui/`


## We will call API using Swagger UI you can use postman also

`http://localhost:8080/swagger-ui/#/I`

