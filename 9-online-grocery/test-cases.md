# Test Cases — Online grocery 

**Module:** online-grocery  
**Tester:** Alexandr Gusev  
**Total Cases:** 18  
**Version:** 2.0

---

## Summary Tables

| Case      | Steps                                                                                       | Price to pay | Expected result                 |
|-----------|---------------------------------------------------------------------------------------------|--------------|---------------------------------|
| TC-OG-001 | 1. Price 999<br>2. Buy it                                                                   | 999          | Discount 0%<br>Total spend 999  |
| TC-OG-002 | 1. Price 1000<br>2. Buy it                                                                  | 1000         | Discount 5%<br>Total spend 1000 |
| TC-OG-003 | 1. Price 1001<br>2. Buy it                                                                  | 1001         | Discount 5%<br>Total spend 1001 |
| TC-OG-004 | 1. Price 1000<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 0    |
| TC-OG-005 | 1. Price 1000<br>2. Buy it<br>3. Price 1000<br>4. Use discount<br>5. Buy it                 | 950          | Discount 5%<br>Total spend 1000 |
| TC-OG-006 | 1. Price 1000<br>2. Buy it<br>3. Price 1000<br>4. Use discount<br>5. Buy it<br>6. Next year | 0            | Discount 0%<br>Total spend 0    |
| TC-OG-007 | 1. Price 1000<br>2. Buy it<br>3. Price 100<br>4. Buy it                                     | 100          | Discount 5%<br>Total spend 1200 |
| TC-OG-008 | 1. Price 1999<br>2. Buy it                                                                  | 1999         | Discount 5%<br>Total spend 1999 |
| TC-OG-009 | 1. Price 2000<br>2. Buy it                                                                  | 2000         | Discount 8%<br>Total spend 2000 |
| TC-OG-010 | 1. Price 2001<br>2. Buy it                                                                  | 2001         | Discount 8%<br>Total spend 2001 |
| TC-OG-011 | 1. Price 1999<br>2. Buy it<br>3. Price 500<br>4. Use discount<br>5. Buy it                  | 475          | Discount 8%<br>Total spend 1999 |
| TC-OG-012 | 1. Price 2000<br>2. Buy it<br>3. Price 1000<br>4. Use discount<br>5. Buy it                 | 920          | Discount 8%<br>Total spend 2920 |
| TC-OG-013 | 1. Price 2500<br>2. Buy it<br>3. Price 100<br>4. Use discount<br>5. Buy it                  | 92           | Discount 8%<br>Total spend 2592 |
| TC-OG-014 | 1. Price 2999<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 0    |
| TC-OG-015 | 1. Price 3000<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 750  |
| TC-OG-016 | 1. Price 3500<br>2. Buy it<br>3. Next year                                                  | 0            | Discount 0%<br>Total spend 875  |
| TC-OG-017 | 1. Price 3000<br>2. Buy it<br>3. Next year<br>4. Price 250<br>5. Buy it                     | 250          | Discount 5%<br>Total spend 1000 |
| TC-OG-018 | 1. Price abc<br>2. Buy it                                                                   | NaN          | Discount 0%<br>Total spend 0    |

---

## Detailed Test Cases
### TC-OG-001

| Field               | Detail                                |
|---------------------|---------------------------------------|
| **Title**           | Purchase below 1000 EUR – no discount |
| **Priority**        | High                                  |
| **Steps**           | 1. Price 999<br>2. Buy it             |
| **Price to pay**    | 999                                   |
| **Expected result** | Discount 0%<br>Total spend 999        |

---

### TC-OG-002

| Field               | Detail                                                    |
|---------------------|-----------------------------------------------------------|
| **Title**           | Purchase exactly 1000 EUR – 5% discount threshold reached |
| **Priority**        | Critical                                                  |
| **Steps**           | 1. Price 1000<br>2. Buy it                                |
| **Price to pay**    | 1000                                                      |
| **Expected result** | Discount 5%<br>Total spend 1000                           |

---

### TC-OG-003

| Field               | Detail                                     |
|---------------------|--------------------------------------------|
| **Title**           | Purchase just above 1000 EUR – 5% discount |
| **Priority**        | High                                       |
| **Steps**           | 1. Price 1001<br>2. Buy it                 |
| **Price to pay**    | 1001                                       |
| **Expected result** | Discount 5%<br>Total spend 1001            |

---

### TC-OG-004

| Field               | Detail                                       |
|---------------------|----------------------------------------------|
| **Title**           | Total spend resets in the next calendar year |
| **Priority**        | High                                         |
| **Steps**           | 1. Price 1000<br>2. Buy it<br>3. Next year   |
| **Price to pay**    | 0                                            |
| **Expected result** | Discount 0%<br>Total spend 0                 |

---

### TC-OG-005

| Field               | Detail                                                                      |
|---------------------|-----------------------------------------------------------------------------|
| **Title**           | R2 – claimed discount excludes current amount from total spend              |
| **Priority**        | Critical                                                                    |
| **Steps**           | 1. Price 1000<br>2. Buy it<br>3. Price 1000<br>4. Use discount<br>5. Buy it |
| **Price to pay**    | 950                                                                         |
| **Expected result** | Discount 5%<br>Total spend 1000                                             |

---

### TC-OG-006

| Field               | Detail                                                                                      |
|---------------------|---------------------------------------------------------------------------------------------|
| **Title**           | Discounted purchase does not carry over to next year                                        |
| **Priority**        | High                                                                                        |
| **Steps**           | 1. Price 1000<br>2. Buy it<br>3. Price 1000<br>4. Use discount<br>5. Buy it<br>6. Next year |
| **Price to pay**    | 0                                                                                           |
| **Expected result** | Discount 0%<br>Total spend 0                                                                |

