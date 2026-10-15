# Execution Report

**Project:** extra-holiday  
**Tester:** Alexandr Gusev  
**Execution Period:** October 2026  
**Build Version:** 1.0

---

## Summary

| Metric           | Count |
|------------------|-------|
| Total test cases | 17    |
| Executed         | 17    |
| Pass             | 17    |
| Fail             | 0     |
| Blocked          | 0     |
| Pass rate        | 100%  |

---

## Execution Report

| Case    | Steps                                                                                       | Price to pay | Expected result                 | Status |
|---------|---------------------------------------------------------------------------------------------|--------------|---------------------------------|--------|
| Case 1  | 1. Price 999<br>2. Buy it                                                                   | 999          | Discount 0%<br>Total spend 999  | ✅      |
| Case 2  | 1. Price 1000<br>2. Buy it                                                                  | 1000         | Discount 5%<br>Total spend 1000 | ✅      |
| Case 3  | 1. Price 1001<br>2. Buy it                                                                  | 1001         | Discount 5%<br>Total spend 1001 | ✅      |
| Case 4  | 1. Price 1000<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 0    | ✅      |
| Case 5  | 1. Price 1000<br>2. Buy it<br>3. Price 1000<br>4. Buy it<br>5. Use discount                 | 950          | Discount 5%<br>Total spend 1000 | ✅      |
| Case 6  | 1. Price 1000<br>2. Buy it<br>3. Price 1000<br>4. Buy it<br>5. Use discount<br>6. Next year | 0            | Discount 0%<br>Total spend 0    | ✅      |
| Case 7  | 1. Price 1000<br>2. Buy it<br>3. Price 100<br>4. Buy it                                     | 100          | Discount 5%<br>Total spend 1200 | ✅      |
| Case 8  | 1. Price 1999<br>2. Buy it                                                                  | 1999         | Discount 5%<br>Total spend 1999 | ✅      |
| Case 9  | 1. Price 2000<br>2. Buy it                                                                  | 2000         | Discount 8%<br>Total spend 2000 | ✅      |
| Case 10 | 1. Price 2001<br>2. Buy it                                                                  | 2001         | Discount 8%<br>Total spend 2001 | ✅      |
| Case 11 | 1. Price 1999<br>2. Buy it<br>3. Price 500<br>4. Buy it<br>5. Use discount                  | 475          | Discount 8%<br>Total spend 1999 | ✅      |
| Case 12 | 1. Price 2000<br>2. Buy it<br>3. Price 1000<br>4. Buy it<br>5. Use discount                 | 920          | Discount 8%<br>Total spend 2920 | ✅      |
| Case 13 | 1. Price 2500<br>2. Buy it<br>3. Price 100<br>4. Buy it<br>5. Use discount                  | 92           | Discount 8%<br>Total spend 2592 | ✅      |
| Case 14 | 1. Price 2999<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 0    | ✅      |
| Case 15 | 1. Price 3000<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 750  | ✅      |
| Case 16 | 1. Price 3500<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 875  | ✅      |
| Case 17 | 1. Price 3000<br>2. Buy it<br>3. Next year<br>4. Price 250<br>5. Buy it                     | 250          | Discount 5%<br>Total spend 1000 | ✅      |

---

## Result
![report.png](report.png)