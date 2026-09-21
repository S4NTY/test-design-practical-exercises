# Execution Report

**Project:** online-book-store    
**Tester:** Alexandr Gusev  
**Execution Period:** September 2026  
**Build Version:** 1.0

---

## Summary

| Metric           | Count |
|------------------|-------|
| Total test cases | 13    |
| Executed         | 13    |
| Pass             | 11    |
| Fail             | 2     |
| Blocked          | 0     |
| Pass rate        | 85%   |

---

## Execution Report

| Case       | New book price | Second hand book price | VIP | Expected total price | Status |
|------------|----------------|------------------------|-----|----------------------|--------|
| TC-OBS-001 | 49.99          | 0                      | Yes | 44.99                | ✅      |
| TC-OBS-002 | 49.99          | 0                      | No  | 49.99                | ✅      |
| TC-OBS-003 | 50             | 0                      | Yes | 42.5                 | ✅      |
| TC-OBS-004 | 50.01          | 0                      | No  | 45.01                | ✅      |
| TC-OBS-005 | 30.01          | 60                     | Yes | 87.01                | ✅      |
| TC-OBS-006 | 30             | 60.01                  | No  | 90.01                | ✅      |
| TC-OBS-007 | 30.01          | 60.01                  | Yes | 84.02                | ✅      |
| TC-OBS-008 | 50             | 60.01                  | No  | 102.01               | ✅      |
| TC-OBS-009 | 50             | 60.01                  | Yes | 99.51                | ✅      |
| TC-OBS-010 | abc            | 0                      | Yes | NaN                  | ✅      |
| TC-OBS-011 | 0              | abc                    | No  | NaN                  | ✅      |
| TC-OBS-012 | -1             | 0                      | Yes | Validation Error     | ❌      |
| TC-OBS-013 | 0              | -1                     | No  | Validation Error     | ❌      |
---

## Result
![report.png](report.png)