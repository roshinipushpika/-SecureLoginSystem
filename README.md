# Secure Login System

## Project Overview

The Secure Login System is a web-based authentication application developed using Python Flask and SQLite. The application provides secure user registration and login functionality with password hashing, session management, and protection against common cyber attacks such as SQL Injection.

This project demonstrates the implementation of important cyber security practices used in modern web applications to ensure secure authentication and controlled user access.



# Objective

The objective of this project is to design and develop a secure login web application that:

- Allows users to register and login securely
- Stores encrypted passwords using bcrypt hashing
- Prevents SQL Injection attacks
- Maintains secure user sessions
- Restricts unauthorized access to protected pages



# Key Features

## User Registration

Users can create a new account by providing:
- Username
- Email Address
- Password

The application validates user input before storing the data.



## Secure Login Authentication

Registered users can securely login using valid credentials.

The system verifies encrypted passwords using bcrypt hashing.

Example:

```python
hashed_password = bcrypt.generate_password_hash(password).decode("utf-8")
```



## Password Hashing using bcrypt

Passwords are never stored in plain text format.

The application uses Flask-Bcrypt to hash passwords before saving them in the database.

---

## SQL Injection Protection

Parameterized SQL queries are used to prevent malicious SQL Injection attacks.

Example:

```python
conn.execute(
    "SELECT * FROM users WHERE email = ?",
    (email,)
)
```



## Input Validation

The application validates:
- Empty fields
- Email format
- Password length

This helps reduce invalid and malicious input.

---

## Session Management

Secure sessions are created after successful login.

Only authenticated users can access protected pages.

---

## Logout Functionality

Users can securely logout and destroy active sessions.



## Protected Dashboard

Unauthorized users cannot directly access the dashboard page without logging in.



# Cyber Security Concepts Implemented

The project implements multiple cyber security techniques including:

- Authentication
- Authorization
- Password Hashing
- Session Security
- Access Control
- SQL Injection Prevention
- Secure User Validation
- Protected Resource Access



# Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend Development |
| Flask | Web Framework |
| SQLite | Database Management |
| Flask-Bcrypt | Password Hashing |
| HTML | Frontend Structure |
| CSS | User Interface Styling |



# Project Structure

```text
SecureLoginSystem/
│
├── app.py
├── database.py
├── requirements.txt
│
├── templates/
│   ├── register.html
│   ├── login.html
│   └── dashboard.html
│
└── static/
    └── style.css
```



# Installation and Execution

## Step 1: Install Required Packages

```bash
py -m pip install -r requirements.txt
```



## Step 2: Create Database

```bash
py database.py
```



## Step 3: Run Application

```bash
py app.py
```



## Step 4: Open Browser

```text
http://127.0.0.1:5000
```



# System Workflow

## Registration Process

1. User enters registration details
2. Input validation is performed
3. Password is hashed using bcrypt
4. User data is securely stored in SQLite database



## Login Process

1. User enters login credentials
2. Database verifies email
3. bcrypt verifies password hash
4. Secure session is created
5. User is redirected to dashboard



## Logout Process

1. Session data is cleared
2. User is redirected to login page



# Security Mechanisms Used

## Password Encryption

bcrypt hashing protects user passwords from exposure.

## SQL Injection Prevention

Parameterized queries prevent malicious database attacks.

## Session-Based Authentication

Authenticated sessions restrict unauthorized access.

## Input Validation

User input is validated before processing.



# Screenshots Included

The following screenshots are included for project demonstration:

- Project Folder Structure
- Flask Server Running
- Registration Page
- Successful Registration
- Login Page
- Dashboard Page
- Logout Page



# Expected Outcome

The Secure Login System securely manages user authentication using encrypted passwords, session management, and secure database operations. The system helps reduce unauthorized access and protects users against common cyber security threats such as SQL Injection and credential exposure.



# Developed By

Roshini Pushpika
