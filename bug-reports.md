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
