Defect: Unable to Test `POST /reset` Endpoint due to Missing Authorization

Summary:  
The `POST /reset` endpoint requires Bearer token authentication, but no valid token or method of obtaining one is provided in the Swagger documentation or exercise instructions.

Steps to Reproduce:  
1. Attempt to execute the `POST /reset` endpoint via Swagger or Postman.
2. Observe the 401 Unauthorized response.
3. Check Swagger UI for authentication requirements.

Observed Behavior:  
- Swagger displays an "Authorize" button requesting a Bearer token.
- Calls to the endpoint return: Status: 401 Unauthorized

Expected Behavior:  
- The endpoint should be accessible for testing purposes, or a valid token should be provided to allow authentication.

Impact:  
- Unable to validate the reset functionality as required by the exercise.
- Test automation involving test data reset cannot be completed.

Recommendation:  
- Provide a valid Bearer token or instructions on how to retrieve one for authenticated testing.

