**Defect** ID: D001 - System Accepts Negative Quantity in Fuel Purchase 

Severity: High
Priority: High

Summary: The application allows the user to submit a fuel purchase with a negative quantity via the UI, resulting in an increase in available fuel units instead of rejecting the input. The impact here is that this allows invalid transactions, can be exploited to increase stock indefinitely, and is a business-critical defect affecting data integrity and financial logic.

Steps to Reproduce:
1. Go to "Buy Energy" page.
2. Select any valid fuel type (e.g., Gas).
3. Enter -1 in the Number of Units Required field.
4. Click the "Buy" button.
5. Observe the confirmation message and fuel unit count.

Expected Result:
1. The system should prevent submission and display a validation error (e.g., "Quantity must be greater than 0").
2. No order should be created.
3. Fuel unit count should remain unchanged.

Actual Result:
1. The order is processed successfully with -1 quantity.
2. Confirmation message is shown: “You have purchased -1 m³ at a cost of [amount].”
3. Fuel unit count increases by 1 instead of decreasing.

Evidence:
1. Screenshot of the filled form with -100 as quantity: screenshots/negative_quantity_input.png
2. Screenshot of the error message -> screenshots/negative_quantity_confirmation_message.png
3. Screenshot of the quantity change on the 'Buy' screen -> screenshots/negative_quantity_units_change.png
