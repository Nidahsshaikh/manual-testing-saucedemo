# Bug Report – SauceDemo

## Application Under Test
https://www.saucedemo.com/

---

# BUG_01

## Title
Login error message UI is partially cut inside red container

### Steps to Reproduce
1. Open login page
2. Enter invalid username/password
3. Click Login

### Actual Result
Top and bottom parts of the error message container appear slightly cut.

### Expected Result
Error message should be fully visible inside properly aligned container.

### Severity
Low

### Status
Open

---

# BUG_02

## Title
First Name field accepts numeric values during checkout

### Steps to Reproduce
1. Login to application
2. Add item to cart
3. Proceed to checkout
4. Enter numeric values in First Name field
5. Click Continue

### Actual Result
Checkout accepts numeric values in First Name field.

### Expected Result
First Name field should allow only alphabetic characters.

### Severity
Medium

### Status
Open

---

# BUG_03

## Title
ZIP/Postal Code field accepts alphabetic characters

### Steps to Reproduce
1. Navigate to checkout page
2. Enter alphabetic values in ZIP field
3. Click Continue

### Actual Result
ZIP field accepts alphabetic characters.

### Expected Result
ZIP field should allow only numeric values.

### Severity
Medium

### Status
Open

---

# BUG_04

## Title
First Name field accepts single character input

### Steps to Reproduce
1. Open checkout page
2. Enter single character in First Name field
3. Continue checkout

### Actual Result
Checkout proceeds successfully with single character input.

### Expected Result
Minimum character validation should be implemented.

### Severity
Low

### Status
Open

---

# BUG_05

## Title
ZIP/Postal Code field accepts excessive length input

### Steps to Reproduce
1. Open checkout page
2. Enter ZIP code longer than expected length
3. Continue checkout

### Actual Result
System accepts excessively long ZIP code.

### Expected Result
ZIP field should restrict maximum length.

### Severity
Medium

### Status
Open

---

# BUG_06

## Title
Last Name field accepts numeric values during checkout

### Steps to Reproduce
1. Login to application
2. Add item to cart
3. Proceed to checkout
4. Enter numeric values in Last Name field
5. Click Continue

### Actual Result
Checkout accepts numeric values in Last Name field.

### Expected Result
Last Name field should allow only alphabetic characters.

### Severity
Medium

### Status
Open

---

# BUG_07

## Title
Last Name field accepts single character input

### Steps to Reproduce
1. Open checkout page
2. Enter single character in Last Name field
3. Continue checkout

### Actual Result
Checkout proceeds successfully with single character input.

### Expected Result
Minimum character validation should be implemented for Last Name field.

### Severity
Low

### Status
Open

---

# BUG_08

## Title
Cart items persist across different user accounts after logout

### Steps to Reproduce
1. Login using first user account
2. Add product to cart
3. Logout from application
4. Login using different user account
5. Open cart page

### Actual Result
Previously added cart items are still visible for different user account.

### Expected Result
Each user account should maintain separate cart session and data.

### Severity
High

### Status
Open

### Notes
This issue may cause session/data leakage between users.

---

# BUG_09

## Title
Checkout form validation is weak for user input fields

### Steps to Reproduce
1. Open checkout form
2. Enter invalid formats in input fields
3. Continue checkout

### Actual Result
Application accepts invalid data formats.

### Expected Result
Application should validate user inputs before processing.

### Severity
Medium

### Status
Open
