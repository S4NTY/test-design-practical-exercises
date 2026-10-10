# Test Cases — Tour competition

**Module:** tour-competition  
**Tester:** Alexandr Gusev  
**Total Cases:** 35  
**Version:** 1.0  

---

## State Diagram

![state diagram.png](state%20diagram.png)

---

## Summary Tables

| Case  | Preconditions                                                     | Steps                                        | Expected message                  | Expected result                                                   |
|-------|-------------------------------------------------------------------|----------------------------------------------|-----------------------------------|-------------------------------------------------------------------|
| R1.1  | "a": {"1", "2", "3"}                                              | "b": {"4", "5", "6"}                         | new team inserted                 | "a": {"1", "2", "3"}<br>"b": {"4", "5", "6"}                      |
| R1.2  |                                                                   | "a": {"1", "", ""}                           | new team inserted                 | "a": {"1", "", ""}                                                |
| R1.3  |                                                                   | "": {"1", "", ""}                            | Team name cannot be empty         | not created                                                       |
| R1.4  | "a": {"1", "2", "3"}                                              | "b": {"1", "4", "5"}                         | all team members should be unique | "a": {"1", "2", "3"}                                              |
| R1.5  |                                                                   | "a": {"1", "1", "2"}                         | members should be different       | not created                                                       |
| R1.6  |                                                                   | "a": {"1", "2", "2"}                         | members should be different       | not created                                                       |
| R1.7  |                                                                   | "": {"", "", ""}                             | At least one member is needed     | not created                                                       |
| R2.1  | "a": {"1", "", ""}                                                | "a": {"1", "2", ""}                          | team modified                     | "a": {"1", "2", ""}                                               |
| R2.2  | "a": {"1", "2", ""}                                               | "a": {"1", "2", "3"}                         | team modified                     | "a": {"1", "2", "3"}                                              |
| R2.3  | "a": {"1", "", ""}                                                | "a": {"1", "2", "3"}                         | team modified                     | "a": {"1", "2", "3"}                                              |
| R2.4  | "a": {"1", "", ""}                                                | "a": {"2", "", ""}                           | team modified                     | "a": {"2", "", ""}                                                |
| R2.5  | "a": {"1", "2", "3"}                                              | "a": {"4", "5", "6"}                         | team modified                     | "a": {"4", "5", "6"}                                              |
| R2.6  | "a": {"1", "2", ""}                                               | "a": {"", "2", ""}                           | team modified                     | "a": {"", "2", ""}                                                |
| R2.7  | "a": {"1", "2", "3"}                                              | "a": {"", "", "3"}                           | team modified                     | "a": {"", "", "3"}                                                |
| R3.1  | "a": {"1", "2", ""}                                               | "b": {"1", "3", "4"}                         | new team inserted                 | "a": {"", "2", ""}<br>"b": {"1", "3", "4"}                        |
| R3.2  | "a": {"1", "2", ""}                                               | "b": {"1", "3", ""}                          | only complete team can stole      | "a": {"1", "2", ""}                                               |
| R3.3  | "a": {"1", "2", "3"}<br>"b": {"4", "", ""}                        | "b": {"4", "2", "3"}                         | all team members should be unique | "a": {"1", "2", "3"}<br>"b": {"4", "", ""}                        |
| R3.4  | "a": {"1", "2", ""}<br>"b": {"3", "4", "5"}                       | "b": {"2", "4", "6"}                         | team modified                     | "a": {"1", "", ""}<br>"b": {"2", "4", "6"}                        |
| R4.1  | "a": {"1", "2", "3"}                                              | "b": {"1", "2", "3"}                         | all team members should be unique | "a": {"1", "2", "3"}                                              |
| R4.2  | "a": {"1", "2", ""}<br>"b": {"3", "4", ""}<br>"c": {"5", "6", ""} | "d": {"1", "4", "5"}                         | All members cannot be 'stolen'    | "a": {"1", "2", ""}<br>"b": {"3", "4", ""}<br>"c": {"5", "6", ""} |
| R5.1  | "a": {"1", "", ""}                                                | "b": {"1", "2", "3"}                         | new team inserted                 | "a" deleted<br>"b": {"1", "2", "3"}                               |
| R5.2  | "a": {"1", "2", ""}                                               | "b": {"1", "2", "3"}                         | new team inserted                 | "a" deleted<br>"b": {"1", "2", "3"}                               |
| R5.3  | "a": {"", "2", "3"}                                               | "b": {"1", "2", "3"}                         | new team inserted                 | "a" deleted<br>"b": {"1", "2", "3"}                               |
| R5.4  | "a": {"1", "", ""}<br>"b": {"1", "2", "3"}                        | "a": {"4", "5", "6"}                         | deleted team name cannot be used  | "a" deleted<br>"b": {"1", "2", "3"}                               |
| R6.1  | "a": {"1", "", ""}<br>"b": {"1", "2", "3"}                        | b: {"4", "2", "3"}                           | Stolen member cannot be modified  | "a" deleted<br>"b": {"1", "2", "3"}                               |
| R6.2  | "a": {"1", "2", ""}<br>"b": {"1", "2", "3"}                       | b: {"1", "2", "4"}<br>b: {"5", "2", "4"}     | Stolen member cannot be modified  | "a" deleted<br>b: {"1", "2", "4"}                                 |
| R6.3  | "a": {"", "2", "3"}<br>"b": {"1", "2", "3"}                       | b: {"1", "2", "4"}                           | Stolen member cannot be modified  | "a" deleted<br>"b": {"1", "2", "3"}                               |
| R6.4  | "a": {"1", "2", "3"}<br>"b": {"4", "5", ""}                       | "a": {"4", "2", "3"}<br>"a": {"6", "2", "3"} | Stolen member cannot be modified  | "a": {"4", "2", "3"}<br>"b": {"", "5", ""}                        |
| R6.5  | "a": {"1", "", ""}<br>"b": {"1", "2", "3"}                        | "b": {"", "2", "3"}                          | team modified                     | "a" deleted<br>"b": {"", "2", "3"}                                |
| R6.6  | "a": {"", "1", ""}<br>"b": {"1", "2", "3"}                        | "b": {"1", "2", ""}<br>"c": {"3", "1", "4"}  | new team inserted                 | "a" deleted<br>"b": {"1", "2", ""}<br>"c": {"3", "1", "4"}        |
| R6.7  | "a": {"1", "", "3"}<br>"b": {"1", "2", "3"}                       | "b": {"1", "2", ""}<br>"b": {"1", "2", "4"}  | new team inserted                 | "a" deleted<br>"b": {"1", "2", ""}<br>"c": {"3", "1", "4"}        |
| R6.8  | "a": {"", "2", "3"}<br>"b": {"4", "5", "3"}                       | "a": {"3", "2", ""}                          | all team members should be unique | "a": {"", "2", ""}<br>"b": {"4", "5", "3"}                        |
| R6.9  | "a": {"", "2", "3"}<br>"b": {"4", "2", "5"}                       | "a": {"", "6", "3"}                          | team modified                     | "a": {"", "6", "3"}<br>"b": {"4", "2", "5"}                       |
| R6.10 | "a": {"1", "2", ""}<br>"b": {"3", "2", "4"}                       | "a": {"1", "5", ""}                          | team modified                     | "a": {"1", "5", ""}<br>"b": {"3", "2", "4"}                       |
| R6.11 | "a": {"1", "2", ""}<br>"b": {"1", "2", "3"}                       | "b": {"", "2", "3"}<br>"b": {"4", "2", "3"}  | team modified                     | "a" deleted<br>"b": {"4", "2", "3"}                               |

