### 📋 User Registration Checklist
This checklist covers the functional testing of the User Registration module.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Register with valid credentials | User is registered and redirected to dashboard | High |
| 2 | Register with already existing email | Error message: "Email already exists" | High |
| 3 | Password length validation (min 8 chars) | Error message if less than 8 characters | Medium |
| 4 | Leave mandatory fields empty | Form should not submit, highlight empty fields | High |
| 5 | Verify "Terms & Conditions" checkbox | Cannot register without checking the box | Medium |

Step,Requirement / Test Case,Expected Result,Priority
1,Login with valid email and password,User is logged in and redirected to home page,High
2,Login with invalid password,"Error message: ""Invalid credentials""",High
3,Login with non-registered email,"Error message: ""User not found""",High
4,"""Show Password"" icon functionality",Password becomes visible/masked when clicked,Medium
5,"Verify ""Remember Me"" checkbox",User session is saved after closing browser,Low
6,Leave email or password field empty,System shows validation error for required fields,High



