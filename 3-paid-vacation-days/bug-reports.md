# Bug Reports

**Project:** paid-vacation-days  
**Tester:** Alexandr Gusev  
**Total Bugs:** 2 

---

## BUG-001

| Field           | Detail                                  |
|-----------------|-----------------------------------------|
| **Title**       | Negative value is accepted in Age field |
| **Severity**    | High                                    |
| **Priority**    | High                                    |
| **Reported by** | Alexandr Gusev                          |
| **Date**        | September 2026                          |

**Environment**  
- Browser: Chrome 153  
- OS: Windows 10  
- URL: https://exercises.test-design.org/paid-vacation-days 

**Steps to Reproduce**  
1. Go to page `paid-vacation-days`  
2. Enter Age = -1  
3. Enter Years of service = 10  
4. Press button `Next test`  

**Expected Result**  
Validation Error (negative Age is not allowed)

**Actual Result**  
27

---

## BUG-002

| Field           | Detail                                               |
|-----------------|------------------------------------------------------|
| **Title**       | Negative value is accepted in Years of service field |
| **Severity**    | High                                                 |
| **Priority**    | High                                                 |
| **Reported by** | Alexandr Gusev                                       |
| **Date**        | September 2026                                       |

**Environment**  
- Browser: Chrome 153  
- OS: Windows 10  
- URL: https://exercises.test-design.org/paid-vacation-days  

**Steps to Reproduce**  
1. Go to page `paid-vacation-days`  
2. Enter Age = 30  
3. Enter Years of service = -1  
4. Press button `Next test` 

**Expected Result**  
Validation Error (negative Years of service is not allowed)

**Actual Result**  
22