## Detailed Test Cases

### TC-R1-001

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Register two complete teams with unique members     |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists                    |
| **Steps**            | 1. Enter team name "b" with members {"4", "5", "6"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | new team inserted                                   |
| **Expected result**  | "a": {"1", "2", "3"}  "b": {"4", "5", "6"}          |

---

### TC-R1-002

| Field                | Detail                                            |
|----------------------|---------------------------------------------------|
| **Title**            | Register team with one member                     |
| **Priority**         | High                                              |
| **Preconditions**    | No teams exist                                    |
| **Steps**            | 1. Enter team name "a" with members {"1", "", ""} |
|                      | 2. Press "Add team"                               |
| **Expected message** | new team inserted                                 |
| **Expected result**  | "a": {"1", "", ""}                                |

---

### TC-R1-003

| Field                | Detail                                           |
|----------------------|--------------------------------------------------|
| **Title**            | Register team with empty team name               |
| **Priority**         | High                                             |
| **Preconditions**    | No teams exist                                   |
| **Steps**            | 1. Enter team name "" with members {"1", "", ""} |
|                      | 2. Press "Add team"                              |
| **Expected message** | Team name cannot be empty                        |
| **Expected result**  | not created                                      |

---

### TC-R1-004

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Register team with member already in another team   |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists                    |
| **Steps**            | 1. Enter team name "b" with members {"1", "4", "5"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | all team members should be unique                   |
| **Expected result**  | "a": {"1", "2", "3"}                                |

---

### TC-R1-005

| Field                | Detail                                               |
|----------------------|------------------------------------------------------|
| **Title**            | Register team with duplicate first and second member |
| **Priority**         | High                                                 |
| **Preconditions**    | No teams exist                                       |
| **Steps**            | 1. Enter team name "a" with members {"1", "1", "2"}  |
|                      | 2. Press "Add team"                                  |
| **Expected message** | members should be different                          |
| **Expected result**  | not created                                          |

---

### TC-R1-006

| Field                | Detail                                               |
|----------------------|------------------------------------------------------|
| **Title**            | Register team with duplicate second and third member |
| **Priority**         | High                                                 |
| **Preconditions**    | No teams exist                                       |
| **Steps**            | 1. Enter team name "a" with members {"1", "2", "2"}  |
|                      | 2. Press "Add team"                                  |
| **Expected message** | members should be different                          |
| **Expected result**  | not created                                          |

---

### TC-R1-007

| Field                | Detail                                          |
|----------------------|-------------------------------------------------|
| **Title**            | Register team with no members                   |
| **Priority**         | High                                            |
| **Preconditions**    | No teams exist                                  |
| **Steps**            | 1. Enter team name "" with members {"", "", ""} |
|                      | 2. Press "Add team"                             |
| **Expected message** | At least one member is needed                   |
| **Expected result**  | not created                                     |

---

### TC-R2-001

| Field                | Detail                                             |
|----------------------|----------------------------------------------------|
| **Title**            | Add second member to incomplete team               |
| **Priority**         | High                                               |
| **Preconditions**    | Team "a": {"1", "", ""} exists                     |
| **Steps**            | 1. Enter team name "a" with members {"1", "2", ""} |
|                      | 2. Press "Add team"                                |
| **Expected message** | team modified                                      |
| **Expected result**  | "a": {"1", "2", ""}                                |

---

### TC-R2-002

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Add third member to incomplete team                 |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", ""} exists                     |
| **Steps**            | 1. Enter team name "a" with members {"1", "2", "3"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | team modified                                       |
| **Expected result**  | "a": {"1", "2", "3"}                                |

---

### TC-R2-003

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Add two missing members to incomplete team          |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "", ""} exists                      |
| **Steps**            | 1. Enter team name "a" with members {"1", "2", "3"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | team modified                                       |
| **Expected result**  | "a": {"1", "2", "3"}                                |

---

### TC-R2-004

| Field                | Detail                                            |
|----------------------|---------------------------------------------------|
| **Title**            | Modify existing member in incomplete team         |
| **Priority**         | High                                              |
| **Preconditions**    | Team "a": {"1", "", ""} exists                    |
| **Steps**            | 1. Enter team name "a" with members {"2", "", ""} |
|                      | 2. Press "Add team"                               |
| **Expected message** | team modified                                     |
| **Expected result**  | "a": {"2", "", ""}                                |

---

### TC-R2-005

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Modify all members of a complete team               |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists                    |
| **Steps**            | 1. Enter team name "a" with members {"4", "5", "6"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | team modified                                       |
| **Expected result**  | "a": {"4", "5", "6"}                                |

---

### TC-R2-006

| Field                | Detail                                            |
|----------------------|---------------------------------------------------|
| **Title**            | Delete first member from incomplete team          |
| **Priority**         | High                                              |
| **Preconditions**    | Team "a": {"1", "2", ""} exists                   |
| **Steps**            | 1. Enter team name "a" with members {"", "2", ""} |
|                      | 2. Press "Add team"                               |
| **Expected message** | team modified                                     |
| **Expected result**  | "a": {"", "2", ""}                                |

---

### TC-R2-007

| Field                | Detail                                            |
|----------------------|---------------------------------------------------|
| **Title**            | Delete first and second member from complete team |
| **Priority**         | High                                              |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists                  |
| **Steps**            | 1. Enter team name "a" with members {"", "", "3"} |
|                      | 2. Press "Add team"                               |
| **Expected message** | team modified                                     |
| **Expected result**  | "a": {"", "", "3"}                                |

---

### TC-R3-001

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Steal member from incomplete team to complete team  |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", ""} exists                     |
| **Steps**            | 1. Enter team name "b" with members {"1", "3", "4"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | new team inserted                                   |
| **Expected result**  | "a": {"", "2", ""}  "b": {"1", "3", "4"}            |

---

### TC-R3-002

| Field                | Detail                                             |
|----------------------|----------------------------------------------------|
| **Title**            | Incomplete team cannot steal member                |
| **Priority**         | High                                               |
| **Preconditions**    | Team "a": {"1", "2", ""} exists                    |
| **Steps**            | 1. Enter team name "b" with members {"1", "3", ""} |
|                      | 2. Press "Add team"                                |
| **Expected message** | only complete team can stole                       |
| **Expected result**  | "a": {"1", "2", ""}                                |

---

### TC-R3-003

| Field                | Detail                                                           |
|----------------------|------------------------------------------------------------------|
| **Title**            | Attempt to steal members already in a complete team              |
| **Priority**         | High                                                             |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists, team "b": {"4", "", ""} exists |
| **Steps**            | 1. Enter team name "b" with members {"4", "2", "3"}              |
|                      | 2. Press "Add team"                                              |
| **Expected message** | all team members should be unique                                |
| **Expected result**  | "a": {"1", "2", "3"}  "b": {"4", "", ""}                         |

---

### TC-R3-004

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Steal one member from incomplete team and modify another          |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"1", "2", ""} exists, team "b": {"3", "4", "5"} exists |
| **Steps**            | 1. Enter team name "b" with members {"2", "4", "6"}               |
|                      | 2. Press "Add team"                                               |
| **Expected message** | team modified                                                     |
| **Expected result**  | "a": {"1", "", ""}  "b": {"2", "4", "6"}                          |

---

### TC-R4-001

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Attempt to steal all members from a complete team   |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists                    |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", "3"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | all team members should be unique                   |
| **Expected result**  | "a": {"1", "2", "3"}                                |

---

### TC-R4-002

| Field                | Detail                                                                             |
|----------------------|------------------------------------------------------------------------------------|
| **Title**            | Attempt to construct team only from stolen members                                 |
| **Priority**         | High                                                                               |
| **Preconditions**    | Team "a": {"1", "2", ""}, team "b": {"3", "4", ""}, team "c": {"5", "6", ""} exist |
| **Steps**            | 1. Enter team name "d" with members {"1", "4", "5"}                                |
|                      | 2. Press "Add team"                                                                |
| **Expected message** | All members cannot be 'stolen'                                                     |
| **Expected result**  | "a": {"1", "2", ""}  "b": {"3", "4", ""}  "c": {"5", "6", ""}                      |

---

### TC-R5-001

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Team deleted when its only member is stolen         |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "", ""} exists                      |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", "3"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | new team inserted                                   |
| **Expected result**  | "a" deleted  "b": {"1", "2", "3"}                   |

---

### TC-R5-002

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Team deleted when both its members are stolen       |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"1", "2", ""} exists                     |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", "3"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | new team inserted                                   |
| **Expected result**  | "a" deleted  "b": {"1", "2", "3"}                   |

---

### TC-R5-003

| Field                | Detail                                              |
|----------------------|-----------------------------------------------------|
| **Title**            | Team deleted when its last two members are stolen   |
| **Priority**         | High                                                |
| **Preconditions**    | Team "a": {"", "2", "3"} exists                     |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", "3"} |
|                      | 2. Press "Add team"                                 |
| **Expected message** | new team inserted                                   |
| **Expected result**  | "a" deleted  "b": {"1", "2", "3"}                   |

---

### TC-R5-004

| Field                | Detail                                                           |
|----------------------|------------------------------------------------------------------|
| **Title**            | Deleted team name cannot be reused                               |
| **Priority**         | High                                                             |
| **Preconditions**    | Team "a": {"1", "", ""} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "a" with members {"4", "5", "6"}              |
|                      | 2. Press "Add team"                                              |
| **Expected message** | deleted team name cannot be used                                 |
| **Expected result**  | "a" deleted  "b": {"1", "2", "3"}                                |

---

### TC-R6-001

| Field                | Detail                                                           |
|----------------------|------------------------------------------------------------------|
| **Title**            | Stolen member cannot be modified                                 |
| **Priority**         | High                                                             |
| **Preconditions**    | Team "a": {"1", "", ""} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"4", "2", "3"}              |
|                      | 2. Press "Add team"                                              |
| **Expected message** | Stolen member cannot be modified                                 |
| **Expected result**  | "a" deleted  "b": {"1", "2", "3"}                                |

---

### TC-R6-002

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Stolen member cannot be modified after multiple changes           |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"1", "2", ""} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", "4"}               |
|                      | 2. Press "Add team"                                               |
|                      | 3. Enter team name "b" with members {"5", "2", "4"}               |
|                      | 4. Press "Add team"                                               |
| **Expected message** | Stolen member cannot be modified                                  |
| **Expected result**  | "a" deleted  "b": {"1", "2", "4"}                                 |

