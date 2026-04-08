# 📋 Test Case Checklists

This document contains functional verification scenarios for core application modules.

---

## 1. User Registration Checklist
| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Register with valid credentials | User is registered and redirected to dashboard | High |
| 2 | Register with already existing email | Error message: "Email already exists" | High |
| 3 | Password length validation (min 8 chars) | Error message if less than 8 characters | Medium |
| 4 | Leave mandatory fields empty | Form should not submit, highlight empty fields | High |
| 5 | Verify "Terms & Conditions" checkbox | Cannot register without checking the box | Medium |

---

## 2. Login Page Checklist
| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Login with valid email and password | User is logged in and redirected to home page | High |
| 2 | Login with invalid password | Error message: "Invalid credentials" | High |
| 3 | Login with non-registered email | Error message: "User not found" | High |
| 4 | "Show Password" icon functionality | Password becomes visible/masked when clicked | Medium |
| 5 | Verify "Remember Me" checkbox | User session is saved after closing browser | Low |

---

## 3. OTP Verification Checklist
| Step | Requirement / Test Case | Expected Result | Priority |
| :--- | :--- | :--- | :--- |
| 1 | Enter valid OTP | User is verified and proceeds to next step | High |
| 2 | Enter invalid/wrong OTP | Error message: "Invalid code" | High |
| 3 | Enter expired OTP | Error message: "Code has expired" | High |
| 4 | Re-use already used OTP | Error message: "Code already used" | High |
| 5 | Resend OTP functionality | New code is sent, old code becomes invalid | High |
| 6 | Enter OTP with No Internet | Error message: "Check your internet connection" | High |
| 7 | Multi-device OTP entry | OTP should work only on the requesting device | Medium |