---

### TC-OG-007

| Field               | Detail                                                  |
|---------------------|---------------------------------------------------------|
| **Title**           | R3 – double amount added when discount is not claimed   |
| **Priority**        | Critical                                                |
| **Steps**           | 1. Price 1000<br>2. Buy it<br>3. Price 100<br>4. Buy it |
| **Price to pay**    | 100                                                     |
| **Expected result** | Discount 5%<br>Total spend 1200                         |

---

### TC-OG-008

| Field               | Detail                                                   |
|---------------------|----------------------------------------------------------|
| **Title**           | Purchase just below 2000 EUR – 8% discount not triggered |
| **Priority**        | High                                                     |
| **Steps**           | 1. Price 1999<br>2. Buy it                               |
| **Price to pay**    | 1999                                                     |
| **Expected result** | Discount 5%<br>Total spend 1999                          |

---

### TC-OG-009

| Field               | Detail                                                    |
|---------------------|-----------------------------------------------------------|
| **Title**           | Purchase exactly 2000 EUR – 8% discount threshold reached |
| **Priority**        | Critical                                                  |
| **Steps**           | 1. Price 2000<br>2. Buy it                                |
| **Price to pay**    | 2000                                                      |
| **Expected result** | Discount 8%<br>Total spend 2000                           |

---

### TC-OG-010

| Field               | Detail                                     |
|---------------------|--------------------------------------------|
| **Title**           | Purchase just above 2000 EUR – 8% discount |
| **Priority**        | High                                       |
| **Steps**           | 1. Price 2001<br>2. Buy it                 |
| **Price to pay**    | 2001                                       |
| **Expected result** | Discount 8%<br>Total spend 2001            |

---

### TC-OG-011

| Field               | Detail                                                                     |
|---------------------|----------------------------------------------------------------------------|
| **Title**           | R4 – 8% discount claimed, current amount excluded from total spend         |
| **Priority**        | Critical                                                                   |
| **Steps**           | 1. Price 1999<br>2. Buy it<br>3. Price 500<br>4. Use discount<br>5. Buy it |
| **Price to pay**    | 475                                                                        |
| **Expected result** | Discount 8%<br>Total spend 1999                                            |

---

### TC-OG-012

| Field               | Detail                                                                      |
|---------------------|-----------------------------------------------------------------------------|
| **Title**           | R4 – 8% discount claimed, current amount added to total spend               |
| **Priority**        | Critical                                                                    |
| **Steps**           | 1. Price 2000<br>2. Buy it<br>3. Price 1000<br>4. Use discount<br>5. Buy it |
| **Price to pay**    | 920                                                                         |
| **Expected result** | Discount 8%<br>Total spend 2920                                             |

---

### TC-OG-013

| Field               | Detail                                                                     |
|---------------------|----------------------------------------------------------------------------|
| **Title**           | R4 – 8% discount with total spend crossing 2000 threshold                  |
| **Priority**        | High                                                                       |
| **Steps**           | 1. Price 2500<br>2. Buy it<br>3. Price 100<br>4. Use discount<br>5. Buy it |
| **Price to pay**    | 92                                                                         |
| **Expected result** | Discount 8%<br>Total spend 2592                                            |

---

### TC-OG-014

| Field               | Detail                                                    |
|---------------------|-----------------------------------------------------------|
| **Title**           | Purchase just below 3000 EUR – no carry-over to next year |
| **Priority**        | High                                                      |
| **Steps**           | 1. Price 2999<br>2. Buy it<br>3. Next year                |
| **Price to pay**    | 0                                                         |
| **Expected result** | Discount 0%<br>Total spend 0                              |

---

### TC-OG-015

| Field               | Detail                                                   |
|---------------------|----------------------------------------------------------|
| **Title**           | R5 – total spend 3000 EUR, 25% carried over to next year |
| **Priority**        | Critical                                                 |
| **Steps**           | 1. Price 3000<br>2. Buy it<br>3. Next year               |
| **Price to pay**    | 0                                                        |
| **Expected result** | Discount 0%<br>Total spend 750                           |

---

### TC-OG-016

| Field               | Detail                                                         |
|---------------------|----------------------------------------------------------------|
| **Title**           | R5 – total spend above 3000 EUR, 25% carried over to next year |
| **Priority**        | High                                                           |
| **Steps**           | 1. Price 3500<br>2. Buy it<br>3. Next year                     |
| **Price to pay**    | 0                                                              |
| **Expected result** | Discount 0%<br>Total spend 875                                 |

---

### TC-OG-017

| Field               | Detail                                                                  |
|---------------------|-------------------------------------------------------------------------|
| **Title**           | R5 – 25% carry-over plus new purchase reaches 5% discount threshold     |
| **Priority**        | Critical                                                                |
| **Steps**           | 1. Price 3000<br>2. Buy it<br>3. Next year<br>4. Price 250<br>5. Buy it |
| **Price to pay**    | 250                                                                     |
| **Expected result** | Discount 5%<br>Total spend 1000                                         | 

---

### TC-OG-018

| Field               | Detail                                                 |
|---------------------|--------------------------------------------------------|
| **Title**           | Invalid price input ("abc") – no purchase, no discount |
| **Priority**        | High                                                   |
| **Steps**           | 1. Price abc<br>2. Buy it                              |
| **Price to pay**    | NaN                                                    |
| **Expected result** | Discount 0%<br>Total spend 0                           |