---

### TC-R6-003

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Stolen member cannot be modified (third position)                 |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"", "2", "3"} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", "4"}               |
|                      | 2. Press "Add team"                                               |
| **Expected message** | Stolen member cannot be modified                                  |
| **Expected result**  | "a" deleted  "b": {"1", "2", "3"}                                 |

---

### TC-R6-004

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Stolen member cannot be modified in incomplete team               |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"1", "2", "3"} exists, team "b": {"4", "5", ""} exists |
| **Steps**            | 1. Enter team name "a" with members {"4", "2", "3"}               |
|                      | 2. Press "Add team"                                               |
|                      | 3. Enter team name "a" with members {"6", "2", "3"}               |
|                      | 4. Press "Add team"                                               |
| **Expected message** | Stolen member cannot be modified                                  |
| **Expected result**  | "a": {"4", "2", "3"}  "b": {"", "5", ""}                          |

---

### TC-R6-005

| Field                | Detail                                                           |
|----------------------|------------------------------------------------------------------|
| **Title**            | Delete stolen member from complete team                          |
| **Priority**         | High                                                             |
| **Preconditions**    | Team "a": {"1", "", ""} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"", "2", "3"}               |
|                      | 2. Press "Add team"                                              |
| **Expected message** | team modified                                                    |
| **Expected result**  | "a" deleted  "b": {"", "2", "3"}                                 |

