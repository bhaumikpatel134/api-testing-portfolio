# Negative Test Scenarios

## Invalid Product ID

Request:
GET /products/999999

Expected:
- Product not found response
- No server crash
- Appropriate error handling

## Invalid Query Parameter

Request:
GET /products?limit=-1

Expected:
- Validation response
- No Internal Server Error

## Invalid Product ID Type

Request:
GET /products/abc

Expected:
- Error response
- No Internal Server Error

## Invalid Search Input

Request:
GET /products/search?q=!@#$%

Expected:
- Empty result or validation response
- No server crash
