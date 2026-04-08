### 📋 User Registration Checklist
This checklist covers the functional testing of the User Registration module.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Register with valid credentials | User is registered and redirected to dashboard | High |
| 2 | Register with already existing email | Error message: "Email already exists" | High |
| 3 | Password length validation (min 8 chars) | Error message if less than 8 characters | Medium |
| 4 | Leave mandatory fields empty | Form should not submit, highlight empty fields | High |
| 5 | Verify "Terms & Conditions" checkbox | Cannot register without checking the box | Medium |
