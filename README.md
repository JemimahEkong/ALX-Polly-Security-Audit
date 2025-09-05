# ALX-Polly-Security-Audit
# ALX Polly - Security Audit

## Overview

This project involves conducting a security audit on the **ALX Polly** application, identifying security vulnerabilities, and applying necessary fixes to ensure that the application is secure and robust. The purpose of this exercise is to provide an understanding of common security flaws in modern web applications and how to mitigate them.

### Key Features:
- **User Authentication**: Secure login and registration.
- **Poll Creation and Sharing**: Users can create polls and share them securely.

---

## Security Flaws Identified & Fixed

During the audit, the following security flaws were identified and fixed:

### 1. **Password Handling**
   - **Flaw**: Weak password storage without hashing.
   - **Fix**: Implemented **password hashing** using **bcrypt** to securely store user passwords, ensuring they are never saved in plaintext.

### 2. **Input Validation**
   - **Flaw**: Lack of proper input validation on user input (e.g., email and password).
   - **Fix**: Added proper validation for **email format** and **password strength**. This prevents invalid or malicious data from being submitted.

### 3. **Cross-Site Scripting (XSS)**
   - **Flaw**: Potential for **XSS attacks** via unsanitized user input.
   - **Fix**: Implemented HTML sanitization and ensured proper encoding of user input to prevent malicious scripts from being executed.

### 4. **SQL Injection**
   - **Flaw**: Potential vulnerability to **SQL injection** due to improper handling of user data in queries.
   - **Fix**: Ensured that all SQL queries are parameterized, which prevents attackers from injecting malicious SQL code.

### 5. **Cross-Site Request Forgery (CSRF)**
   - **Flaw**: No protection against CSRF attacks.
   - **Fix**: Added **CSRF tokens** to forms to ensure that requests are made by the authenticated user and not a malicious third party.

### 6. **Session Management**
   - **Flaw**: Insecure session management.
   - **Fix**: Implemented **secure session cookies** with the `HttpOnly` and `Secure` flags to protect against session hijacking.



