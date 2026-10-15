# Execution Report

**Project:** car-rental   
**Tester:** Alexandr Gusev  
**Execution Period:** October 2026  
**Build Version:** 1.0

---

## Summary

| Metric           | Count |
|------------------|-------|
| Total test cases | 14    |
| Executed         | 14    |
| Pass             | 14    |
| Fail             | 0     |
| Blocked          | 0     |
| Pass rate        | 100%  |

---

## Execution Report

| Case      | Preconditions   | Steps                          | Expected result     | Total rental price | Status |
|-----------|-----------------|--------------------------------|---------------------|--------------------|--------|
| TC-CR-001 | 0 cars, 0 bikes | Add 2 cars                     | 2 cars, 0 bikes     | 600                | ✅      |
| TC-CR-002 | 0 cars, 0 bikes | Add 2 bikes                    | 0 cars, 2 bikes     | 200                | ✅      |
| TC-CR-003 | 0 cars, 2 bikes | Remove 1 bike                  | 0 cars, 1 bike      | 100                | ✅      |
| TC-CR-004 | 2 cars, 0 bikes | Remove 1 car                   | 1 car, 0 bikes      | 300                | ✅      |
| TC-CR-005 | 0 cars, 0 bikes | Add 3 cars                     | 3 cars, 1 free bike | 900                | ✅      |
| TC-CR-006 | 0 cars, 1 bike  | Add 3 cars                     | 3 cars, 1 free bike | 900                | ✅      |
| TC-CR-007 | 0 cars, 2 bikes | Add 3 cars                     | 3 cars, 2 bikes     | 1000               | ✅      |
| TC-CR-008 | 3 cars, 0 bikes | Remove 2 cars                  | 1 car, 0 bikes      | 300                | ✅      |
| TC-CR-009 | 3 cars, 1 bike  | Remove 1 car                   | 2 cars, 1 bike      | 700                | ✅      |
| TC-CR-010 | 3 cars, 2 bikes | Remove 1 bike                  | 3 cars, 1 bike      | 900                | ✅      |
| TC-CR-011 | 4 cars, 0 bikes | Remove 1 car                   | 3 cars, 1 free bike | 900                | ✅      |
| TC-CR-012 | 3 cars, 0 bikes | Remove 1 free bike, Add car    | 4 cars, 1 free bike | 1200               | ✅      |
| TC-CR-013 | 3 cars, 0 bikes | Remove 1 free bike, Remove car | 2 cars, 0 bikes     | 600                | ✅      |
| TC-CR-014 | 3 cars, 0 bikes | Remove 1 free bike, Add bike   | 3 cars, 1 bike      | 900                | ✅      |

## Result
![report.png](report.png)