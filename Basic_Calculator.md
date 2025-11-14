# Basic Calculator Testing – TestSheepNZ

## Page Under Test  
**Basic Calculator – TestSheepNZ**  
URL: [https://testsheepnz.github.io/BasicCalculator.html](https://testsheepnz.github.io/BasicCalculator.html) 

---

## Objective  
To validate the functionality of the basic calculator including arithmetic operations (add, subtract, multiply, divide), string concatenation mode, integer mode toggle, input validation, and UI behaviour.

| Sl. No. | DATE       | Application        | Test Case ID | Test Case Name                     | Module / Feature | Test Step No. | Step Description            | Keyword | Test Object / Element | Input Data      | Expected Result | Actual Result | Status | Notes                   | Time |
|---------|------------|--------------------|---------------|-------------------------------------|-------------------|----------------|------------------------------|---------|------------------------|------------------|------------------|---------------|--------|-------------------------|------|
| 1       | 2025-02-14 | Basic Calculator   | TC_ADD_01     | Add two positive integers           | Addition          | 1              | Enter 5 and 3               | Type    | Number Fields         | 5,3              | 8                |               |        |                         |      |
| 2       | 2025-02-14 | Basic Calculator   | TC_ADD_02     | Add two negative values             | Addition          | 1              | Enter -5 and -7             | Type    | Fields                | -5,-7            | -12              |               |        |                         |      |
| 3       | 2025-02-14 | Basic Calculator   | TC_ADD_03     | Add positive + negative             | Addition          | 1              | Enter 12 and -4             | Type    | Fields                | 12,-4            | 8                |               |        |                         |      |
| 4       | 2025-02-14 | Basic Calculator   | TC_ADD_04     | Add with zero                       | Addition          | 1              | Enter 0 and 8               | Type    | Fields                | 0,8              | 8                |               |        |                         |      |
| 5       | 2025-02-14 | Basic Calculator   | TC_ADD_05     | Large value addition                | Addition          | 1              | Enter 999999 + 999999       | Type    | Fields                | 999999,999999    | 1999998          |               |        | Performance check       |      |
| 6       | 2025-02-14 | Basic Calculator   | TC_ADD_06     | Add decimal numbers                 | Addition          | 1              | Enter 3.5 + 2.1             | Type    | Fields                | 3.5,2.1          | 5.6              |               |        | If decimals allowed     |      |
| 7       | 2025-02-14 | Basic Calculator   | TC_ADD_07     | Add very small decimals             | Addition          | 1              | Enter 0.0003 + 0.0004       | Type    | Fields                | 0.0003,0.0004    | 0.0007           |               |        | Precision test          |      |
| 8       | 2025-02-14 | Basic Calculator   | TC_ADD_08     | Add long decimal values             | Addition          | 1              | Enter 1.123456 + 2.654321   | Type    | Fields                | 1.123456,2.654321| 3.777777         |               |        | Floating point accuracy |      |
| 9       | 2025-02-14 | Basic Calculator   | TC_ADD_09     | Add extremely large integers        | Addition          | 1              | Enter 99999999 + 99999999   | Type    | Fields                | 99M,99M          | 199999998        |               |        | Boundary test           |      |
| 10      | 2025-02-14 | Basic Calculator   | TC_ADD_10     | Add blank input (first missing)     | Validation        | 1              | Leave first field empty     | Type    | Field                 | "",5              | Error message     |               | Fail   | Missing validation       |      |
| 11      | 2025-02-14 | Basic Calculator   | TC_ADD_11     | Add blank input (second missing)    | Validation        | 1              | Leave second field empty    | Type    | Field                 | 5,""              | Error message     |               | Fail   | Missing validation       |      |
| 12      | 2025-02-14 | Basic Calculator   | TC_ADD_12     | Add unsupported characters          | Validation        | 1              | Enter ABC + 5               | Type    | Fields                | ABC,5            | Error message     |               | Fail   | Needs input filtering   |      |

---

## Notes & Explanations  
- This page offers **basic arithmetic operations** plus a **concatenation mode** where inputs are treated as strings.  
- The “Integers only” toggle limits results to integer outputs when enabled.  
- Input validation is essential — non-numeric input in numeric modes must be handled safely.  
- UI behaviour under mode switching, viewport resizing, keyboard navigation, and large value operations should all be verified.

---

## End Notes  
Though simple in appearance, the Basic Calculator application introduces various functional and non-functional test concerns: numeric vs string mode, error conditions (like division by zero or invalid input), UI responsiveness, mode toggles, and accessibility.  
Covering these scenarios helps ensure reliability, correct handling of edge-cases, and a solid user experience.

**File Name:** `basic_calculator_testing.md`  
**Category:** Web UI – Basic Calculator  
**Purpose:** Manual + Automation test documentation  
