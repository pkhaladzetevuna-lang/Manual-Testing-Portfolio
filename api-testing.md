# 📡 API Testing & Postman Assertions

This section demonstrates my expertise in API testing using Postman, including automated test scripts (JavaScript) to validate responses.

---

## 🛠 Automated Test Scripts in Postman
I use the **Tests** tab in Postman to write JavaScript assertions. This ensures that every request meets the expected criteria automatically.

### 1. Status Code & Response Time Validation
**Scenario:** Verify that the API responds successfully and quickly.
```javascript
// Check if status code is 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

// Check if response time is below 500ms
pm.test("Response time is less than 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
2. JSON Body & Data Integrity
Scenario: Verify that the returned user data contains the correct fields and values.

JavaScript
pm.test("Verify User Data", function () {
    var jsonData = pm.response.json();
    
    // Check if ID is correct
    pm.expect(jsonData.id).to.eql(101);
    
    // Check if email field exists
    pm.expect(jsonData).to.have.property("email");
    
    // Verify specific value
    pm.expect(jsonData.status).to.eql("active");
});
3. Schema Validation
Scenario: Ensure the response structure strictly follows the API documentation.

JavaScript
var schema = {
    "type": "object",
    "required": ["id", "username", "email"],
    "properties": {
        "id": { "type": "number" },
        "username": { "type": "string" },
        "email": { "type": "string" }
    }
};

pm.test("Response schema is valid", function () {
    pm.response.to.have.jsonSchema(schema);
});
4. Setting Environment Variables
Scenario: Automatically save a Token from a Login response to use it in future requests.

JavaScript
var jsonData = pm.response.json();
pm.environment.set("auth_token", jsonData.token);
console.log("Token has been saved successfully!");
🧪 Collection Runner & Reporting
I use Postman Collection Runner to execute all tests at once and ensure the entire API suite passes without regressions.

Positive Testing: Validating successful requests (200 OK, 201 Created).

Negative Testing: Validating error handling (400 Bad Request, 401 Unauthorized, 404 Not Found).
