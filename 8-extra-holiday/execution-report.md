# Execution Report

**Project:** extra-holiday  
**Tester:** Alexandr Gusev  
**Execution Period:** October 2026  
**Build Version:** 1.0

---

## Summary

| Metric           | Count |
|------------------|-------|
| Total test cases | 10    |
| Executed         | 10    |
| Pass             | 10    |
| Fail             | 0     |
| Blocked          | 0     |
| Pass rate        | 100%  |

---

## Execution Report

| Case    | Steps                                                                                                      | Expected result                              | Status |
|---------|------------------------------------------------------------------------------------------------------------|----------------------------------------------|--------|
| Case 1  | Add 3 extra day<br>Add 1 lateness                                                                          | Extra days: 0<br>Free days: 0                | ✅      |
| Case 2  | Add 4 extra day<br>Add 1 lateness                                                                          | Extra days: 1<br>Free days: 0                | ✅      |
| Case 3  | Get 1 free day                                                                                             | Extra days: 0<br>Free days: 0                | ✅      |
| Case 4  | Add 9 extra day<br>Get 3 free days<br>Add 2 lateness                                                       | Extra days: -2<br>Free days: 0               | ✅      |
| Case 5  | Add 9 extra day<br>Get 1 free day<br>Add 1 lateness<br>Add 1 extra day<br>Get 2 free day<br>Add 1 lateness | Extra days: 1<br>Free days: 0                | ✅      |
| Case 6  | Add 1 lateness<br>Add 1 extra day<br>Add 1 lateness                                                        | Extra days: 0<br>Free days: -1               | ✅      |
| Case 7  | Add 5 lateness                                                                                             | Extra days: -1<br>Free days: -3<br>Game Over | ✅      |
| Case 8  | Add 5 lateness<br>Add 1 extra day                                                                          | Extra days: -1<br>Free days: -3<br>Game Over | ✅      |
| Case 9  | Add 5 lateness<br>Get 1 free day                                                                           | Extra days: -1<br>Free days: -3<br>Game Over | ✅      |
| Case 10 | Add 6 lateness                                                                                             | Extra days: -1<br>Free days: -3<br>Game Over | ✅      |

---

## Result
![report.png](report.png)