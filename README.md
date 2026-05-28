# Restful Booker Manual & API QA Project

## About
This project demonstrates manual and API testing of the Restful Booker API.

The goal of the project is to verify core booking functionality, test negative and edge case scenarios, document defects, and track failed test cases using Jira.

## Tested Features
- Create Booking
- Get Booking by ID
- Update Booking
- Delete Booking
- Authentication
- Negative input validation
- Edge case scenarios

## Tools Used
- Postman
- Jira
- Google Sheets
- GitHub

## Test Execution Summary
- Total Test Cases: 19
- Passed: 9
- Failed: 10
- Not Run: 0

## Bugs Found
The project includes documented Jira bugs from KAN-4 to KAN-12.

Main issues found:
- Missing required fields are accepted or handled incorrectly
- Invalid date values are accepted
- Missing booking date fields return 500 Internal Server Error
- Checkout date before checkin date is accepted
- Negative total price is accepted
- Empty firstname is accepted
- Special characters in firstname are accepted
- Very long firstname is accepted

## Repository Files
- `Test_Cases.xlsx` . Full test cases with expected results, actual results, status, and Jira bug traceability
- `Bug_Reports.md` . Documented bug reports with steps to reproduce, expected result, actual result, severity, and priority
- `Test_Summary_Report.md` . Summary of test execution, bugs found, risks, and conclusion
- `Postman Collection` . API requests used during testing
- `evidence/` . Screenshots and evidence from Jira and test documentation

## Traceability
Failed test cases are linked to Jira bugs using the `Jira Bug` column in `Test_Cases.xlsx`.

Example:
- TC-015 -> KAN-10
- TC-016 -> KAN-11
- TC-017 -> KAN-12

## Conclusion
Core booking flows were tested successfully, including create, get, update, delete, and authentication-related scenarios.

Negative and edge case testing found multiple validation issues in the Create Booking endpoint. These issues were documented in Jira and linked back to the relevant failed test cases.
