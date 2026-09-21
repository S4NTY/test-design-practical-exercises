# Bug Reports

**Project:** paid-vacation-days  
**Tester:** Alexandr Gusev  
**Total Bugs:** 3  

---

## BUG-001


| Field           | Detail                                                                   |
|-----------------|--------------------------------------------------------------------------|
| **Title**       | System reports incomplete boundary coverage and suggests redundant tests |
| **Severity**    | Critical                                                                 |
| **Priority**    | Critical                                                                 |
| **Reported by** | Alexandr Gusev                                                           |
| **Date**        | September 2026                                                           |


**Environment**  
- Browser: Chrome 153  
- OS: Windows 10  
- URL: https://exercises.test-design.org/paid-vacation-days

**Steps to Reproduce**  
1. Go to page `paid-vacation-days`  
2. Execute all test cases covering all boundary values according to the specified rules (Age and Years of service boundaries: 17/18, 44/45, 59/60 and 10/14/15, 29/30)  
3. Submit the set of test cases for evaluation  
4. Observe the system feedback  

**Expected Result**  
System confirms that all boundary values are fully covered. No additional test cases are suggested.

**Actual Result**  
System reports that some variants remain uncovered and proposes excess/redundant test cases that are not required by the boundary conditions.

## BUG-002

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

## BUG-003

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