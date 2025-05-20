Endpoint: PUT /buy/4/5

Description: System allows a purchase of oil even when inventory is insufficient, resulting in negative unit count.

Expected Result: Request should be blocked with an appropriate error (e.g., "Insufficient stock"). Inventory should never go below 0.

Actual Result: Request is processed, and response shows negative units remaining.

{
  "message": "You have purchased 5 Litres at a cost of 3.0 there are -25 units remaining. Your orderid is ff38396a-5574-42f2-9770-d4ff60af6b61."
}
