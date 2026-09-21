# Test Cases — Price Calculation

**Module:** price-calculation  
**Tester:** Alexandr Gusev  
**Total Cases:** 11  
**Version:** 1.0  

---

## Summary Tables
### Summary table of positive tests

| Case      | Price | Weight | Pay with credit card | Expected total price |
|-----------|-------|--------|----------------------|----------------------|
| TC-PC-001 | 99    | 4.9    | Yes                  | 96                   |
| TC-PC-002 | 100   | 5      | No                   | 105                  |
| TC-PC-003 | 101   | 4.9    | Yes                  | 98                   |
| TC-PC-004 | 199   | 5      | No                   | 199                  |
| TC-PC-005 | 200   | 4.9    | Yes                  | 170                  |
| TC-PC-006 | 200   | 5      | Yes                  | 174.6                |
| TC-PC-007 | 201   | 6      | No                   | 180.9                |

---

### Summary table of negative tests

| Case      | Price | Weight | Pay with credit card | Expected result  |
|-----------|-------|--------|----------------------|------------------|
| TC-PC-008 | abc   | 5      | No                   | NaN              |
| TC-PC-009 | 100   | abc    | Yes                  | NaN              |
| TC-PC-010 | -1    | 4.9    | No                   | Validation Error |
| TC-PC-011 | 200   | -1     | Yes                  | Validation Error |

---

## Detailed Test Cases

### TC-PC-001
| Field             | Detail                                                                               |
|-------------------|--------------------------------------------------------------------------------------|
| **Title**         | Price < 100, weight < 5, payment by credit card                                      |
| **Priority**      | High                                                                                 |
| **Preconditions** | Web page is open                                                                     |
| **Steps**         | 1. Enter Price = 99<br>2. Enter Weight = 4.9<br>3. Select Pay with credit card = Yes |
| **Expected**      | Total price = 96                                                                     |

---

### TC-PC-002
| Field             | Detail                                                                             |
|-------------------|------------------------------------------------------------------------------------|
| **Title**         | Price = 100, weight = 5, no credit card                                            |
| **Priority**      | High                                                                               |
| **Preconditions** | Web page is open                                                                   |
| **Steps**         | 1. Enter Price = 100<br>2. Enter Weight = 5<br>3. Select Pay with credit card = No |
| **Expected**      | Total price = 105                                                                  |

---

### TC-PC-003
| Field             | Detail                                                                                |
|-------------------|---------------------------------------------------------------------------------------|
| **Title**         | Price > 100, weight < 5, payment by credit card                                       |
| **Priority**      | High                                                                                  |
| **Preconditions** | Web page is open                                                                      |
| **Steps**         | 1. Enter Price = 101<br>2. Enter Weight = 4.9<br>3. Select Pay with credit card = Yes |
| **Expected**      | Total price = 98                                                                      |


---

### TC-PC-004
| Field             | Detail                                                                             |
|-------------------|------------------------------------------------------------------------------------|
| **Title**         | Price just below 200, weight = 5, no credit card                                   |
| **Priority**      | High                                                                               |
| **Preconditions** | Web page is open                                                                   |
| **Steps**         | 1. Enter Price = 199<br>2. Enter Weight = 5<br>3. Select Pay with credit card = No |
| **Expected**      | Total price = 199                                                                  |

---

### TC-PC-005
| Field             | Detail                                                                                |
|-------------------|---------------------------------------------------------------------------------------|
| **Title**         | Price = 200, weight = 4.9, payment by credit card (Rule R5)                           |
| **Priority**      | Critical                                                                              |
| **Preconditions** | Web page is open                                                                      |
| **Steps**         | 1. Enter Price = 200<br>2. Enter Weight = 4.9<br>3. Select Pay with credit card = Yes |
| **Expected**      | Total price = 170                                                                     |

---

### TC-PC-006
| Field             | Detail                                                                              |
|-------------------|-------------------------------------------------------------------------------------|
| **Title**         | Price = 200, weight = 5, payment by credit card (Rule R5)                           |
| **Priority**      | Critical                                                                            |
| **Preconditions** | Web page is open                                                                    |
| **Steps**         | 1. Enter Price = 200<br>2. Enter Weight = 5<br>3. Select Pay with credit card = Yes |
| **Expected**      | Total price = 174.6                                                                   |

---

### TC-PC-007
| Field             | Detail                                                                             |
|-------------------|------------------------------------------------------------------------------------|
| **Title**         | Price > 200, weight = 6, no credit card                                            |
| **Priority**      | High                                                                               |
| **Preconditions** | Web page is open                                                                   |
| **Steps**         | 1. Enter Price = 201<br>2. Enter Weight = 6<br>3. Select Pay with credit card = No |
| **Expected**      | Total price = 180.9                                                                |

---

### TC-PC-008
| Field             | Detail                                                                             |
|-------------------|------------------------------------------------------------------------------------|
| **Title**         | Invalid price (letters instead of number)                                          |
| **Priority**      | High                                                                               |
| **Preconditions** | Web page is open                                                                   |
| **Steps**         | 1. Enter Price = abc<br>2. Enter Weight = 5<br>3. Select Pay with credit card = No |
| **Expected**      | Validation Error                                                                   |

---

### TC-PC-009
| Field             | Detail                                                                                |
|-------------------|---------------------------------------------------------------------------------------|
| **Title**         | Invalid weight (letters instead of number)                                            |
| **Priority**      | High                                                                                  |
| **Preconditions** | Web page is open                                                                      |
| **Steps**         | 1. Enter Price = 100<br>2. Enter Weight = abc<br>3. Select Pay with credit card = Yes |
| **Expected**      | Validation Error                                                                      |

---

### TC-PC-010
| Field             | Detail                                                                              |
|-------------------|-------------------------------------------------------------------------------------|
| **Title**         | Negative price value                                                                |
| **Priority**      | High                                                                                |
| **Preconditions** | Web page is open                                                                    |
| **Steps**         | 1. Enter Price = -1<br>2. Enter Weight = 4.9<br>3. Select Pay with credit card = No |
| **Expected**      | Validation Error                                                                    |

---

### TC-PC-011
| Field             | Detail                                                                               |
|-------------------|--------------------------------------------------------------------------------------|
| **Title**         | Negative weight value                                                                |
| **Priority**      | High                                                                                 |
| **Preconditions** | Web page is open                                                                     |
| **Steps**         | 1. Enter Price = 200<br>2. Enter Weight = -1<br>3. Select Pay with credit card = Yes |
| **Expected**      | Validation Error                                                                     |