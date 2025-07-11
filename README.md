# Ecomerce
Online Ecomerce web page

# Online Shop Application

#### A full-stack Online Shop web application using Spring Boot 2 and Angular 7. 
This is a Single Page Appliaction with client-side rendering. It includes backend and frontend two seperate projects on different branches.
The frontend client makes API calls to the backend server when it is running.

## Features
- REST API
- Docker
- Docker Compose
- JWT authentication
- Cookie based visitors' shopping cart
- Persistent customers' shopping cart
- Cart & order management
- Checkout
- Catalogue
- Order management
- Pagination
## Technology Stacks
**Backend**
  - Java 11
  - Spring Boot 2.2
  - Spring Security
  - JWT Authentication
  - Spring Data JPA
  - Hibernate
  - PostgreSQL
  - Maven

**Frontend**
  - Angular 7
  - Angular CLI
  - Bootstrap

## Database Schema

Install Postgressql -> after installation -> search PGAdmin
Open Admin -> give password which you provide at the time of installation.
Create Database with name "ecommerce". Then run queries provided in eshop.sql script one by one.


## How to  Run

Start the backend server before the frontend client.  

**Backend**

  1. Install [PostgreSQL](https://www.postgresql.org/download/) 
  2. Configure datasource in `application.yml`.
  3. `cd backend`.
  4. Run `mvn install`.
  5. Run `mvn spring-boot:run`.
  6. Spring Boot will import mock data into database by executing `import.sql` automatically.
  7. The backend server is running on [localhost:8080]().

**Frontend**
  1. Install [Node.js and npm](https://www.npmjs.com/get-npm)
  2. `cd frontend`.
  3. Run `npm install`.
  4. Run `ng serve`
  5. The frontend client is running on [localhost:4200]().
  
Note: The backend API url is configured in `src/environments/environment.ts` of the frontend project. It is `localhost:8080/api` by default.
  
#### Run in Docker
You can build the image and run the container with Docker. 
0. Run Postgre in Docker 
```bash 
docker run --name mypostgres -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=root -p5432:5432 -d postgres:9.4.5
sudo apt update
sudo apt install maven
mvn -version
``` 
1. Build backend project
```bash
cd backend
mvn package
```
2. Build fontend project
```bash
cd frontend
npm install
alias ng="node_modules/@angular/cli/bin/ng"
ng build --prod
```
3. Build images and run containers
```bash
docker-compose up --build


```

Modules:
1.Customer login
	- Create Customer from sign up page
2.Admin login
	- Default Admin Login
		User Name - abc@gmail.com
		Password - 1234

