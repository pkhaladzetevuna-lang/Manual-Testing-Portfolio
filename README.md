# 🚀 Manual Testing Portfolio
Welcome to my QA portfolio. Here you can find my test documentation for various web applications.

---

### 📋 1. User Registration Checklist
This checklist covers the functional testing of the User Registration module.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Register with valid credentials | User is registered and redirected to dashboard | High |
| 2 | Register with already existing email | Error message: "Email already exists" | High |
| 3 | Password length validation (min 8 chars) | Error message if less than 8 characters | Medium |
| 4 | Leave mandatory fields empty | Form should not submit, highlight empty fields | High |
| 5 | Verify "Terms & Conditions" checkbox | Cannot register without checking the box | Medium |

---

### 📋 2. Login Page Checklist
This checklist covers the user authentication process.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Login with valid email and password | User is logged in and redirected to home page | High |
| 2 | Login with invalid password | Error message: "Invalid credentials" | High |
| 3 | Login with non-registered email | Error message: "User not found" | High |
| 4 | "Show Password" icon functionality | Password becomes visible/masked when clicked | Medium |

---

### 📋 3. Forgot Password Checklist
This checklist covers the password recovery functionality.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Submit valid registered email | Recovery email is sent to the user | High |
| 2 | Submit invalid/wrong email format | Error message: "Please enter a valid email" | Medium |
