# Test Cases — Online pizza ordering 

**Module:** online-pizza-ordering  
**Tester:** Alexandr Gusev  
**Total Cases:** 25  
**Version:** 1.0

---

## Summary Tables

| Case  | Preconditions                                  | Steps                                                      | Expected result                             | Total price |
|-------|------------------------------------------------|------------------------------------------------------------|---------------------------------------------|-------------|
| R3-1  |                                                | Add 1 fresca<br>Remove fresca                              | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R3-2  |                                                | Add 1 polo<br>Remove polo                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R3-3  |                                                | Add 1 beer<br>Remove beer                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R3-4  |                                                | Add 1 coke<br>Remove coke                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R4-1  |                                                | Add 3 fresca<br>Choose free beer                           | fresca: 3<br>polo: 0<br>beer: 1<br>coke: 0  | 54          |
| R4-2  |                                                | Add 3 polo<br>Choose free coke                             | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 1  | 45          |
| R4-3  |                                                | Add 15 coke<br>Nothing to choose                           | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 15 | 45          |
| R4-4  |                                                | Add 12 beer<br>Nothing to choose                           | fresca: 0<br>polo: 0<br>beer: 15<br>coke: 0 | 48          |
| R4-5  | Add 1 fresca                                   | Add 3 polo<br>Choose free coke<br>Remove fresca            | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 1  | 45          |
| R4-6  | Add 3 fresca<br>Add 1 polo<br>Choose free beer | Remove polo                                                | fresca: 3<br>polo: 0<br>beer: 1<br>coke: 0  | 54          |
| R4-7  |                                                | Add 1 beer<br>Add 3 polo<br>Choose free beer               | fresca: 0<br>polo: 3<br>beer: 2<br>coke: 0  | 49          |
| R4-8  |                                                | Add 1 coke<br>Add 3 fresca<br>Choose free coke             | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 2  | 57          |
| R4-9  | Add 3 polo<br>Choose free coke                 | Add 1 polo                                                 | fresca: 4<br>polo: 0<br>beer: 0<br>coke: 1  | 60          |
| R4-10 | Add 3 fresca<br>Choose free coke               | Add 1 coke<br>Remove fresca                                | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 1  | 3           |
| R4-11 | Add 3 polo<br>Choose free beer                 | Add 1 beer<br>Remove polo                                  | fresca: 0<br>polo: 0<br>beer: 1<br>coke: 0  | 4           |
| R6-1  | Add 2 fresca<br>Add 1 polo<br>Choose nothing   | Remove polo<br>Add polo<br>Choose free coke                | fresca: 2<br>polo: 1<br>beer: 0<br>coke: 1  | 51          |
| R6-2  | Add 3 fresca<br>Choose free coke               | Remove coke<br>Remove fresca<br>Add 1 coke<br>Add 3 fresca | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 1  | 54          |
| R6-3  | Add 3 fresca<br>Choose free coke               | Remove coke<br>Remove fresca<br>Add 3 fresca<br>Add 1 coke | fresca: 3<br>polo: 0<br>beer: 0<br>coke: 1  | 54          |
| R6-4  | Add 3 polo<br>Choose free beer                 | Remove beer<br>Remove polo<br>Add 1 beer<br>Add 3 polo     | fresca: 0<br>polo: 3<br>beer: 1<br>coke: 0  | 45          |
| R6-5  | Add 3 polo<br>Choose free beer                 | Remove beer<br>Remove polo<br>Add 3 polo<br>Add 1 beer     | fresca: 0<br>polo: 3<br>beer: 1<br>coke: 0  | 45          |
| R8-1  | Add 1 coke                                     | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R8-2  | Add 3 polo<br>Choose nothing                   | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R8-3  | Add 3 polo<br>Choose free coke                 | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R8-4  | Add 3 fresca<br>Choose free beer               | Clear all                                                  | fresca: 0<br>polo: 0<br>beer: 0<br>coke: 0  | 0           |
| R8-5  | Add 3 fresca<br>Choose free beer               | Clear all<br>Add 3 polo                                    | fresca: 0<br>polo: 3<br>beer: 0<br>coke: 0  | 45          |

---

## Detailed Test Cases

### TC-R3-001

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add and remove 1 fresca                     |
| **Priority**         | Medium                                      |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 1 fresca                             |
|                      | 2. Remove fresca                            |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R3-002

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add and remove 1 polo                       |
| **Priority**         | Medium                                      |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 1 polo                               |
|                      | 2. Remove polo                              |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R3-003

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add and remove 1 beer                       |
| **Priority**         | Medium                                      |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 1 beer                               |
|                      | 2. Remove beer                              |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R3-004

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add and remove 1 coke                       |
| **Priority**         | Medium                                      |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 1 coke                               |
|                      | 2. Remove coke                              |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R4-001

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add 3 fresca and choose free beer           |
| **Priority**         | High                                        |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 3 fresca                             |
|                      | 2. Choose free beer                         |
| **Expected result**  | fresca: 3  polo: 0  beer: 1  coke: 0        |
| **Total price**      | 54                                          |

