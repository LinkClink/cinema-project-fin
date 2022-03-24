 * project under development

## Cinema-project

This is a prototype of a web application that works like a cinema service. Configured authorization and authentication. 
In this application, user can have two roles `ADMIN` or `USER`.
___

## Project structure

Here used 3-tier architecture:
* Data access layer (DAO).
* Application layer (service).
* Presentation layer (controllers).

___

## Opportunities depending on the role
There are two roles application:
- ADMIN
- USER

User:
* GET: /orders (display all the orders)
* GET: /shopping-carts/by-user (display the contents of the current user's shopping)
* POST: /orders/complete (complete the current order)
* PUT: /shopping-carts/movie-sessions (add movie session to the shopping cart)

Admin:
* POST: /cinema-halls (add new cinema hall)
* POST: /movies (add new movie)
* POST: /movie-sessions (add new movie session)
* PUT: /movie-sessions/{id} (update movie session with specified id)
* DELETE: /movie-sessions/{id} (delete movie session by id)
* GET: /users/by-email (find user by email)

User and Admin:
* GET: /cinema-halls (display all the cinema halls)
* GET: /movies (display all the movies)
* GET: /movie-sessions/available (display all the available movie sessions)
___
### Technologies:
The following stack of technologies was used in the project:

* Tomcat
* Hibernate
* Spring Web
* Spring Security
* Spring Core
* MySQL
* Maven 
___
### How to start the application

1. Install and Configure Apache Tomcat 9.0.50
2. Install MySQL and Create a Schema
3. In the db.properties change YOUR_URL, YOUR_USERNAME and YOUR_PASSWORD values
   to the ones you specified when installing MySQL, also change JDBC_DRIVER
4. There is one already registered ADMIN user with username `admin@i.ua` and password `admin123` fill free to use it, or register a new user using Postman
5. Run the application

