# 🐛 Comprehensive Bug Reports Collection

This document contains a collection of identified defects across various web and mobile applications, categorized by their impact and type.

---

### [BUG-001] Profile Picture Upload fails without error message
**Severity:** Medium | **Priority:** Medium | **Status:** Open
* **Description:** System hangs on "Uploading..." state when a file exceeds 5MB.
* **Steps:** Log in > Profile Settings > Change Photo > Select 10MB+ file.
* **Actual Result:** Infinite loading state, no error message.
* **Expected Result:** Error message: "File size exceeds the 5MB limit."

---

### [BUG-002] OTP Auto-fill functionality is not working on iOS
**Severity:** Minor | **Priority:** Medium | **Status:** Open
* **Environment:** iPhone 12 Pro Max (iOS 26.3)
* **Description:** Incoming SMS OTP code is not suggested or auto-filled by the system.
* **Steps:** Open ODIN > Identomat > Enter Data > Save & Continue > Receive SMS.
* **Actual Result:** Code is received but not detected by the input field.
* **Expected Result:** System should suggest the code for auto-fill.

---

### [BUG-003] Generic "Bad Request" error on Invalid Email
**Severity:** Minor | **Priority:** Medium | **Status:** Open
* **Environment:** iPhone 13 (iOS 26.2)
* **Description:** System shows a technical error instead of a user-friendly validation message.
* **Steps:** Open Morbed > Registration > Enter invalid email (testmail.com) > Register.
* **Actual Result:** Pop-up says "Bad Request".
* **Expected Result:** Pop-up should say "Please enter a valid email" and the field should turn red.

---

### [BUG-004] Keyboard overlaps UI elements on Authorization screen
**Severity:** Medium | **Priority:** High | **Status:** Open
* **Environment:** iPhone 13 (iOS 26.3)
* **Description:** Keyboard covers the "Log In" button and lower input fields.
* **Steps:** Open Morbedi > Go to Login > Tap on Password field.
* **Actual Result:** Keyboard covers the button; screen doesn't scroll up.
* **Expected Result:** View should scroll up so all elements remain visible.

---

### [BUG-005] User can register with a Future Date of Birth (Logic Bug)
**Severity:** Medium | **Priority:** High | **Status:** Open
* **Description:** The system allows registration for users with birth dates in the future.
* **Steps:** Registration > Date of Birth > Select "2027" > Submit.
* **Actual Result:** Registration successful.
* **Expected Result:** Validation error: "Birth date cannot be in the future."

---

### [BUG-006] Search Results disappear after Screen Rotation (UI/UX)
**Severity:** Minor | **Priority:** Low | **Status:** Open
* **Description:** Rotating the device from Portrait to Landscape clears the search results.
* **Steps:** Search for any item > View results > Rotate phone to Landscape mode.
* **Actual Result:** Search results disappear, and the user is taken back to the empty search bar.
* **Expected Result:** Search results should remain visible and adjust to the new screen orientation.

---

### [BUG-007] "Resend OTP" button is active immediately (Spam Risk)
**Severity:** Medium | **Priority:** Medium | **Status:** Open
* **Description:** Users can click "Resend" infinitely without any time delay.
* **Steps:** Request OTP > Immediately click "Resend" 10 times.
* **Actual Result:** 10 different SMS messages are sent.
* **Expected Result:** Button should be disabled for 60 seconds after the first click to prevent SMS spam/costs.
