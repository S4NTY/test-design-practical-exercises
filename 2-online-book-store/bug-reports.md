# Bug Reports

**Project:** online-book-store  
**Tester:** Alexandr Gusev  
**Total Bugs:** 2  

---

## BUG-001

| Field           | Detail                                             |
|-----------------|----------------------------------------------------|
| **Title**       | Negative value is accepted in New book price field |
| **Severity**    | High                                               |
| **Priority**    | High                                               |
| **Reported by** | Alexandr Gusev                                     |
| **Date**        | September 2026                                     |


**Environment**  
- Browser: Chrome 153  
- OS: Windows 10  
- URL: https://exercises.test-design.org/online-book-store  

**Steps to Reproduce**  
1. Go to page `online-book-store`  
2. Enter New book price = -1  
3. Enter Second hand book price = 0  
4. Select VIP = Yes  
5. Press button `Next test`

**Expected Result**  
Validation Error (negative price is not allowed)

**Actual Result**  
-0.9

---

## BUG-002

| Field           | Detail                                                     |
|-----------------|------------------------------------------------------------|
| **Title**       | Negative value is accepted in Second hand book price field |
| **Severity**    | High                                                       |
| **Priority**    | High                                                       |
| **Reported by** | Alexandr Gusev                                             |
| **Date**        | September 2026                                             |

**Environment**  
- Browser: Chrome 153  
- OS: Windows 10  
- URL: https://exercises.test-design.org/online-book-store  

**Steps to Reproduce**  
1. Go to page `online-book-store`  
2. Enter New book price = 0  
3. Enter Second hand book price = -1  
4. Select VIP = No  
5. Press button `Next test` (or Calculate)  

**Expected Result**  
Validation Error (negative price is not allowed)

**Actual Result**  
-1