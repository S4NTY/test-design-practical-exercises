# Execution Report

**Project:** online-pizza-ordering  
**Tester:** Alexandr Gusev  
**Execution Period:** October 2026  
**Build Version:** 1.0

---

## Summary

| Metric           | Count |
|------------------|-------|
| Total test cases | 25    |
| Executed         | 25    |
| Pass             | 25    |
| Fail             | 0     |
| Blocked          | 0     |
| Pass rate        | 100%  |

---

## Execution Report

| Case      | Preconditions                                  | Steps                                                      | Expected result                             | Total price | Status |
|-----------|------------------------------------------------|------------------------------------------------------------|---------------------------------------------|-------------|--------|
| TC-R3-001 |                                                | Add 1 fresca<br>Remove fresca                              | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R3-002 |                                                | Add 1 polo<br>Remove polo                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R3-003 |                                                | Add 1 beer<br>Remove beer                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R3-004 |                                                | Add 1 coke<br>Remove coke                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R4-001 |                                                | Add 3 fresca<br>Choose free beer                           | fresca: 3<br>polo: 0<br>beer: 1<br>coke: 0  | 54          | ✅      |
| TC-R4-002 |                                                | Add 3 polo<br>Choose free coke                             | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 1  | 45          | ✅      |
| TC-R4-003 |                                                | Add 15 coke<br>Nothing to choose                           | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 15 | 45          | ✅      |
| TC-R4-004 |                                                | Add 12 beer<br>Nothing to choose                           | fresca: 0<br>polo: 0<br>beer: 15<br>coke: 0 | 48          | ✅      |
| TC-R4-005 | Add 1 fresca                                   | Add 3 polo<br>Choose free coke<br>Remove fresca            | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 1  | 45          | ✅      |
| TC-R4-006 | Add 3 fresca<br>Add 1 polo<br>Choose free beer | Remove polo                                                | fresca: 3<br>polo: 0<br>beer: 1<br>coke: 0  | 54          | ✅      |
| TC-R4-007 |                                                | Add 1 beer<br>Add 3 polo<br>Choose free beer               | fresca: 0<br>polo: 3<br>beer: 2<br>coke: 0  | 49          | ✅      |
| TC-R4-008 |                                                | Add 1 coke<br>Add 3 fresca<br>Choose free coke             | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 2  | 57          | ✅      |
| TC-R4-009 | Add 3 polo<br>Choose free coke                 | Add 1 polo                                                 | fresca: 4<br>polo: 0<br>beer: 0<br>coke: 1  | 60          | ✅      |
| TC-R4-010 | Add 3 fresca<br>Choose free coke               | Add 1 coke<br>Remove fresca                                | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 1  | 3           | ✅      |
| TC-R4-011 | Add 3 polo<br>Choose free beer                 | Add 1 beer<br>Remove polo                                  | fresca: 0<br>polo: 0<br>beer: 1<br>coke: 0  | 4           | ✅      |
| TC-R6-001 | Add 2 fresca<br>Add 1 polo<br>Choose nothing   | Remove polo<br>Add polo<br>Choose free coke                | fresca: 2<br>polo: 1<br>beer: 0<br>coke: 1  | 51          | ✅      |
| TC-R6-002 | Add 3 fresca<br>Choose free coke               | Remove coke<br>Remove fresca<br>Add 1 coke<br>Add 3 fresca | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 1  | 54          | ✅      |
| TC-R6-003 | Add 3 fresca<br>Choose free coke               | Remove coke<br>Remove fresca<br>Add 3 fresca<br>Add 1 coke | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 1  | 54          | ✅      |
| TC-R6-004 | Add 3 polo<br>Choose free beer                 | Remove beer<br>Remove polo<br>Add 1 beer<br>Add 3 polo     | fresca: 0<br>polo: 3<br>beer: 1<br>coke: 0  | 45          | ✅      |
| TC-R6-005 | Add 3 polo<br>Choose free beer                 | Remove beer<br>Remove polo<br>Add 3 polo<br>Add 1 beer     | fresca: 0<br>polo: 3<br>beer: 1<br>coke: 0  | 45          | ✅      |
| TC-R8-001 | Add 1 coke                                     | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R8-002 | Add 3 polo<br>Choose nothing                   | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R8-003 | Add 3 polo<br>Choose free coke                 | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R8-004 | Add 3 fresca<br>Choose free beer               | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| TC-R8-005 | Add 3 fresca<br>Choose free beer               | Clear all<br>Add 3 polo                                    | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 0  | 45          | ✅      |

---

## Result
![report.png](report.png)