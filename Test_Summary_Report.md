# Test Summary Report . Restful Booker QA Project

## Project Name
Restful Booker QA Project

## Test Scope
Manual and API testing for core booking flows:
- Create Booking
- Get Booking
- Update Booking
- Delete Booking
- Positive scenarios
- Negative scenarios
- Edge case scenarios
- Authentication scenarios

## Tools Used
- Postman
- Jira
- Google Sheets
- GitHub

## Test Execution Summary
Total Test Cases: 30
Passed: 15
Failed: 15
Not Run: 0

## Bugs Found
- KAN-4 . Create Booking allows missing lastname
- KAN-5 . Create Booking allows invalid checkin date value
- KAN-6 . Create Booking returns 500 when booking date field is missing
- KAN-7 . Create Booking allows checkout date before checkin date
- KAN-8 . Create Booking allows negative total price
- KAN-9 . Create Booking allows empty firstname
- KAN-10 . Create Booking allows special characters in firstname
- KAN-11 . Create Booking allows very long firstname
- KAN-12 . Create Booking allows invalid date format
- KAN-14 . Create Booking allows empty string fields
- KAN-15 . Create Booking allows totalprice value 0
- KAN-16 . Create Booking returns 500 when totalprice field is missing
- KAN-17 . Create Booking returns 500 when depositpaid field is missing
- KAN-18 . Create Booking allows invalid depositpaid value

## Risks
The Create Booking endpoint allows several invalid or incomplete input values, including missing fields, invalid date values, invalid date order, negative price, empty firstname, special characters, and very long firstname values.

Some invalid requests return 200 OK and create a booking instead of returning a validation error. In missing booking date field scenarios, the API returns 500 Internal Server Error instead of a controlled client-side validation response.

## Conclusion
Core booking flows such as create, get, update, delete, and authentication-related negative scenarios were tested successfully.

Negative and edge case testing found multiple validation issues in the Create Booking endpoint. The main risk is that the API accepts invalid booking data or returns incorrect error handling behavior instead of rejecting invalid requests with a clear validation response.
