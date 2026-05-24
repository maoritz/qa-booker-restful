# Bug Reports . Restful Booker QA Project

## BUG-001 . Create Booking allows missing firstname

**Jira ID:** KAN-4  
**Related Test Case:** TC-005  
**Severity:** Medium  
**Priority:** Medium  
**Status:** In Progress  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Remove the firstname field from the request body.
3. Keep all other required fields valid.
4. Click Send.

### Expected Result
Booking should not be created.  
API should return an error response or validation message.  
Response should not contain a valid bookingid.

### Actual Result
Booking was created successfully.  
Response returned a valid bookingid.

---

## BUG-002 . Create Booking allows invalid checkin date value

**Jira ID:** KAN-5  
**Related Test Case:** TC-009  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set the method to POST.
3. Fill in all required booking fields with valid data.
4. Set Check-in Date to "not-a-date".
5. Keep all other required fields valid.
6. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with invalid checkin date value.  
Response returned a valid bookingid.
