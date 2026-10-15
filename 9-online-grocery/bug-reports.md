# Bug Reports

**Project:** online-grocery
**Tester:** Alexandr Gusev  
**Total Bugs:** 1  

---

## BUG-001

| Field           | Detail                                              |
|-----------------|-----------------------------------------------------|
| **Title**       | Input of characters into the price field is allowed |
| **Severity**    | High                                                |
| **Priority**    | High                                                |
| **Reported by** | Alexandr Gusev                                      |
| **Date**        | October 2026                                        |


**Environment**  
- Browser: Chrome 153  
- OS: Windows 10  
- URL: https://exercises.test-design.org/grocery/  

**Steps to Reproduce**  
1. Go to page `online-grocery`  
2. Enter Price = "abc"
3. Press button `I buy it`

**Expected Result**  
Price to pay: NaN  
Total spending: 0     
Price reduction %: 0

**Actual Result**  
Price to pay: NaN   
Total spending: NaN     
Price reduction %: 0  

Total spending added NaN.
