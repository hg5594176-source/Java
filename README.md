# Java Projects & Assignments

This repository contains Java-based academic and laboratory projects, covering core Java database connectivity (JDBC with MySQL) as well as modern backend web services using Spring Boot REST APIs.

---

## 📁 Repository Structure

```text
Java/
├── EmployeeManagement/            # Spring Boot REST API for Employee Management (CO5)
├── HostelManagement-JDBC/         # Menu-driven JDBC application for Hostel Management
├── HostelManagement-SpringBoot/   # Spring Boot REST API for Hostel Management
├── InventoryManagement/           # Menu-driven JDBC application for Product Inventory (CO4)
├── .gitignore
└── README.md
```

---

## 🛠️ Prerequisites

- **Java Development Kit (JDK)**: Java 17 or higher
- **Database**: MySQL Server 8.0+
- **Build Tool**: Apache Maven (included wrapper `mvnw` where applicable)
- **IDE**: IntelliJ IDEA / Eclipse / VS Code
- **API Testing**: Postman or Curl

---

## 🚀 Projects Overview

### 1. Hostel Management System – JDBC & MySQL
**Directory:** [`HostelManagement-JDBC/`](./HostelManagement-JDBC)  
**Tech Stack:** Java, JDBC, MySQL

A menu-driven console application to manage student hostel allocations and fee records.

- **Features:**
  - Insert new student accommodation records
  - Retrieve student details based on hostel name and fee criteria
  - Update hostel fees dynamically
  - Search and modify room allocation details
  - Calculate total fee collections and perform conditional record deletion
- **Database:** `hostel_db`
- **Setup:**
  1. Create database in MySQL:
     ```sql
     CREATE DATABASE hostel_db;
     ```
  2. Configure your MySQL credentials in `HostelManagement-JDBC/src/DBConnection.java`.
  3. Compile and execute `HostelManagement.java`.

---

### 2. Hostel Management System – Spring Boot REST API
**Directory:** [`HostelManagement-SpringBoot/`](./HostelManagement-SpringBoot)  
**Tech Stack:** Java 17, Spring Boot, Spring Data JPA, MySQL, Maven

A RESTful backend service for managing hostel accommodation records.

- **Features & Endpoints:**
  | Method | Endpoint | Description |
  |--------|----------|-------------|
  | `POST` | `/students` | Register a new hostel student |
  | `GET` | `/students` | Fetch all hostel students |
  | `GET` | `/students/{id}` | Fetch student details by ID |
  | `PUT` | `/students/{id}` | Update student hostel information |
  | `DELETE` | `/students/{id}` | Remove student record |
- **Database:** `hostel_db`
- **Setup:**
  1. Ensure `hostel_db` exists in MySQL.
  2. Configure `src/main/resources/application.properties` with your MySQL user/password.
  3. Run the application:
     ```bash
     cd HostelManagement-SpringBoot
     ./mvnw spring-boot:run
     ```

---

### 3. Inventory Management System – JDBC & MySQL
**Directory:** [`InventoryManagement/`](./InventoryManagement)  
**Course Outcome:** CO4  
**Tech Stack:** Java, JDBC, PreparedStatement, MySQL

A menu-driven product inventory application using parameterized SQL queries.

- **Features:**
  - Insert product records securely with `PreparedStatement`
  - Retrieve products by category where quantity is below threshold (< 20)
  - Sort products by price in descending order
  - Update product stock and modify pricing
  - Calculate total inventory evaluation using `SUM(quantity * price)`
  - Delete products only when stock quantity is zero
- **Database:** `retail_db`
- **Setup:**
  1. Create database in MySQL:
     ```sql
     CREATE DATABASE retail_db;
     ```
  2. Update database credentials in `InventoryManagement/src/com/kiet/inventory/DBConnection.java`.
  3. Compile and run `InventoryManagement.java`.

---

### 4. Employee Management System – Spring Boot REST API
**Directory:** [`EmployeeManagement/`](./EmployeeManagement)  
**Course Outcome:** CO5  
**Tech Stack:** Java 17, Spring Boot, Spring Data JPA, Hibernate, MySQL, Maven

A complete REST API demonstrating enterprise layered architecture (Entity, Repository, Controller) for managing employee profiles.

- **REST API Endpoints:**
  | Method | Endpoint | Description |
  |--------|----------|-------------|
  | `POST` | `/employees` | Add a new employee |
  | `GET` | `/employees` | Retrieve list of all employees |
  | `GET` | `/employees/{id}` | Retrieve employee by ID |
  | `PUT` | `/employees/{id}` | Update employee details |
  | `DELETE` | `/employees/{id}` | Delete employee by ID |
- **Database:** `employee_db`
- **Setup:**
  1. Create MySQL database:
     ```sql
     CREATE DATABASE employee_db;
     ```
  2. Configure connection settings in `EmployeeManagement/src/main/resources/application.properties`.
  3. Start the application:
     ```bash
     cd EmployeeManagement
     ./mvnw spring-boot:run
     ```
