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

| Case  | Preconditions                                  | Steps                                                      | Expected result                             | Total price | Status |
|-------|------------------------------------------------|------------------------------------------------------------|---------------------------------------------|-------------|--------|
| R3-1  |                                                | Add 1 fresca<br>Remove fresca                              | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R3-2  |                                                | Add 1 polo<br>Remove polo                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R3-3  |                                                | Add 1 beer<br>Remove beer                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R3-4  |                                                | Add 1 coke<br>Remove coke                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R4-1  |                                                | Add 3 fresca<br>Choose free beer                           | fresca: 3<br>polo: 0<br>beer: 1<br>coke: 0  | 54          | ✅      |
| R4-2  |                                                | Add 3 polo<br>Choose free coke                             | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 1  | 45          | ✅      |
| R4-3  |                                                | Add 15 coke<br>Nothing to choose                           | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 15 | 45          | ✅      |
| R4-4  |                                                | Add 12 beer<br>Nothing to choose                           | fresca: 0<br>polo: 0<br>beer: 15<br>coke: 0 | 48          | ✅      |
| R4-5  | Add 1 fresca                                   | Add 3 polo<br>Choose free coke<br>Remove fresca            | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 1  | 45          | ✅      |
| R4-6  | Add 3 fresca<br>Add 1 polo<br>Choose free beer | Remove polo                                                | fresca: 3<br>polo: 0<br>beer: 1<br>coke: 0  | 54          | ✅      |
| R4-7  |                                                | Add 1 beer<br>Add 3 polo<br>Choose free beer               | fresca: 0<br>polo: 3<br>beer: 2<br>coke: 0  | 49          | ✅      |
| R4-8  |                                                | Add 1 coke<br>Add 3 fresca<br>Choose free coke             | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 2  | 57          | ✅      |
| R4-9  | Add 3 polo<br>Choose free coke                 | Add 1 polo                                                 | fresca: 4<br>polo: 0<br>beer: 0<br>coke: 1  | 60          | ✅      |
| R4-10 | Add 3 fresca<br>Choose free coke               | Add 1 coke<br>Remove fresca                                | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 1  | 3           | ✅      |
| R4-11 | Add 3 polo<br>Choose free beer                 | Add 1 beer<br>Remove polo                                  | fresca: 0<br>polo: 0<br>beer: 1<br>coke: 0  | 4           | ✅      |
| R6-1  | Add 2 fresca<br>Add 1 polo<br>Choose nothing   | Remove polo<br>Add polo<br>Choose free coke                | fresca: 2<br>polo: 1<br>beer: 0<br>coke: 1  | 51          | ✅      |
| R6-2  | Add 3 fresca<br>Choose free coke               | Remove coke<br>Remove fresca<br>Add 1 coke<br>Add 3 fresca | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 1  | 54          | ✅      |
| R6-3  | Add 3 fresca<br>Choose free coke               | Remove coke<br>Remove fresca<br>Add 3 fresca<br>Add 1 coke | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 1  | 54          | ✅      |
| R6-4  | Add 3 polo<br>Choose free beer                 | Remove beer<br>Remove polo<br>Add 1 beer<br>Add 3 polo     | fresca: 0<br>polo: 3<br>beer: 1<br>coke: 0  | 45          | ✅      |
| R6-5  | Add 3 polo<br>Choose free beer                 | Remove beer<br>Remove polo<br>Add 3 polo<br>Add 1 beer     | fresca: 0<br>polo: 3<br>beer: 1<br>coke: 0  | 45          | ✅      |
| R8-1  | Add 1 coke                                     | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R8-2  | Add 3 polo<br>Choose nothing                   | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R8-3  | Add 3 polo<br>Choose free coke                 | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R8-4  | Add 3 fresca<br>Choose free beer               | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           | ✅      |
| R8-5  | Add 3 fresca<br>Choose free beer               | Clear all<br>Add 3 polo                                    | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 0  | 45          | ✅      |

---

## Result
![report.png](report.png)