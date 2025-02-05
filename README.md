# Library-Management-System

- This application demonstrates functionalities of an online library (Turku City Library), that allows users to view, search, and manage books in the library, interacting with the backend API.
- The frontend application repository can be found at: https://github.com/Madhavi96/library-frontend
- The backend application repository can be found at : https://github.com/Madhavi96/library-backend

## Frontend Technologies
- React: JavaScript library for building the user interface.
- React Router: For routing between pages.
- Axios: For making HTTP requests to the backend.
- Sass/SCSS: For styling the components.
- Redux: For managing state.

## Backend Technologies
- Spring Boot: The framework for building the backend API.
- Spring Data JPA: For database interaction using Java Persistence API.
- MySQL: The relational database used to store library data.
- Swagger: API documentation and testing tool.
- Lombok: For reducing boilerplate code (e.g., getters, setters, etc.).
- Mapstruct: For mapping DTOs to the relevant entities and vice versa

### Screenshots

- Login Page
![Screenshot (79)](https://github.com/user-attachments/assets/8d1bc886-ee98-4149-934c-ba5e0eeb48f5)

- Main Page 
![Screenshot (78)](https://github.com/user-attachments/assets/6814c97b-4f99-410b-b09b-0b34864ba82d)

- Swagger
![Screenshot (77)](https://github.com/user-attachments/assets/020b8c8e-97a5-4399-a284-cf899d94ef22)

## Setup Backend

### Prerequisites

- Java 17+ (or the version compatible with your Spring Boot version)
- Maven for building the project
- MySQL for the database

#### 1. Clone the Repository
- Clone the repository to your local machine:

```
git clone https://github.com/Madhavi96/Library-Management-System.git
cd Library-Management-System/backend
```

#### 2. Setup MySQL Database
- Use Docker to spin up a mysql container.

- Create a database called library (or modify the application.properties for a different name).

```
docker run --name mysql-container -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=library -p 3306:3306 -d mysql:latest
```

- As an additional step, we can also open a terminal session inside the mysql-container, to check the database and tables.

```
docker exec -it mysql-container mysql -u root -p
```
- After authenticating with the password, below commands can be used to interact with the database and tables.

```
use library;
show tables;
```


#### 3. Configure the database credentials in src/main/resources/application.properties file:

```
spring.datasource.url=jdbc:mysql://localhost:3306/library
spring.datasource.username=root
spring.datasource.password=root
```

#### 4. Build and Run the Application

- To run the application, use the following command:

```
mvn spring-boot:run
```

- The application will start on the default port 8080. You can change this in the application.properties if needed.

#### 5. Swagger API Documentation
The backend exposes API documentation via Swagger UI. Once the application is running, visit:

```
http://localhost:8080/swagger-ui/
```
This will show the API endpoints with details on how to interact with them.


## Setup Frontend

#### 1. Clone the Repository
- Clone the repository to your local machine:

```
git clone https://github.com/Madhavi96/Library-Management-System.git
cd Library-Management-System/frontend
npm clean install
npm start
```
