# Student Management System

This is a simple Spring Boot application that provides RESTful APIs for managing students. The application allows you to create, read, update, and delete student records.

## Features

- Create a new student
- Get a list of all students
- Get a student by ID
- Update a student by ID
- Delete a student by ID

## Technologies Used

- Java
- Spring Boot
- Spring Data JPA (for database interactions)
- H2 Database (in-memory database for testing)
- Maven (for project management)

## Getting Started

### Prerequisites

- JDK 11 or higher
- Maven 3.6.3 or higher

  
## Explanation of Each Method
- getStudent Method

URL: http://localhost:8080/students/student
HTTP Method: GET
Purpose: Returns a single student object.
Response: A Student object wrapped in a ResponseEntity with a custom header and status OK (200).

- getStudents Method

URL: http://localhost:8080/students
HTTP Method: GET
Purpose: Returns a list of student objects.
Response: A list of Student objects wrapped in a ResponseEntity with status OK (200).

- studentPathVariable Method

URL: http://localhost:8080/students/{id}/{first-name}/{last-name}
HTTP Method: GET
Purpose: Returns a student object based on path variables.
Parameters:
id - student ID
first-name - first name of the student
last-name - last name of the student
Response: A Student object wrapped in a ResponseEntity with status OK (200).

- studentRequestVariable Method

URL: http://localhost:8080/students/query?id=1&firstName=Ramesh&lastName=Fadatare
HTTP Method: GET
Purpose: Returns a student object based on request parameters.
Parameters:
id - student ID
firstName - first name of the student
lastName - last name of the student
Response: A Student object wrapped in a ResponseEntity with status OK (200).

- createStudent Method

URL: http://localhost:8080/students/create
HTTP Method: POST
Purpose: Creates a new student.
Request Body: A Student object to be created.
Response: The created Student object wrapped in a ResponseEntity with status CREATED (201).

- updateStudent Method

URL: http://localhost:8080/students/{id}/update
HTTP Method: PUT
Purpose: Updates an existing student by ID.
Request Body: A Student object with updated information.
Parameters: id - student ID to be updated.
Response: The updated Student object wrapped in a ResponseEntity with status OK (200).

- deleteStudent Method

URL: http://localhost:8080/students/{id}/delete
HTTP Method: DELETE
Purpose: Deletes a student by ID.
Parameters: id - student ID to be deleted.
Response: A message indicating successful deletion wrapped in a ResponseEntity with status OK (200).
Each method in the StudentController class is mapped to a specific HTTP request and provides the corresponding functionality as described.
