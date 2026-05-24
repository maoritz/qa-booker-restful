# Test Summary Report . Restful Booker QA Project

## Project Name
Restful Booker QA Project

## Test Scope
Manual and API testing for core booking flows:
- Create Booking
- Get Booking
- Update Booking
- Delete Booking
- Negative and edge case scenarios

## Tools Used
- Postman
- Jira
- Google Sheets
- GitHub

## Test Execution Summary
Total Test Cases: 9  
Passed: 7  
Failed: 2  
Not Run: 0  

## Bugs Found
- KAN-4 . Create Booking allows missing firstname
- KAN-5 . Create Booking allows invalid checkin date value

## Risks
The API allows invalid or incomplete booking data in some create booking scenarios.

## Conclusion
Core booking flows passed successfully, but negative testing found validation issues in the Create Booking endpoint.
