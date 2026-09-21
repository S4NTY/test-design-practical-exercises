# Test Cases — Paid vacation days

**Module:** paid-vacation-days  
**Tester:** Alexandr Gusev  
**Total Cases:** 13  
**Version:** 1.0  

---

## Summary Tables
### Summary table of positive tests


| Case      | Age | Years of service | Expected paid vacation days |
|-----------|-----|------------------|-----------------------------|
| TC-PV-001 | 17  | 29               | 27                          |
| TC-PV-002 | 18  | 29               | 24                          |
| TC-PV-003 | 18  | 30               | 27                          |
| TC-PV-004 | 18  | 10               | 22                          |
| TC-PV-005 | 44  | 14               | 22                          |
| TC-PV-006 | 45  | 14               | 24                          |
| TC-PV-007 | 44  | 15               | 24                          |
| TC-PV-008 | 59  | 29               | 24                          |
| TC-PV-009 | 60  | 29               | 27                          |
| TC-PV-010 | 59  | 30               | 27                          |
| TC-PV-011 | 60  | 30               | 30                          |


---

### Summary table of negative tests

| Case      | Age | Years of service | Expected result  |
|-----------|-----|------------------|------------------|
| TC-PV-012 | -1  | 10               | Validation Error |
| TC-PV-013 | 30  | -1               | Validation Error |


---

## Detailed Test Cases

### TC-PV-001

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age < 18, Years of service = 29                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 17<br>2. Enter Years of service = 29 |
| **Expected**      | Paid vacation days = 27                             |


---

### TC-PV-002

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 18, Years of service = 29                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 18<br>2. Enter Years of service = 29 |
| **Expected**      | Paid vacation days = 24                             |


---

### TC-PV-003

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 18, Years of service = 30                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 18<br>2. Enter Years of service = 30 |
| **Expected**      | Paid vacation days = 27                             |


---

### TC-PV-004

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 18, Years of service = 10                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 18<br>2. Enter Years of service = 10 |
| **Expected**      | Paid vacation days = 22                             |


---

### TC-PV-005

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 44, Years of service = 14                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 44<br>2. Enter Years of service = 14 |
| **Expected**      | Paid vacation days = 22                             |


---

### TC-PV-006

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 45, Years of service = 14                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 45<br>2. Enter Years of service = 14 |
| **Expected**      | Paid vacation days = 24                             |


---

### TC-PV-007

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 44, Years of service = 15                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 44<br>2. Enter Years of service = 15 |
| **Expected**      | Paid vacation days = 24                             |


---

### TC-PV-008

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 59, Years of service = 29                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 59<br>2. Enter Years of service = 29 |
| **Expected**      | Paid vacation days = 24                             |


---

### TC-PV-009

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 60, Years of service = 29                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 60<br>2. Enter Years of service = 29 |
| **Expected**      | Paid vacation days = 27                             |


---

### TC-PV-010

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 59, Years of service = 30                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 59<br>2. Enter Years of service = 30 |
| **Expected**      | Paid vacation days = 27                             |


---

### TC-PV-011

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Age = 60, Years of service = 30                     |
| **Priority**      | Critical                                            |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 60<br>2. Enter Years of service = 30 |
| **Expected**      | Paid vacation days = 30                             |


---

### TC-PV-012

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Negative Age value                                  |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = -1<br>2. Enter Years of service = 10 |
| **Expected**      | Validation Error                                    |


---

### TC-PV-013

| Field             | Detail                                              |
|-------------------|-----------------------------------------------------|
| **Title**         | Negative Years of service value                     |
| **Priority**      | High                                                |
| **Preconditions** | Web page is open                                    |
| **Steps**         | 1. Enter Age = 30<br>2. Enter Years of service = -1 |
| **Expected**      | Validation Error                                    |
