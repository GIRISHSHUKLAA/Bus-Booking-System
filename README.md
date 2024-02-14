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


## API Module Endpoints

### Login Module

* `POST //login/admin` : Admin can login with mobile number and password provided at the time of registation
<!--
### User Module


* `POST /customer/login` : Logging in customer with valid mobile number & password
* `GET /customer/availablecabs` : Getting the list of all the available cabs
* `GET /customers/cabs` : Getting All the cabs
* `GET /customers/checkhistory` : Getting the history of completed tr
* `PUT /customer/update/{mobile}` : Updates customer details based on mobile number
* `PATCH /customer/updatepassword/{mobile}` : Updates customer's password based on the given mobile number
* `POST /customer/booktrip` : Customer can book a cab
* `POST /customer/updatetrip` : Customer can modify or update the trip
* `POST /customer/logout` : Logging out customer based on session token
* `DELETE /customer/delete` : Deletes logged in user 
* `DELETE /customer/complete/{tripid}` : Completed the trip with the given tripid 
* `DELETE /customer/canceltrip` : Cancel the trip with the given tripid   


### Admin Module

* `POST /admin/register` : Register a new admin with proper data validation and admin session
* `POST /admin/login` : Admin can login with mobile number and password provided at the time of registation
* `GET /admin/logout` : Logging out admin based on session token
* `GET /admin/listoftripsbycustomer` : Get list of trips of by a customer id
* `GET /admin/listoftrips` : Get list of trips of all the trips
* `GET /admin/listocustomers` : Get list of all the customers
* `GET /admin/listodrivers` : Get list of all the drivers
* `PUT /admin/update/{username}` : Updates admin detaisl by passed user name
* `DELETE /admin/delete` : Deletes the admin with passed id   -->


### Sample API Response for Admin Login

`POST   localhost:8080/login/admin`

* Sample Request Body

```
    {
        "mobileNo": "8891067909",
        "password": "Moarpllme@007"
    }
```

* Sample Response Body

```
   CurrentAdminSession( adminId=1, uuid=uUcWXg,localDatetime=2022-11-11 12:29:52.376508)
   
```

### Swagger UI

---
### User and User Login Controller

---
![Screenshot (291)](https://user-images.githubusercontent.com/100846744/201393329-4ca0173c-b6fe-46f9-afe0-a977f096687f.png)


![Screenshot (292)](https://user-images.githubusercontent.com/100846744/201393274-7d2f08c6-2fbe-47d2-af20-e85f0cc6482b.png)

---

### Admin and Admin Login Controller

---
![Screenshot (290)](https://user-images.githubusercontent.com/100846744/201393426-bdee2b71-4b89-47c2-b60a-969464088294.png)
![Screenshot (285)](https://user-images.githubusercontent.com/100846744/201393509-babcc11c-8501-4ad9-b8a7-30a5a67615a9.png)

---

### Bus Controller

---


![Screenshot (286)](https://user-images.githubusercontent.com/100846744/201393212-9f8d839e-a6cd-4d9e-aac3-7cd975d04675.png)

---
