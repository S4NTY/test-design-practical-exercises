# Test Cases — University course grade system

**Module:** university-grade  
**Tester:** Alexandr Gusev  
**Total Cases:** 14  
**Version:** 1.0  

---

## Summary Tables

### Summary table of tests


| Case      | BE | LE | WP | Expected result |
|-----------|----|----|----|-----------------|
| TC-UG-001 | 20 | 50 | 50 | failed          |
| TC-UG-002 | 24 | 50 | 50 | failed          |
| TC-UG-003 | 50 | 20 | 50 | failed          |
| TC-UG-004 | 50 | 24 | 50 | failed          |
| TC-UG-005 | 50 | 50 | 20 | failed          |
| TC-UG-006 | 50 | 50 | 24 | failed          |
| TC-UG-007 | 25 | 50 | 50 | good            |
| TC-UG-008 | 50 | 50 | 30 | very good       |
| TC-UG-009 | 25 | 25 | 25 | failed          |
| TC-UG-010 | 26 | 25 | 25 | satisfactory    |
| TC-UG-011 | 40 | 30 | 30 | satisfactory    |
| TC-UG-012 | 40 | 30 | 31 | good            |
| TC-UG-013 | 40 | 40 | 45 | good            |
| TC-UG-014 | 41 | 40 | 45 | very good       |

---

## Detailed Test Cases

### TC-UG-001

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | BE < 25 (BE = 20)                                        |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 20<br>2. Enter LE = 50<br>3. Enter WP = 50 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-002

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | BE = 24 (boundary < 25)                                  |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 24<br>2. Enter LE = 50<br>3. Enter WP = 50 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-003

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | LE < 25 (LE = 20)                                        |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 50<br>2. Enter LE = 20<br>3. Enter WP = 50 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-004

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | LE = 24 (boundary < 25)                                  |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 50<br>2. Enter LE = 24<br>3. Enter WP = 50 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-005

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | WP < 25 (WP = 20)                                        |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 50<br>2. Enter LE = 50<br>3. Enter WP = 20 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-006

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | WP = 24 (boundary < 25)                                  |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 50<br>2. Enter LE = 50<br>3. Enter WP = 24 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-007

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | All ≥ 25, SUM = 125 (upper boundary of “good”)           |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 25<br>2. Enter LE = 50<br>3. Enter WP = 50 |
| **Expected**      | Course result = good                                     |

---

### TC-UG-008

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | SUM > 125 (very good)                                    |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 50<br>2. Enter LE = 50<br>3. Enter WP = 30 |
| **Expected**      | Course result = very good                                |

---

### TC-UG-009

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | All = 25, SUM = 75 (< 76)                                |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 25<br>2. Enter LE = 25<br>3. Enter WP = 25 |
| **Expected**      | Course result = failed                                   |

---

### TC-UG-010

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | SUM = 76 (lower boundary of “satisfactory”)              |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 26<br>2. Enter LE = 25<br>3. Enter WP = 25 |
| **Expected**      | Course result = satisfactory                             |

---

### TC-UG-011

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | SUM = 100 (upper boundary of “satisfactory”)             |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 40<br>2. Enter LE = 30<br>3. Enter WP = 30 |
| **Expected**      | Course result = satisfactory                             |

---

### TC-UG-012

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | SUM = 101 (lower boundary of “good”)                     |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 40<br>2. Enter LE = 30<br>3. Enter WP = 31 |
| **Expected**      | Course result = good                                     |

---

### TC-UG-013

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | SUM = 125 (upper boundary of “good”)                     |
| **Priority**      | High                                                     |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 40<br>2. Enter LE = 40<br>3. Enter WP = 45 |
| **Expected**      | Course result = good                                     |

---

### TC-UG-014

| Field             | Detail                                                   |
|-------------------|----------------------------------------------------------|
| **Title**         | SUM = 126 (lower boundary of “very good”)                |
| **Priority**      | Critical                                                 |
| **Preconditions** | Web page is open                                         |
| **Steps**         | 1. Enter BE = 41<br>2. Enter LE = 40<br>3. Enter WP = 45 |
| **Expected**      | Course result = very good                                |
