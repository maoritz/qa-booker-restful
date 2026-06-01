# Bug Reports . Restful Booker QA Project

## BUG-001 . Create Booking allows missing lastname

**Jira ID:** KAN-4  
**Related Test Case:** TC-005  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Remove the lastname field from the request body.
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
2. Fill in all required booking fields with valid data.
3. Set checkin date to an invalid value.
4. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with invalid checkin date value.  
Response returned a valid bookingid.

---

## BUG-003 . Create Booking returns 500 when booking date field is missing

**Jira ID:** KAN-6  
**Related Test Cases:** TC-010, TC-011  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Send a Create Booking request with the checkin field missing.
3. Send another Create Booking request with the checkout field missing.
4. Keep all other required fields valid.

### Expected Result
API should return 400 Bad Request or a validation error.  
Booking should not be created.  
Response should not contain a valid bookingid.

### Actual Result
API returned 500 Internal Server Error.  
Booking was not created.  
No bookingid was returned.

---

## BUG-004 . Create Booking allows checkout date before checkin date

**Jira ID:** KAN-7  
**Related Test Case:** TC-012  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set checkin date to a later date.
3. Set checkout date to an earlier date.
4. Keep all other required fields valid.
5. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with checkout date before checkin date.  
Response returned a valid bookingid.

---

## BUG-005 . Create Booking allows negative total price

**Jira ID:** KAN-8  
**Related Test Case:** TC-013  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set totalprice to a negative value.
3. Keep all other required fields valid.
4. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with negative total price.  
Response returned a valid bookingid.

---

## BUG-006 . Create Booking allows empty firstname

**Jira ID:** KAN-9  
**Related Test Case:** TC-014  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set firstname to an empty value.
3. Keep all other required fields valid.
4. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with empty firstname.  
Response returned a valid bookingid.

---

## BUG-007 . Create Booking allows special characters in firstname

**Jira ID:** KAN-10  
**Related Test Case:** TC-015  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set firstname with special characters.
3. Keep all other required fields valid.
4. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with special characters in firstname.  
Response returned a valid bookingid.

---

## BUG-008 . Create Booking allows very long firstname

**Jira ID:** KAN-11  
**Related Test Case:** TC-016  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set firstname with more than 100 characters.
3. Keep all other required fields valid.
4. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with a very long firstname.  
Response returned a valid bookingid.

---

## BUG-009 . Create Booking allows invalid date format

**Jira ID:** KAN-12  
**Related Test Case:** TC-017  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Open Postman and select the Create Booking request.
2. Set checkin date with invalid format.
3. Keep all other required fields valid.
4. Click Send.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

---

## BUG-010 . Create Booking allows empty string fields

**Jira ID:** KAN-14  
**Related Test Case:** TC-022  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Send POST /booking request.
2. Set firstname, lastname, and additionalneeds as empty strings.
3. Keep all other required fields valid.
4. Send the request.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with empty string fields.  
Response returned a valid bookingid.

---

## BUG-011 . Create Booking allows totalprice value 0

**Jira ID:** KAN-15  
**Related Test Case:** TC-024  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Send POST /booking request.
2. Set totalprice to 0.
3. Keep all other required fields valid.
4. Send the request.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with totalprice value 0.  
Response returned a valid bookingid.

---

## BUG-012 . Create Booking returns 500 when totalprice field is missing

**Jira ID:** KAN-16  
**Related Test Case:** TC-025  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Send POST /booking request.
2. Remove the totalprice field from the request body.
3. Keep all other required fields valid.
4. Send the request.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 500 Internal Server Error.  
Booking was not created.  
No bookingid was returned.

---

## BUG-013 . Create Booking returns 500 when depositpaid field is missing

**Jira ID:** KAN-17  
**Related Test Case:** TC-026  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Send POST /booking request.
2. Remove the depositpaid field from the request body.
3. Keep all other required fields valid.
4. Send the request.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 500 Internal Server Error.  
Booking was not created.  
No bookingid was returned.

---

## BUG-014 . Create Booking allows invalid depositpaid value

**Jira ID:** KAN-18  
**Related Test Case:** TC-027  
**Severity:** Medium  
**Priority:** Medium  
**Status:** To Do  

### Steps to Reproduce
1. Send POST /booking request.
2. Set depositpaid to an invalid value: "yes".
3. Keep all other required fields valid.
4. Send the request.

### Expected Result
API returns 400 Bad Request or a validation error.  
Booking is not created.  
Response does not contain a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with invalid depositpaid value.  
Response returned a valid bookingid.

### Actual Result
API returned 200 OK.  
Booking was created successfully with invalid date format.  
Response returned a valid bookingid.
