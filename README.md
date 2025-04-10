# hospital-appointment-management-system
Hospital Appointment Management System is a web-based Java project that allows admin to manage patients, appointments, and hospital data securely using JSP, Servlet, and MySQL.


Here's a complete README.md for your Hospital Appointment Management System (JSP + Servlet + MySQL + Tomcat 10 + Maven + NetBeans):

# Hospital Appointment Management System

A complete Admin-Patient based Hospital Appointment Management System developed using:
- Java (JSP + Servlet)
- Apache Tomcat 10+
- MySQL Database
- Maven Project Structure
- NetBeans IDE (Recommended)

---

## Features

- Admin Login / Dashboard
- Manage Appointments
- Patient Management
- Secure Login with Session Management
- Responsive UI with Custom CSS
- Clean JSP Pages

---

## Requirements

- NetBeans IDE with Apache Tomcat 10+
- MySQL Server
- Maven installed (NetBeans handles automatically)

---

## Project Setup Guide

### 1. Import Project in NetBeans
1. Open NetBeans → File → Open Project
2. Select this folder: `HospitalAppointmentManagement_Updated`
3. Clean & Build the project.

---

### 2. MySQL Database Setup

#### Create Database & Tables:
Open MySQL Command Line or phpMyAdmin → Execute:

```sql
CREATE DATABASE hospital_db;

USE hospital_db;

CREATE TABLE admin (
  id INT PRIMARY KEY AUTO_INCREMENT,
  name VARCHAR(100),
  email VARCHAR(100),
  password VARCHAR(100)
);

INSERT INTO admin (name, email, password) VALUES ('Admin', 'admin@gmail.com', 'admin123');
(Add other tables like patient, appointments as per your project structure.)

3. Database Configuration in Project
Go to → src/main/java/dao/DBConnect.java

Update:

String url = "jdbc:mysql://localhost:3306/hospital_db";
String username = "root";
String password = "my_password";
(Use your MySQL credentials)

4. Run Project in Tomcat
Right Click → Run

OR Deploy Manually in Apache Tomcat 10's webapps folder.

Access:
http://localhost:8080/HospitalAppointmentManagement_Updated/
Admin Login Credentials (Default)
Email	Password
admin@gmail.com	admin123
Folder Structure
bash
Copy
Edit
src/
 ├── main/
 │   ├── java/dao/
 │   ├── java/entities/
 │   ├── java/servlets/
 │   └── webapp/
 │        ├── jsp/
 │        └── css/js
pom.xml
Debugging / Logs
Check server logs in NetBeans Console

Or check:

<tomcat-installation>/logs/catalina.out
Notes
Recommended Java Version: 17+

Apache Tomcat: 10+

Database: MySQL 8+

IDE: NetBeans 15+

Author
Made with ❤️ by Mayank Aneja


License
This project is for educational purposes only.
