# Test Cases — Car Rental

**Module:** car-rental
**Tester:** Alexandr Gusev  
**Total Cases:**  
**Version:** 1.0  

---

## State Diagram

![state diagram.png](state%20diagram.png)

---

## Summary Tables

| Case    | Preconditions   | Steps                               | Expected result     | Total rental price |
|---------|-----------------|-------------------------------------|---------------------|--------------------|
| Case 1  | 0 cars, 0 bikes | Add 2 cars                          | 2 cars, 0 bikes     | 600                |
| Case 2  | 0 cars, 0 bikes | Add 2 bikes                         | 0 cars, 2 bikes     | 200                |
| Case 3  | 0 cars, 2 bikes | Remove 1 bike                       | 0 cars, 1 bike      | 100                |
| Case 4  | 2 cars, 0 bikes | Remove 1 car                        | 1 car, 0 bikes      | 300                |
| Case 5  | 0 cars, 0 bikes | Add 3 cars                          | 3 cars, 1 free bike | 900                |
| Case 6  | 0 cars, 1 bike  | Add 3 cars                          | 3 cars, 1 free bike | 900                |
| Case 7  | 0 cars, 2 bikes | Add 3 cars                          | 3 cars, 2 bikes     | 1000               |
| Case 8  | 3 cars, 0 bikes | Remove 2 cars                       | 1 car, 0 bikes      | 300                |
| Case 9  | 3 cars, 1 bike  | Remove 1 car                        | 2 cars, 1 bike      | 700                |
| Case 10 | 3 cars, 2 bikes | Remove 1 bike                       | 3 cars, 1 bike      | 900                |
| Case 11 | 4 cars, 0 bikes | Remove 1 car                        | 3 cars, 1 free bike | 900                |
| Case 12 | 3 cars, 0 bikes | Remove 1 free bike, Add car         | 4 cars, 1 free bike | 1200               |
| Case 13 | 3 cars, 0 bikes | Remove 1 free bike, Remove car      | 2 cars, 0 bikes     | 600                |
| Case 14 | 3 cars, 0 bikes | Remove 1 free bike, Add bike        | 3 cars, 1 bike      | 900                |

---

## Detailed Test Cases

### TC-CR-001

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Add 2 cars                                               |
| **Priority**      | High                                                     |
| **Preconditions** | 0 cars, 0 bikes                                          |
| **Steps**         | 1. Add 1 car<br>2. Add 1 car                             |
| **Expected**      | 2 cars, 0 bikes; Total rental price = 600                |

---

### TC-CR-002

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Add 2 bikes                                              |
| **Priority**      | High                                                     |
| **Preconditions** | 0 cars, 0 bikes                                          |
| **Steps**         | 1. Add 1 bike<br>2. Add 1 bike                           |
| **Expected**      | 0 cars, 2 bikes; Total rental price = 200                |

---

### TC-CR-003

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove 1 bike                                            |
| **Priority**      | Medium                                                   |
| **Preconditions** | 0 cars, 2 bikes                                          |
| **Steps**         | 1. Remove 1 bike                                         |
| **Expected**      | 0 cars, 1 bike; Total rental price = 100                 |

---

### TC-CR-004

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove 1 car                                             |
| **Priority**      | Medium                                                   |
| **Preconditions** | 2 cars, 0 bikes                                          |
| **Steps**         | 1. Remove 1 car                                          |
| **Expected**      | 1 car, 0 bikes; Total rental price = 300                 |

---

### TC-CR-005

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Add 3 cars — free bike added (R3b)                       |
| **Priority**      | Critical                                                 |
| **Preconditions** | 0 cars, 0 bikes                                          |
| **Steps**         | 1. Add 1 car<br>2. Add 1 car<br>3. Add 1 car             |
| **Expected**      | 3 cars, 1 free bike; Total rental price = 900            |

---

### TC-CR-006

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Add 3 cars with 1 bike — bike becomes free (R3a)         |
| **Priority**      | Critical                                                 |
| **Preconditions** | 0 cars, 1 bike                                           |
| **Steps**         | 1. Add 1 car<br>2. Add 1 car<br>3. Add 1 car             |
| **Expected**      | 3 cars, 1 free bike; Total rental price = 900            |

---

### TC-CR-007

| Field             | Detail                                                       |
|-------------------|--------------------------------------------------------------|
| **Title**         | Add 3 cars with 2 bikes — only one bike is free (R3a)        |
| **Priority**      | High                                                         |
| **Preconditions** | 0 cars, 2 bikes                                              |
| **Steps**         | 1. Add 1 car<br>2. Add 1 car<br>3. Add 1 car                 |
| **Expected**      | 3 cars, 1 free bike + 1 paid bike; Total rental price = 1000 |

---

### TC-CR-008

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove 2 cars — threshold no longer holds                |
| **Priority**      | High                                                     |
| **Preconditions** | 3 cars, 0 bikes                                          |
| **Steps**         | 1. Remove 1 car<br>2. Remove 1 car                       |
| **Expected**      | 1 car, 0 bikes; Total rental price = 300                 |

---

### TC-CR-009

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove 1 car — free bike becomes paid (R4)               |
| **Priority**      | Critical                                                 |
| **Preconditions** | 3 cars, 1 free bike                                      |
| **Steps**         | 1. Remove 1 car                                          |
| **Expected**      | 2 cars, 1 paid bike; Total rental price = 700            |

---

### TC-CR-010

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove 1 paid bike — free bike remains                   |
| **Priority**      | Medium                                                   |
| **Preconditions** | 3 cars, 2 bikes (1 free)                                 |
| **Steps**         | 1. Remove 1 paid bike                                    |
| **Expected**      | 3 cars, 1 free bike; Total rental price = 900            |

---

### TC-CR-011

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove 1 car from 4 — free bike added (R3b)              |
| **Priority**      | High                                                     |
| **Preconditions** | 4 cars, 0 bikes                                          |
| **Steps**         | 1. Remove 1 car                                          |
| **Expected**      | 3 cars, 1 free bike; Total rental price = 900            |

---

### TC-CR-012

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove free bike, then add car (R5)                      |
| **Priority**      | High                                                     |
| **Preconditions** | 3 cars, 0 bikes                                          |
| **Steps**         | 1. Remove 1 free bike<br>2. Add 1 car                    |
| **Expected**      | 4 cars, 1 free bike; Total rental price = 1200           |

---

### TC-CR-013

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove free bike, then remove car — discount withdrawn   |
| **Priority**      | Medium                                                   |
| **Preconditions** | 3 cars, 0 bikes                                          |
| **Steps**         | 1. Remove 1 free bike<br>2. Remove 1 car                 |
| **Expected**      | 2 cars, 0 bikes; Total rental price = 600                |

---

### TC-CR-014

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | Remove free bike, then add bike — bike becomes free (R5) |
| **Priority**      | High                                                     |
| **Preconditions** | 3 cars, 0 bikes                                          |
| **Steps**         | 1. Remove 1 free bike<br>2. Add 1 bike                   |
| **Expected**      | 3 cars, 1 free bike; Total rental price = 900            |

---

