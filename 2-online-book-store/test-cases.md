# Test Cases — Online book store

**Module:** online-book-store  
**Tester:** Alexandr Gusev  
**Total Cases:** 13  
**Version:** 1.0  

---

## Summary Tables
### Summary table of positive tests

| Case       | New book price | Second hand book price | VIP | Expected total price |
|------------|----------------|------------------------|-----|----------------------|
| TC-OBS-001 | 49.99          | 0                      | Yes | 44.99                |
| TC-OBS-002 | 49.99          | 0                      | No  | 49.99                |
| TC-OBS-003 | 50             | 0                      | Yes | 42.5                 |
| TC-OBS-004 | 50.01          | 0                      | No  | 45.01                |
| TC-OBS-005 | 30.01          | 60                     | Yes | 87.01                |
| TC-OBS-006 | 30             | 60.01                  | No  | 90.01                |
| TC-OBS-007 | 30.01          | 60.01                  | Yes | 84.02                |
| TC-OBS-008 | 50             | 60.01                  | No  | 102.01               |
| TC-OBS-009 | 50             | 60.01                  | Yes | 99.51                |

---

### Summary table of negative tests
| Case       | New book price | Second hand book price | VIP | Expected total price |
|------------|----------------|------------------------|-----|----------------------|
| TC-OBS-010 | abc            | 0                      | Yes | NaN                  |
| TC-OBS-011 | 0              | abc                    | No  | NaN                  |
| TC-OBS-012 | -1             | 0                      | Yes | Validation Error     |
| TC-OBS-013 | 0              | -1                     | No  | Validation Error     |


---

## Detailed Test Cases

### TC-OBS-001

| Field             | Detail                                                                                        |
|-------------------|-----------------------------------------------------------------------------------------------|
| **Title**         | New book price < 50, no second hand book, VIP = Yes                                           |
| **Priority**      | High                                                                                          |
| **Preconditions** | Web page is open                                                                              |
| **Steps**         | 1. Enter New book price = 49.99<br>2. Enter second hand book price = 0<br>3. Select VIP = Yes |
| **Expected**      | Total price = 44.99                                                                           |


---

### TC-OBS-002

| Field             | Detail                                                                                       |
|-------------------|----------------------------------------------------------------------------------------------|
| **Title**         | New book price < 50, no second hand book, VIP = No                                           |
| **Priority**      | Medium                                                                                       |
| **Preconditions** | Web page is open                                                                             |
| **Steps**         | 1. Enter New book price = 49.99<br>2. Enter second hand book price = 0<br>3. Select VIP = No |
| **Expected**      | Total price = 49.99                                                                          |


---

### TC-OBS-003

| Field             | Detail                                                                                     |
|-------------------|--------------------------------------------------------------------------------------------|
| **Title**         | New book price = 50, no second hand book, VIP = Yes                                        |
| **Priority**      | Critical                                                                                   |
| **Preconditions** | Web page is open                                                                           |
| **Steps**         | 1. Enter New book price = 50<br>2. Enter second hand book price = 0<br>3. Select VIP = Yes |
| **Expected**      | Total price = 42.5                                                                         |


---

### TC-OBS-004

| Field             | Detail                                                                                       |
|-------------------|----------------------------------------------------------------------------------------------|
| **Title**         | New book price > 50, no second hand book, VIP = No                                           |
| **Priority**      | High                                                                                         |
| **Preconditions** | Web page is open                                                                             |
| **Steps**         | 1. Enter New book price = 50.01<br>2. Enter second hand book price = 0<br>3. Select VIP = No |
| **Expected**      | Total price = 45.01                                                                          |


---

### TC-OBS-005

| Field             | Detail                                                                                         |
|-------------------|------------------------------------------------------------------------------------------------|
| **Title**         | New book price > 30, second hand book price = 60, VIP = Yes                                    |
| **Priority**      | High                                                                                           |
| **Preconditions** | Web page is open                                                                               |
| **Steps**         | 1. Enter New book price = 30.01<br>2. Enter second hand book price = 60<br>3. Select VIP = Yes |
| **Expected**      | Total price = 87.01                                                                            |


