



### 📋 Login Page Checklist
This checklist covers the user authentication process.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Login with valid email and password | User is logged in and redirected to home page | High |
| 2 | Login with invalid password | Error message: "Invalid credentials" | High |
| 3 | Login with non-registered email | Error message: "User not found" | High |
| 4 | "Show Password" icon functionality | Password becomes visible/masked when clicked | Medium |
| 5 | Verify "Remember Me" checkbox | User session is saved after closing browser | Low |
| 6 | Leave email or password field empty | System shows validation error | High |

### 📋 Forgot Password Checklist
This checklist covers the password recovery functionality.

| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Submit valid registered email | Recovery email is sent to the user | High |
| 2 | Submit invalid/wrong email format | Error message: "Please enter a valid email" | Medium |
| 3 | Password reset link expiration | Link should not work after 24 hours | High |
| 4 | Set new password with valid criteria | New password is saved, user can login | High |



