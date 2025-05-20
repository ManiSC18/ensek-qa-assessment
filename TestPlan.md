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
  
4. Test Scenarios (Examples):
TC1: Verify that all top menu navigation buttons ('Home', 'About', 'Contact', 'Register', 'Login') are clickable and lead to the correct pages. (UI Navigation / Functional Test)
TC2: Verify that the 'Buy Energy' button navigates to the correct page and displays fuel types and quantity input fields. (UI Functional Test)
TC3: Place a valid fuel order (e.g. select fuel type and positive quantity) and confirm that a success message with order ID is shown. (UI + API Integration Test)
TC4: Attempt to buy fuel with invalid input (e.g. zero or negative quantity) and verify appropriate error handling. (UI Negative Test)
TC5: Use the /orders API endpoint to verify that previous purchases are listed with correct fuel type, quantity, and timestamp. (API Functional Test)
TC6: Place multiple orders of different fuel types and confirm that all are reflected in /orders with accurate data. (API Validation Test)
TC7: Attempt to access the /reset endpoint and note that it returns 401 Unauthorized — assume it's not accessible to candidates. (API Security / Exploratory Test)

6. Tools and Technologies
   - Postman - API Test Execution and Assertions
   - Github - For Version Control and Submission
  
7. Assumptions:
   - /reset endpoint is not available to candidate users
   - No login or token based auth is required for valid endpoints
   - Test environment data may persist across test runs (unless reset through UI)
  
8. Defect Reporting:
   - Defects are recorded manually with:
        - Title
        - Steps to reproduce
        - Expected v Actual result
        - Screenshots or API responses
    
9. Test Evidence:
   - Screenshots stored in /screenshots/
   - API Test results in /api-tests/
   - Collection shared as .json in /postman-collection/

