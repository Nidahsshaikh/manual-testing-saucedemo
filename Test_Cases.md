# Test Cases – SauceDemo

---

# LOGIN MODULE

| TC ID | Test Scenario | Precondition | Steps | Expected Result | Actual Result | Test Type | Status |
|------|----------------|--------------|-------|----------------|--------------|----------|--------|
| TC_01 | Valid Login | User on login page | Enter standard_user / secret_sauce and click Login | User should navigate to Products page | User successfully navigated to Products page | Functional | Pass |
| TC_02 | Invalid Username | Login page open | Enter invalid username and valid password | Error message should display | Error message displayed correctly | Negative | Pass |
| TC_03 | Invalid Password | Login page open | Enter valid username and invalid password | Error message should display | Error message displayed correctly | Negative | Pass |
| TC_04 | Empty Fields | Login page open | Click Login without entering data | Validation error should display | Validation error displayed | Negative | Pass |
| TC_05 | Locked User Login | Login page open | Enter locked_out_user credentials | User should be blocked | User blocked with error message | Negative | Pass |
| TC_06 | Login Page UI Check | Login page open | Verify buttons, fields, labels | All UI elements should display correctly | Error message container slightly clipped | UI | Fail |

---

# PRODUCTS MODULE

| TC ID | Test Scenario | Precondition | Steps | Expected Result | Actual Result | Test Type | Status |
|------|----------------|--------------|-------|----------------|--------------|----------|--------|
| TC_07 | Product Display | User logged in | Login successfully | Product list should display | Product list displayed correctly | Functional | Pass |
| TC_08 | Add Product to Cart | Product page open | Click Add to Cart | Product should be added to cart | Product added successfully | Functional | Pass |
| TC_09 | Remove Product from Cart | Product already added | Click Remove button | Product should be removed | Product removed successfully | Functional | Pass |
| TC_10 | Cart Badge Update | Product added | Add item to cart | Cart count should update | Cart count updated correctly | Functional | Pass |
| TC_11 | Product Sorting | User on product page | Use sorting dropdown | Products should reorder correctly | Products reordered correctly | Functional | Pass |

---

# CART MODULE

| TC ID | Test Scenario | Precondition | Steps | Expected Result | Actual Result | Test Type | Status |
|------|----------------|--------------|-------|----------------|--------------|----------|--------|
| TC_12 | Open Cart | User logged in | Click cart icon | Cart page should open | Cart page opened successfully | Functional | Pass |
| TC_13 | Remove Item from Cart | Item present in cart | Click Remove | Item should disappear | Item removed successfully | Functional | Pass |
| TC_14 | Continue Shopping | Cart page open | Click Continue Shopping | User should return to products page | User redirected successfully | Functional | Pass |

---

# CHECKOUT MODULE

| TC ID | Test Scenario | Precondition | Steps | Expected Result | Actual Result | Test Type | Status |
|------|----------------|--------------|-------|----------------|--------------|----------|--------|
| TC_15 | Checkout Navigation | Cart page open | Click Checkout | Checkout page should open | Checkout page opened successfully | Functional | Pass |
| TC_16 | Empty Checkout Form | Checkout page open | Click Continue without entering data | Validation error should display | Validation error displayed | Negative | Pass |
| TC_17 | Valid Checkout Details | Checkout page open | Enter valid details and continue | User should move to overview page | User moved successfully | Functional | Pass |
| TC_18 | Complete Order | Overview page open | Click Finish | Order confirmation should display | Order completed successfully | Functional | Pass |

---

# VALIDATION & SESSION TESTING

| TC ID | Test Scenario | Precondition | Steps | Expected Result | Actual Result | Test Type | Status |
|------|----------------|--------------|-------|----------------|--------------|----------|--------|
| TC_19 | Numeric Input in First Name | Checkout page open | Enter numeric values in First Name field | System should reject numeric input | Numeric values accepted | Boundary | Fail |
| TC_20 | Alphabetic Input in ZIP Code | Checkout page open | Enter letters in ZIP field | System should reject alphabetic input | Alphabetic values accepted | Boundary | Fail |
| TC_21 | Long ZIP Code Input | Checkout page open | Enter ZIP code longer than expected length | System should restrict input length | Long ZIP values accepted | Boundary | Fail |
| TC_22 | Numeric Input in Last Name | Checkout page open | Enter numeric values in Last Name field | System should reject numeric input | Numeric values accepted | Boundary | Fail |
| TC_23 | Single Character in Last Name | Checkout page open | Enter single character in Last Name field | Minimum character validation should apply | Single character accepted | Boundary | Fail |
| TC_24 | Cart Persistence Across Users | First user has item in cart | Login with User A → Add item → Logout → Login with User B | Cart should be empty for different user | Previous user cart item still visible | Session | Fail |