---

### TC-OBS-006

| Field             | Detail                                                                                        |
|-------------------|-----------------------------------------------------------------------------------------------|
| **Title**         | New book price = 30, second hand book price > 60, VIP = No                                    |
| **Priority**      | Medium                                                                                        |
| **Preconditions** | Web page is open                                                                              |
| **Steps**         | 1. Enter New book price = 30<br>2. Enter second hand book price = 60.01<br>3. Select VIP = No |
| **Expected**      | Total price = 90.01                                                                           |


---

### TC-OBS-007

| Field             | Detail                                                                                            |
|-------------------|---------------------------------------------------------------------------------------------------|
| **Title**         | New book price > 30, second hand book price > 60, VIP = Yes                                       |
| **Priority**      | Critical                                                                                          |
| **Preconditions** | Web page is open                                                                                  |
| **Steps**         | 1. Enter New book price = 30.01<br>2. Enter second hand book price = 60.01<br>3. Select VIP = Yes |
| **Expected**      | Total price = 84.02                                                                               |


---

### TC-OBS-008

| Field             | Detail                                                                                        |
|-------------------|-----------------------------------------------------------------------------------------------|
| **Title**         | New book price = 50, second hand book price > 60, VIP = No                                    |
| **Priority**      | High                                                                                          |
| **Preconditions** | Web page is open                                                                              |
| **Steps**         | 1. Enter New book price = 50<br>2. Enter second hand book price = 60.01<br>3. Select VIP = No |
| **Expected**      | Total price = 102.01                                                                          |


---

### TC-OBS-009

| Field             | Detail                                                                                         |
|-------------------|------------------------------------------------------------------------------------------------|
| **Title**         | New book price = 50, second hand book price > 60, VIP = Yes                                    |
| **Priority**      | Critical                                                                                       |
| **Preconditions** | Web page is open                                                                               |
| **Steps**         | 1. Enter New book price = 50<br>2. Enter second hand book price = 60.01<br>3. Select VIP = Yes |
| **Expected**      | Total price = 99.51                                                                            |


---

### TC-OBS-010

| Field             | Detail                                                                                      |
|-------------------|---------------------------------------------------------------------------------------------|
| **Title**         | Invalid new book price (letters instead of number)                                          |
| **Priority**      | High                                                                                        |
| **Preconditions** | Web page is open                                                                            |
| **Steps**         | 1. Enter New book price = abc<br>2. Enter second hand book price = 0<br>3. Select VIP = Yes |
| **Expected**      | NaN / Validation Error                                                                      |


---

### TC-OBS-011

| Field             | Detail                                                                                     |
|-------------------|--------------------------------------------------------------------------------------------|
| **Title**         | Invalid second hand book price (letters instead of number)                                 |
| **Priority**      | High                                                                                       |
| **Preconditions** | Web page is open                                                                           |
| **Steps**         | 1. Enter New book price = 0<br>2. Enter second hand book price = abc<br>3. Select VIP = No |
| **Expected**      | NaN / Validation Error                                                                     |


---

### TC-OBS-012

| Field             | Detail                                                                                     |
|-------------------|--------------------------------------------------------------------------------------------|
| **Title**         | Negative new book price                                                                    |
| **Priority**      | High                                                                                       |
| **Preconditions** | Web page is open                                                                           |
| **Steps**         | 1. Enter New book price = -1<br>2. Enter second hand book price = 0<br>3. Select VIP = Yes |
| **Expected**      | Validation Error                                                                           |


---

### TC-OBS-013

| Field             | Detail                                                                                    |
|-------------------|-------------------------------------------------------------------------------------------|
| **Title**         | Negative second hand book price                                                           |
| **Priority**      | High                                                                                      |
| **Preconditions** | Web page is open                                                                          |
| **Steps**         | 1. Enter New book price = 0<br>2. Enter second hand book price = -1<br>3. Select VIP = No |
| **Expected**      | Validation Error                                                                          |