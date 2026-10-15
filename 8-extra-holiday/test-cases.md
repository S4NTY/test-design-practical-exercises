# Test Cases — Extra holiday

**Module:** extra-holiday  
**Tester:** Alexandr Gusev  
**Total Cases:** 10  
**Version:** 1.0

---

## Summary Tables

| Case      | Steps                                                                                                      | Expected result                              |
|-----------|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| TC-EH-001 | Add 3 extra day<br>Add 1 lateness                                                                          | Extra days: 0<br>Free days: 0                |
| TC-EH-002 | Add 4 extra day<br>Add 1 lateness                                                                          | Extra days: 1<br>Free days: 0                |
| TC-EH-003 | Get 1 free day                                                                                             | Extra days: 0<br>Free days: 0                |
| TC-EH-004 | Add 9 extra day<br>Get 3 free days<br>Add 2 lateness                                                       | Extra days: -2<br>Free days: 0               |
| TC-EH-005 | Add 9 extra day<br>Get 1 free day<br>Add 1 lateness<br>Add 1 extra day<br>Get 2 free day<br>Add 1 lateness | Extra days: 1<br>Free days: 0                |
| TC-EH-006 | Add 1 lateness<br>Add 1 extra day<br>Add 1 lateness                                                        | Extra days: 0<br>Free days: -1               |
| TC-EH-007 | Add 5 lateness                                                                                             | Extra days: -1<br>Free days: -3<br>Game Over |
| TC-EH-008 | Add 5 lateness<br>Add 1 extra day                                                                          | Extra days: -1<br>Free days: -3<br>Game Over |
| TC-EH-009 | Add 5 lateness<br>Get 1 free day                                                                           | Extra days: -1<br>Free days: -3<br>Game Over |
| TC-EH-010 | Add 6 lateness                                                                                             | Extra days: -1<br>Free days: -3<br>Game Over |

---

## Detailed Test Cases

### TC-EH-001

| Field        | Detail                                  |
|--------------|-----------------------------------------|
| **Title**    | Overtime accumulation without lateness  |
| **Priority** | High                                    |
| **Steps**    | 1. Add 3 extra day<br>2. Add 1 lateness |
| **Expected** | Extra days: 0<br>Free days: 0           |

---

### TC-EH-002

| Field        | Detail                                         |
|--------------|------------------------------------------------|
| **Title**    | Overtime carries over after lateness deduction |
| **Priority** | High                                           |
| **Steps**    | 1. Add 4 extra day<br>2. Add 1 lateness        |
| **Expected** | Extra days: 1<br>Free days: 0                  |

---

### TC-EH-003

| Field        | Detail                                     |
|--------------|--------------------------------------------|
| **Title**    | Taking a free day with no overtime balance |
| **Priority** | High                                       |
| **Steps**    | 1. Get 1 free day                          |
| **Expected** | Extra days: 0<br>Free days: 0              |

---

### TC-EH-004

| Field        | Detail                                                                 |
|--------------|------------------------------------------------------------------------|
| **Title**    | Lateness with zero overtime and zero free days withdraws two overtimes |
| **Priority** | Critical                                                               |
| **Steps**    | 1. Add 9 extra day<br>2. Get 3 free days<br>3. Add 2 lateness          |
| **Expected** | Extra days: -2<br>Free days: 0                                         |

---

### TC-EH-005

| Field        | Detail                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------|
| **Title**    | R5 – three free days without lateness protects subsequent one-time lateness                                                  |
| **Priority** | Critical                                                                                                                     |
| **Steps**    | 1. Add 9 extra day<br>2. Get 1 free day<br>3. Add 1 lateness<br>4. Add 1 extra day<br>5. Get 2 free day<br>6. Add 1 lateness |
| **Expected** | Extra days: 1<br>Free days: 0                                                                                                |

---

### TC-EH-006

| Field        | Detail                                                       |
|--------------|--------------------------------------------------------------|
| **Title**    | Lateness with negative overtime reduces free days            |
| **Priority** | High                                                         |
| **Steps**    | 1. Add 1 lateness<br>2. Add 1 extra day<br>3. Add 1 lateness |
| **Expected** | Extra days: 0<br>Free days: -1                               |

---

### TC-EH-007

| Field        | Detail                                               |
|--------------|------------------------------------------------------|
| **Title**    | GAME OVER after five latenesses (free days reach -3) |
| **Priority** | Critical                                             |
| **Steps**    | 1. Add 5 lateness                                    |
| **Expected** | Extra days: -1<br>Free days: -3<br>Game Over         |

---

### TC-EH-008

| Field        | Detail                                          |
|--------------|-------------------------------------------------|
| **Title**    | GAME OVER cannot be reverted by adding overtime |
| **Priority** | Critical                                        |
| **Steps**    | 1. Add 5 lateness<br>2. Add 1 extra day         |
| **Expected** | Extra days: -1<br>Free days: -3<br>Game Over    |

---

### TC-EH-009

| Field        | Detail                                            |
|--------------|---------------------------------------------------|
| **Title**    | GAME OVER cannot be reverted by taking a free day |
| **Priority** | Critical                                          |
| **Steps**    | 1. Add 5 lateness<br>2. Get 1 free day            |
| **Expected** | Extra days: -1<br>Free days: -3<br>Game Over      |

---

### TC-EH-010

| Field        | Detail                                                       |
|--------------|--------------------------------------------------------------|
| **Title**    | GAME OVER persists with additional lateness beyond threshold |
| **Priority** | Critical                                                     |
| **Steps**    | 1. Add 6 lateness                                            |
| **Expected** | Extra days: -1<br>Free days: -3<br>Game Over                 |