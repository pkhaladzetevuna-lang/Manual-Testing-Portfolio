# 📁 QA Assets & Test Artifacts

This section contains reusable assets and documentation used during the software testing lifecycle (STLC).

---

## 📊 Test Documentation (External Files)
These files represent the structured approach I take toward comprehensive testing:

* 📥 [**Registration_Checklist.xlsx**](./Registration_Checklist_English.xlsx) — A detailed master checklist covering all edge cases for User Registration.
* 📥 [**API_Collection_Export.json**](./Postman_Collection.json) — Postman collection containing all documented API requests and tests.

---

## 🖼️ Test Evidence & Visuals
Visual documentation is key to effective bug reporting. I maintain organized evidence for every critical defect found.

* **Bug Evidence Folder:** Contains screenshots and screen recordings of identified issues.
* **UI/UX Audits:** Visual comparisons between "Expected Design" (Figma) and "Actual Result" (App).

---

## 🛠️ Test Data (Static Data)
I maintain a set of predefined test data to ensure consistency across different testing environments:

| Data Type | Example Value | Use Case |
| :--- | :--- | :--- |
| **Valid Email** | `test.user@example.com` | Positive Login/Reg |
| **Invalid Email** | `plainaddress` | Validation Testing |
| **Long String** | `LoremIpsum... (255+ chars)` | Boundary Value Testing |
| **SQL Injection** | `' OR 1=1 --` | Basic Security Check |
| **Large Image** | `heavy_asset_10MB.png` | Performance/Upload Testing |

---

## 📑 Templates Used
To maintain high standards, I follow specific templates for my documentation:
1. **Bug Report Template:** Clear Steps, Actual/Expected results, and Environment details.
2. **Test Case Template:** Includes ID, Pre-conditions, Test Steps, and Pass/Fail status.
