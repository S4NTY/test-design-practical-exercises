# Bug Reports

**Project:** price-calculation  
**Tester:** Alexandr Gusev  
**Total Bugs:** 3  

---

## BUG-001

| Field           | Detail                                               |
|-----------------|------------------------------------------------------|
| **Title**       | Input of characters into the weight field is allowed |
| **Severity**    | High                                                 |
| **Priority**    | Normal                                               |
| **Reported by** | Alexandr Gusev                                       |
| **Date**        | September 2026                                       |

**Environment**
- Browser: Chrome 153
- OS: Windows 10
- URL: https://exercises.test-design.org/price-calculation

**Steps to Reproduce**
1. Go to page `price-calculation`
2. Enter Price = 100
3. Enter Weight = abc
4. Select Pay with credit card = Yes
5. Press button `Next test`

**Expected Result**  
Total price: NaN

**Actual Result**  
Total price: 97

---

## BUG-002

| Field           | Detail                                                  |
|-----------------|---------------------------------------------------------|
| **Title**       | Entering negative numbers in the price field is allowed |
| **Severity**    | Critical                                                |
| **Priority**    | Critical                                                |
| **Reported by** | Alexandr Gusev                                          |
| **Date**        | September 2026                                          |

**Environment**
- Browser: Chrome 153
- OS: Windows 10
- URL: https://exercises.test-design.org/price-calculation

**Steps to Reproduce**
1. Go to page `price-calculation`
2. Enter Price = -1
3. Enter Weight = 4.9
4. Select Pay with credit card = No
5. Press button `Next test`

**Expected Result**  
Total price: Validation Error

**Actual Result**  
Total price: -1

---

## BUG-003

| Field           | Detail                                                  |
|-----------------|---------------------------------------------------------|
| **Title**       | Entering negative numbers in the price field is allowed |
| **Severity**    | Critical                                                |
| **Priority**    | Critical                                                |
| **Reported by** | Alexandr Gusev                                          |
| **Date**        | September 2026                                          |

**Environment**
- Browser: Chrome 153
- OS: Windows 10
- URL: https://exercises.test-design.org/price-calculation

**Steps to Reproduce**
1. Go to page `price-calculation`
2. Enter Price = 200
3. Enter Weight = -1
4. Select Pay with credit card = Yes
5. Press button `Next test`

**Expected Result**  
Total price: Validation Error

**Actual Result**  
Total price: 170