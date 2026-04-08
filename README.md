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


---

### 📋 4. OTP (One-Time Password) Verification Checklist
This checklist focuses on the security and functionality of verification codes.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Enter valid OTP | User is verified and proceeds to next step | High |
| 2 | Enter invalid/wrong OTP | Error message: "Invalid code" | High |
| 3 | Enter expired OTP | Error message: "Code has expired" | High |
| 4 | Re-use already used OTP | Error message: "Code already used" | High |
| 5 | Resend OTP multiple times | System should limit frequency (Throttling) | Medium |
| 6 | Copy/Paste OTP with spaces | System should trim spaces and accept the code | Low |
| 7 | Multi-device OTP entry | Same OTP should work only on the device it was requested | Medium |
| 8 | Enter OTP with No Internet | Error message: "Check your internet connection" | High |
| 9 | Rapid "Resend" clicks | Button should be disabled for 60 seconds | Medium |
