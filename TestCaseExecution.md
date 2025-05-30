Test Case Execution, Test Case 4 (TC4): Buy Energy with Invalid Input (Negative Quantity)

Test Case ID: TC4
Title: Attempt to buy fuel with invalid input (negative quantity)
Test Type: UI Negative Test
Objective:
To verify that the application handles invalid input (negative fuel quantity) gracefully and prevents the transaction.

Steps Taken:
1. Navigated to the "Buy Energy" page from the homepage.
2. Selected a valid fuel type (e.g., Gas).
3. Entered an invalid quantity: -100 in the 'Number of Units Required' text input
4. Clicked the "Buy" button.

Expected Result:
1. An error message should be displayed on the UI indicating that the quantity is invalid
2. No order should be processed.

Actual Result:
1. No error message was shown, instead, a success message was shown 'Thank you for your purchase of -100 units of Gas We have popped it in the post and it will be with you shortly.
There are now 3100 units of Gas left in our stores.'
2. The negative input was allowed, and the number of units of gas were incremented by 100.

Evidence:
1. Screenshot of the filled form with -100 as quantity: screenshots/negative_quantity_input.png
2. Screenshot of the error message -> screenshots/negative_quantity_confirmation_message.png
3. Screenshot of the quantity change on the 'Buy' screen -> screenshots/negative_quantity_units_change.png