---

### TC-R4-002

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add 3 polo and choose free coke             |
| **Priority**         | High                                        |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 3 polo                               |
|                      | 2. Choose free coke                         |
| **Expected result**  | fresca: 0  polo: 3  beer: 0  coke: 1        |
| **Total price**      | 45                                          |

---

### TC-R4-003

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add 15 coke with nothing to choose          |
| **Priority**         | Medium                                      |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 15 coke                              |
|                      | 2. Nothing to choose                        |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 15       |
| **Total price**      | 45                                          |

---

### TC-R4-004

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add 12 beer with nothing to choose          |
| **Priority**         | Medium                                      |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 12 beer                              |
|                      | 2. Nothing to choose                        |
| **Expected result**  | fresca: 0  polo: 0  beer: 15  coke: 0       |
| **Total price**      | 48                                          |

---

### TC-R4-005

| Field               | Detail                                         |
|---------------------|------------------------------------------------|
| **Title**           | Add 3 polo and choose free coke after 1 fresca |
| **Priority**        | High                                           |
| **Preconditions**   | Add 1 fresca                                   |
| **Steps**           | 1. Add 3 polo                                  |
|                     | 2. Choose free coke                            |
|                     | 3. Remove fresca                               |
| **Expected result** | fresca: 0  polo: 3  beer: 0  coke: 1           |
| **Total price**     | 45                                             |

---

### TC-R4-006

| Field               | Detail                                         |
|---------------------|------------------------------------------------|
| **Title**           | Remove polo after choosing free beer           |
| **Priority**        | High                                           |
| **Preconditions**   | Add 3 fresca<br>Add 1 polo<br>Choose free beer |
| **Steps**           | 1. Remove polo                                 |
| **Expected result** | fresca: 3  polo: 0  beer: 1  coke: 0           |
| **Total price**     | 54                                             |

---

### TC-R4-007

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add beer, then 3 polo and choose free beer  |
| **Priority**         | High                                        |
| **Preconditions**    | —                                           |
| **Steps**            | 1. Add 1 beer                               |
|                      | 2. Add 3 polo                               |
|                      | 3. Choose free beer                         |
| **Expected result**  | fresca: 0  polo: 3  beer: 2  coke: 0        |
| **Total price**      | 49                                          |

---

### TC-R4-008

| Field               | Detail                                       |
|---------------------|----------------------------------------------|
| **Title**           | Add coke, then 3 fresca and choose free coke |
| **Priority**        | High                                         |
| **Preconditions**   | —                                            |
| **Steps**           | 1. Add 1 coke                                |
|                     | 2. Add 3 fresca                              |
|                     | 3. Choose free coke                          |
| **Expected result** | fresca: 3  polo: 0  beer: 0  coke: 2         |
| **Total price**     | 57                                           |

---

### TC-R4-009

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Add 1 polo after choosing free coke         |
| **Priority**         | High                                        |
| **Preconditions**    | Add 3 polo<br>Choose free coke              |
| **Steps**            | 1. Add 1 polo                               |
| **Expected result**  | fresca: 4  polo: 0  beer: 0  coke: 1        |
| **Total price**      | 60                                          |

---

### TC-R4-010

| Field               | Detail                                              |
|---------------------|-----------------------------------------------------|
| **Title**           | Add coke and remove fresca after choosing free coke |
| **Priority**        | High                                                |
| **Preconditions**   | Add 3 fresca<br>Choose free coke                    |
| **Steps**           | 1. Add 1 coke                                       |
|                     | 2. Remove fresca                                    |
| **Expected result** | fresca: 0  polo: 0  beer: 0  coke: 1                |
| **Total price**     | 3                                                   |

---

### TC-R4-011

| Field               | Detail                                            |
|---------------------|---------------------------------------------------|
| **Title**           | Add beer and remove polo after choosing free beer |
| **Priority**        | High                                              |
| **Preconditions**   | Add 3 polo<br>Choose free beer                    |
| **Steps**           | 1. Add 1 beer                                     |
|                     | 2. Remove polo                                    |
| **Expected result** | fresca: 0  polo: 0  beer: 1  coke: 0              |
| **Total price**     | 4                                                 |

---

### TC-R6-001

