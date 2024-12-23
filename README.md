# Employee-Management-System
### Overview
Employee Management System allows users to add, promote, delete, and search employee records. Data is stored using MySQL Database.

### Key Classes
1. **Employee**
   - Represents an employee with attributes like `id`, `first_Name`, `last_Name`,`email_id`.
   - Includes getter and setter methods for each attribute.

2. **EmployeeService**
   - Provides methods for managing employees, such as retrieving the list of employees, creating new employees, and updating or deleting existing ones.

3. **EmployeeController**
   - Acts as the interface for handling HTTP requests, invoking methods from the `EmployeeService` to perform operations on employee data.

## Employee Management API Design
### Overview

This API streamlines the management of employee records, providing essential functionality for data manipulation and ensuring structured operations.

#### Servers
Production:[SwaggerHub API Auto Mocking]

Development:http://localhost:8080/api/v1


#### Endpoints Overview
1. **GET /employees**: Retrieve a list of employees.  
   - **Responses:** 200 (Success), 500 (Internal Server Error).

2. **POST /employees**: Create a new employee.  
   - **Request Body:** Employee object required.  
   - **Responses:** 201 (Created), 400 (Bad Request), 500 (Internal Server Error).

3. **GET /employees/{id}**: Retrieve an employee by ID.  
   - **Parameters:** `id` (integer, required).  
   - **Responses:** 200 (Success), 404 (Not Found), 500 (Internal Server Error).

4. **PUT /employees/{id}**: Update an employee's details.  
   - **Parameters:** `id` (integer, required).  
   - **Request Body:** Employee object required.  
   - **Responses:** 200 (Success), 400 (Bad Request), 404 (Not Found), 500 (Internal Server Error).

5. **DELETE /employees/{id}**: Delete an employee.  
   - **Parameters:** `id` (integer, required).  
   - **Responses:** 204 (No Content), 404 (Not Found), 500 (Internal Server Error).

#### Employee Schema
- **Properties:**

| Property    | Type     | Description                               |
|-------------|----------|-------------------------------------------|
| `id`        | Integer  | Unique identifier for the employee       |
| `firstName` | String   | Employee's first_name                    |
| `lastName`  | String   | Employee's last_name                     |                            |
| `email`     | String   | Email address (format: email_id)           |

## Test Cases for Employee Management API

#### Summary
These test cases provide a comprehensive approach to validating the core functionalities of the Employee Management API, contributing to reliable and effective management of employee data.

#### Test Scenarios
1. **Retrieve Employee Data**
   - Verify the ability to fetch a list of employees and individual employee details using valid, non-existent, and invalid IDs.

2. **Create Employee Records**
   - Test successful creation of new employee records and ensure appropriate error handling for invalid input.

3. **Update Employee Information**
   - Assess the API's capability to update existing employee details, including validation for invalid inputs and handling attempts to update non-existent records.

4. **Delete Employee Records**
   - Confirm successful deletion of employee records while ensuring proper error responses for non-existent IDs.
   
### Expected Outcomes
- The API should return appropriate status codes (200, 201, 204, 400, 404, 500) based on the actions performed.
- Responses should include relevant messages to indicate success or the nature of any errors encountered.
- The API must maintain data integrity, ensuring accurate retrieval, creation, updating, and deletion of employee records.

## Database Schema for Employee Management

### Summary
This schema supports the functionality of the Employee Management API, facilitating efficient management of employee data.

### Employee Table Schema
 **Table Name:** `employees`

| Column Name  | Data Type  | Constraints                          | Description                      |
|--------------|------------|-------------------------------------|----------------------------------|
| `id`         | INTEGER    | PRIMARY KEY, SERIAL                  | Unique identifier for each employee |
| `firstName`  | VARCHAR(50)| NOT NULL                            | Employee's first name            |
| `lastName`   | VARCHAR(50)| NOT NULL                            | Employee's last name             |
| `email`      | VARCHAR(100)| NOT NULL, UNIQUE                   | Employee's email address         |

### Benefits of the Schema
- **Structured Data Management:** The schema allows for organized storage and retrieval of employee records.
- **Data Integrity:** Constraints ensure that only valid data is entered, preventing inconsistencies.
- **Scalability:** The schema is designed to accommodate a growing number of employee records easily.

## Employee Management API

This is a Spring Boot-based RESTful API designed for managing employee records. It supports CRUD (Create, Read, Update, Delete) operations and uses Spring Data JPA to interact with a relational database (e.g., PostgreSQL).

### Features

- **Create Employee** (`POST /employees`): Allows the creation of a new employee record.
- **Get All Employees** (`GET /employees`): Retrieves a list of all employees.
- **Get Employee by ID** (`GET /employees/{id}`): Retrieves a specific employee's details by ID.
- **Update Employee** (`PUT /employees/{id}`): Updates the details of an existing employee.
- **Delete Employee** (`DELETE /employees/{id}`): Deletes an employee by their ID.

### Technologies Used

- **Spring Boot**: Framework for building the API.
- **Spring Data JPA**: To interact with the database using JPA repositories.
- **MySQL Workbench** (or other relational databases): For storing employee records.
- **RESTful API**: Follows REST principles for data access.

- ### Link -
- (https://github.com/Keerthana2312-rgb/FirstEmployeeProject/tree/master/src/main/java/com/example/springboot)

## Questions or Clarifications

If you have any doubts or need clarification regarding the employee details schema or the architecture diagram, please feel free to reach out to me. I'm here to help!

### Contact Details
- **Name:** Keerthana Rajasekaran
- **Email:** rkeerthana2312@gmail.com
- **Phone:** +91 912-350-0196

Thank you!