---

### TC-R6-006

| Field                | Detail                                                           |
|----------------------|------------------------------------------------------------------|
| **Title**            | Stolen member can be further stolen from incomplete team         |
| **Priority**         | High                                                             |
| **Preconditions**    | Team "a": {"", "1", ""} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", ""}               |
|                      | 2. Press "Add team"                                              |
|                      | 3. Enter team name "c" with members {"3", "1", "4"}              |
|                      | 4. Press "Add team"                                              |
| **Expected message** | new team inserted                                                |
| **Expected result**  | "a" deleted  "b": {"1", "2", ""}  "c": {"3", "1", "4"}           |

---

### TC-R6-007

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Stolen member deleted then re-added to same team                  |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"1", "", "3"} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"1", "2", ""}                |
|                      | 2. Press "Add team"                                               |
|                      | 3. Enter team name "b" with members {"1", "2", "4"}               |
|                      | 4. Press "Add team"                                               |
| **Expected message** | new team inserted                                                 |
| **Expected result**  | "a" deleted  "b": {"1", "2", ""}  "c": {"3", "1", "4"}            |

---

### TC-R6-008

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Attempt to steal member already in a complete team                |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"", "2", "3"} exists, team "b": {"4", "5", "3"} exists |
| **Steps**            | 1. Enter team name "a" with members {"3", "2", ""}                |
|                      | 2. Press "Add team"                                               |
| **Expected message** | all team members should be unique                                 |
| **Expected result**  | "a": {"", "2", ""}  "b": {"4", "5", "3"}                          |