| Field               | Detail                                        |
|---------------------|-----------------------------------------------|
| **Title**           | Remove and re-add polo, then choose free coke |
| **Priority**        | High                                          |
| **Preconditions**   | Add 2 fresca<br>Add 1 polo<br>Choose nothing  |
| **Steps**           | 1. Remove polo                                |
|                     | 2. Add polo                                   |
|                     | 3. Choose free coke                           |
| **Expected result** | fresca: 2  polo: 1  beer: 0  coke: 1          |
| **Total price**     | 51                                            |

---

### TC-R6-002

| Field               | Detail                                             |
|---------------------|----------------------------------------------------|
| **Title**           | Remove coke and fresca, then add coke and 3 fresca |
| **Priority**        | High                                               |
| **Preconditions**   | Add 3 fresca<br>Choose free coke                   |
| **Steps**           | 1. Remove coke                                     |
|                     | 2. Remove fresca                                   |
|                     | 3. Add 1 coke                                      |
|                     | 4. Add 3 fresca                                    |
| **Expected result** | fresca: 3  polo: 0  beer: 0  coke: 1               |
| **Total price**     | 54                                                 |

---

### TC-R6-003

| Field               | Detail                                             |
|---------------------|----------------------------------------------------|
| **Title**           | Remove coke and fresca, then add 3 fresca and coke |
| **Priority**        | High                                               |
| **Preconditions**   | Add 3 fresca<br>Choose free coke                   |
| **Steps**           | 1. Remove coke                                     |
|                     | 2. Remove fresca                                   |
|                     | 3. Add 3 fresca                                    |
|                     | 4. Add 1 coke                                      |
| **Expected result** | fresca: 3  polo: 0  beer: 0  coke: 1               |
| **Total price**     | 54                                                 |

---

### TC-R6-004

| Field               | Detail                                         |
|---------------------|------------------------------------------------|
| **Title**           | Remove beer and polo, then add beer and 3 polo |
| **Priority**        | High                                           |
| **Preconditions**   | Add 3 polo<br>Choose free beer                 |
| **Steps**           | 1. Remove beer                                 |
|                     | 2. Remove polo                                 |
|                     | 3. Add 1 beer                                  |
|                     | 4. Add 3 polo                                  |
| **Expected result** | fresca: 0  polo: 3  beer: 1  coke: 0           |
| **Total price**     | 45                                             |

---

### TC-R6-005

| Field               | Detail                                         |
|---------------------|------------------------------------------------|
| **Title**           | Remove beer and polo, then add 3 polo and beer |
| **Priority**        | High                                           |
| **Preconditions**   | Add 3 polo<br>Choose free beer                 |
| **Steps**           | 1. Remove beer                                 |
|                     | 2. Remove polo                                 |
|                     | 3. Add 3 polo                                  |
|                     | 4. Add 1 beer                                  |
| **Expected result** | fresca: 0  polo: 3  beer: 1  coke: 0           |
| **Total price**     | 45                                             |

---

### TC-R8-001

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Clear all after adding 1 coke               |
| **Priority**         | Medium                                      |
| **Preconditions**    | Add 1 coke                                  |
| **Steps**            | 1. Clear all                                |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R8-002

| Field               | Detail                                            |
|---------------------|---------------------------------------------------|
| **Title**           | Clear all after adding 3 polo with nothing chosen |
| **Priority**        | Medium                                            |
| **Preconditions**   | Add 3 polo<br>Choose nothing                      |
| **Steps**           | 1. Clear all                                      |
| **Expected result** | fresca: 0  polo: 0  beer: 0  coke: 0              |
| **Total price**     | 0                                                 |

---

### TC-R8-003

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Clear all after choosing free coke          |
| **Priority**         | High                                        |
| **Preconditions**    | Add 3 polo<br>Choose free coke              |
| **Steps**            | 1. Clear all                                |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R8-004

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Clear all after choosing free beer          |
| **Priority**         | High                                        |
| **Preconditions**    | Add 3 fresca<br>Choose free beer            |
| **Steps**            | 1. Clear all                                |
| **Expected result**  | fresca: 0  polo: 0  beer: 0  coke: 0        |
| **Total price**      | 0                                           |

---

### TC-R8-005

| Field                | Detail                                      |
|----------------------|---------------------------------------------|
| **Title**            | Clear all then add 3 polo                   |
| **Priority**         | High                                        |
| **Preconditions**    | Add 3 fresca<br>Choose free beer            |
| **Steps**            | 1. Clear all                                |
|                      | 2. Add 3 polo                               |
| **Expected result**  | fresca: 0  polo: 3  beer: 0  coke: 0        |
| **Total price**      | 45                                          |
