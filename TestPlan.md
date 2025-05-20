ENSEK Software Tester Assessment - Task 1: Test Plan Creation

1. Objectives:
   - To validate the core functionality and behaviour of the Demo ENSEK platform through:
       - Functional and Exploratory UI Testing
       - Targeted API test automation using the given endpoints on Swagger
    
2. Test Scope:
   - Included:
       - Home page UI navigation
       - Buy Energy flow (both through UI and API)
       - API-based order verification (/orders)
       - Handling of multiple energy types
       - Error handlings (e.g. Invalid Buys)
    
   - Out of scope:
       - Backend validation through DB
       - Authorization tests (since there are no login tokens)
       - Restricted /reset endpoint (returns 401 on swagger)
    
3. Test Types:
   - Functional Testing (UI and API)
   - Exploratory Testing
   - Negative Testing
   - Basic automation via Postman Collection
  
4. Test Scenarios:
  | ID  | Scenario Description                                   | Type           |
  | --- | ------------------------------------------------------ | -------------- |
  | TC1 | Verify navigation menu buttons (Home, About, Contact)  | UI Functional  |
  | TC2 | Verify Buy Energy page loads and allows input          | UI Functional  |
  | TC3 | Place order via Buy button (valid fuel + quantity)     | UI + API       |
  | TC4 | Attempt to buy with invalid data (e.g., negative qty)  | UI Negative    |
  | TC5 | Verify `/orders` returns all orders with expected info | API Validation |
  | TC6 | Buy multiple fuel types and confirm order count        | API Functional |
  | TC7 | Attempt `/reset` and handle 401 gracefully             | API (Skipped)  |

5. Tools and Technologies
   - Postman - API Test Execution and Assertions
   - Github - For Version Control and Submission
  
6. Assumptions:
   - /reset endpoint is not available to candidate users
   - No login or token based auth is required for valid endpoints
   - Test environment data may persist across test runs (unless reset through UI)
  
7. Defect Reporting:
   - Defects are recorded manually with:
        - Title
        - Steps to reproduce
        - Expected v Actual result
        - Screenshots or API responses
    
8. Test Evidence:
   - Screenshots stored in /screenshots/
   - API Test results in /api-tests/
   - Collection shared as .json in /postman-collection/