---

### TC-R6-009

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Modify non-stolen member in incomplete team                       |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"", "2", "3"} exists, team "b": {"4", "2", "5"} exists |
| **Steps**            | 1. Enter team name "a" with members {"", "6", "3"}                |
|                      | 2. Press "Add team"                                               |
| **Expected message** | team modified                                                     |
| **Expected result**  | "a": {"", "6", "3"}  "b": {"4", "2", "5"}                         |

---

### TC-R6-010

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Modify non-stolen member in incomplete team (second case)         |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"1", "2", ""} exists, team "b": {"3", "2", "4"} exists |
| **Steps**            | 1. Enter team name "a" with members {"1", "5", ""}                |
|                      | 2. Press "Add team"                                               |
| **Expected message** | team modified                                                     |
| **Expected result**  | "a": {"1", "5", ""}  "b": {"3", "2", "4"}                         |

---

### TC-R6-011

| Field                | Detail                                                            |
|----------------------|-------------------------------------------------------------------|
| **Title**            | Delete stolen member then add new member to same team             |
| **Priority**         | High                                                              |
| **Preconditions**    | Team "a": {"1", "2", ""} exists, team "b": {"1", "2", "3"} exists |
| **Steps**            | 1. Enter team name "b" with members {"", "2", "3"}                |
|                      | 2. Press "Add team"                                               |
|                      | 3. Enter team name "b" with members {"4", "2", "3"}               |
|                      | 4. Press "Add team"                                               |
| **Expected message** | team modified                                                     |
| **Expected result**  | "a" deleted  "b": {"4", "2", "3"}                                 |

