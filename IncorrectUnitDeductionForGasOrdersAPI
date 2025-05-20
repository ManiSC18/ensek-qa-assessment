Endpoint: PUT /buy/1/5

Description: Each time a gas order is placed, the ordered quantity becomes the deducted amount, instead of subtracting the correct value from the inventory.

Expected Result: Inventory should reduce by the fixed amount (e.g., 5 units per order).

Actual Result: Inventory appears to be calculated by subtracting the newly purchased quantity from the quantity just purchased, not the previous remaining inventory.

e.g. first order:
{
  "message": "You have purchased 1456 m³ at a cost of 1.7 there are 5 units remaining."
}

second order:

{
  "message": "You have purchased 1451 m³ at a cost of 1.7 there are 5 units remaining."
}

