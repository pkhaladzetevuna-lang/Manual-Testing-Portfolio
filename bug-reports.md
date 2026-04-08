# 🐛 Bug Report: Profile Picture Upload Issue

### [BUG-001] Profile Picture Upload fails without error message for large files

---

## 📝 Description
When a user attempts to upload a profile picture larger than the allowed limit (5MB), the system stays in an infinite "Uploading..." state. No error message is displayed to inform the user about the file size limit.

| Attribute | Details |
| :--- | :--- |
| **Severity** | Medium |
| **Priority** | High |
| **Status** | Open |
| **Type** | Functional Bug |

---

## 🚀 Steps to Reproduce
1. Log in to the application with valid credentials.
2. Navigate to the **Profile Settings** page.
3. Click on the **"Change Photo"** button.
4. Select a JPEG/PNG file larger than 10MB (e.g., `test_large_image.jpg`).
5. Click **"Open/Upload"** and observe the behavior.

---

## 🔍 Expected Result
The system should validate the file size and display a clear error message: 
> *"File size exceeds the 5MB limit. Please upload a smaller file."*

## ❌ Actual Result
The button changes to **"Uploading..."** and stays in that state indefinitely. The user interface becomes unresponsive, and no error message appears.

---

## 💻 Environment
* **OS:** Windows 11
* **Browser:** Google Chrome (Version 122.0.6261.129)
* **Screen Resolution:** 1920x1080

---

## 📸 Attachments
*(Note: In a real project, you would attach a screenshot or screen recording here showing the infinite loading state.)*

---

### 🐛 Bug #6: Keyboard overlaps UI elements on Authorization screen
**Severity:** Medium | **Priority:** High | **Status:** Open

**Description:**
On the Authorization screen, when the keyboard opens, it overlaps the input fields and the "Log In" button, preventing the user from seeing what they are typing or proceeding.

**Environment:**
* **Device:** iPhone 13
* **OS:** iOS 26.3
* **Frequency:** 100%

**Steps to Reproduce:**
1. Open the **Morbedi** application.
2. Navigate to the **Authorization / Login** screen.
3. Tap on any input field (Email or Password) to start typing.
4. Observe the keyboard behavior and the UI.

**Actual Result:**
The keyboard covers the lower half of the screen, including the "Log In" button and the bottom input field. The view does not scroll up to accommodate the keyboard.

**Expected Result:**
The UI should be responsive. When the keyboard is active, the view should automatically scroll up or adjust so that all input fields and the action button remain visible above the keyboard.
