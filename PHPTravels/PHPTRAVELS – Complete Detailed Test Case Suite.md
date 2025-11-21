# PHPTRAVELS – Complete Detailed Test Case Suite

Below is a fully structured, table-formatted suite containing **all modules**, **all flows**, **positive/negative/boundary** scenarios, mapped to your standard format.

---

## 1. General / UI / Navigation Test Cases

| Sl. No. | DATE | Application | Test Case ID | Test Case Name       | Module / Feature | Test Step No. | Step Description            | Keyword  | Test Object / Element | Input Data                                       | Expected Result                | Actual Result | Status | Notes | Elapsed time |
| ------- | ---- | ----------- | ------------ | -------------------- | ---------------- | ------------- | --------------------------- | -------- | --------------------- | ------------------------------------------------ | ------------------------------ | ------------- | ------ | ----- | ------------ |
| 1       |      | PHPTRAVELS  | GM-001       | Homepage load        | General          | 1             | Navigate to homepage        | Open URL | Browser               | [https://phptravels.com](https://phptravels.com) | Homepage loads fully           |               |        |       |              |
| 2       |      | PHPTRAVELS  | GM-002       | Header navigation    | General          | 1             | Click each header menu item | Click    | Header menu           | Flights/Hotels/Tours/Cars                        | Relevant pages load            |               |        |       |              |
| 3       |      | PHPTRAVELS  | GM-003       | Footer links working | General          | 1             | Click footer links          | Click    | Footer                | Terms/Privacy                                    | Pages open without 404         |               |        |       |              |
| 4       |      | PHPTRAVELS  | GM-004       | Responsiveness       | General          | 1             | Resize browser              | Resize   | Browser               | Mobile/Desktop                                   | Page adjusts responsively      |               |        |       |              |
| 5       |      | PHPTRAVELS  | GM-005       | SSL validation       | General          | 1             | Check URL                   | Validate | Browser               | -                                                | HTTPS active, no mixed content |               |        |       |              |

---

## 2. User Registration Test Cases

| Sl. No. | DATE | App        | Test Case ID | Test Case Name               | Module       | Step No. | Step Description               | Action   | Element           | Input Data       | Expected                  | Actual | Status | Notes | Time |
| ------- | ---- | ---------- | ------------ | ---------------------------- | ------------ | -------- | ------------------------------ | -------- | ----------------- | ---------------- | ------------------------- | ------ | ------ | ----- | ---- |
| 1       |      | PHPTRAVELS | UR-001       | Register valid user          | Registration | 1        | Open registration page         | Open URL | Registration link | -                | Page loads                |        |        |       |      |
|         |      |            |              |                              |              | 2        | Enter valid user details       | Input    | Form fields       | Name, email, pwd | Registration success      |        |        |       |      |
| 2       |      | PHPTRAVELS | UR-002       | Register with existing email | Registration | 1        | Open registration page         | Open URL | Registration link | -                | Page loads                |        |        |       |      |
|         |      |            |              |                              |              | 2        | Enter existing email           | Input    | Email field       | Existing email   | Error shown               |        |        |       |      |
| 3       |      | PHPTRAVELS | UR-003       | Invalid email format         | Registration | 1        | Submit invalid email           | Input    | Email field       | user@@domain     | Error: Invalid email      |        |        |       |      |
| 4       |      | PHPTRAVELS | UR-004       | Blank fields                 | Registration | 1        | Click submit with blank fields | Click    | Submit button     | -                | Required validations show |        |        |       |      |

---

## 3. Login Test Cases

| Sl. No. | App        | Test Case ID | Test Case Name     | Module | Step No. | Step Description                | Action   | Element        | Input         | Expected               |
| ------- | ---------- | ------------ | ------------------ | ------ | -------- | ------------------------------- | -------- | -------------- | ------------- | ---------------------- |
| 1       | PHPTRAVELS | LG-001       | Login valid user   | Login  | 1        | Open login page                 | Open URL | Login link     | -             | Page loads             |
|         |            |              |                    |        | 2        | Enter valid credentials         | Input    | Email/pwd      | Correct creds | Login successful       |
| 2       | PHPTRAVELS | LG-002       | Incorrect password | Login  | 1        | Enter wrong password            | Input    | Password field | Wrong pwd     | Error message shown    |
| 3       | PHPTRAVELS | LG-003       | Blank fields       | Login  | 1        | Attempt login with blank fields | Click    | Login button   | Empty         | Field-level validation |

---

## 4. Hotels Module Test Cases

### Search

| Sl. No. | ID     | Test Case          | Step | Description                  | Input              | Expected         |
| ------- | ------ | ------------------ | ---- | ---------------------------- | ------------------ | ---------------- |
| 1       | HT-001 | Valid hotel search | 1    | Enter location + valid dates | Dubai, valid dates | Results load     |
| 2       | HT-002 | Invalid date range | 1    | Checkout < Checkin           | 10 Dec < 05 Dec    | Validation error |
| 3       | HT-003 | Blank search       | 1    | Click search without input   | Empty              | Required message |

### Booking

| Sl. No. | ID | Name | Step | Description | Input | Expected |
| 4 | HT-004 | Select hotel | 1 | Click result item | Select first result | Hotel details load |
| 5 | HT-005 | Book valid | 1 | Click Book | Guest details | Booking successful + email |
| 6 | HT-006 | Payment failure | 1 | Enter invalid card | Wrong card info | Payment declined |

---

## 5. Flights Module Test Cases

### Search

| Sl. No. | ID | Name | Step | Description | Input | Expected |
| 1 | FL-001 | Valid flight search | 1 | Enter origin/destination/dates | DXB → DEL | Results load |
| 2 | FL-002 | Invalid route | 1 | Origin and destination same | DXB → DXB | Validation |
| 3 | FL-003 | Past date | 1 | Enter past date | Past date | Error |

### Booking

| Sl. No. | ID | Name | Step | Input | Expected |
| 4 | FL-004 | Book flight | 1 | Passenger details + payment | Booking success |
| 5 | FL-005 | Payment failed | 1 | Invalid card | Decline + message |

---

## 6. Tours Test Cases

| Sl. No. | ID     | Name          | Step | Description           | Input           | Expected         |
| ------- | ------ | ------------- | ---- | --------------------- | --------------- | ---------------- |
| 1       | TR-001 | Search tours  | 1    | Enter city/date       | Dubai           | Tours list       |
| 2       | TR-002 | Filter tours  | 1    | Apply category filter | Adventure       | Filtered results |
| 3       | TR-003 | Book tour     | 1    | Valid booking         | Guest + payment | Booking success  |
| 4       | TR-004 | Over-capacity | 1    | Enter > allowed seats | Seats > limit   | Error shown      |

---

## 7. Cars Test Cases

| Sl. No. | ID     | Name         | Step | Description       | Input                 | Expected       |
| ------- | ------ | ------------ | ---- | ----------------- | --------------------- | -------------- |
| 1       | CR-001 | Search cars  | 1    | Enter pickup/drop | Dubai, valid times    | Car list loads |
| 2       | CR-002 | Invalid time | 1    | Return < Pickup   | Wrong times           | Error          |
| 3       | CR-003 | Book car     | 1    | Valid booking     | Driver info + payment | Success        |

---

## 8. Admin Module Test Cases

| Sl. No. | ID     | Name            | Step | Description     | Input        | Expected             |
| ------- | ------ | --------------- | ---- | --------------- | ------------ | -------------------- |
| 1       | AD-001 | Admin login     | 1    | Valid login     | Admin creds  | Dashboard loads      |
| 2       | AD-002 | Manage hotels   | 1    | Add/edit/delete | Hotel fields | CRUD success         |
| 3       | AD-003 | Manage users    | 1    | Change roles    | User role    | Updated successfully |
| 4       | AD-004 | Manage bookings | 1    | Approve/reject  | Booking ref  | Status updated       |

---

## 9. Payment Gateway Test Cases

| Sl. No. | ID     | Name          | Step | Input      | Expected          |
| ------- | ------ | ------------- | ---- | ---------- | ----------------- |
| 1       | PY-001 | Valid payment | 1    | Valid CC   | Payment success   |
| 2       | PY-002 | Invalid card  | 1    | Wrong CC   | Payment failure   |
| 3       | PY-003 | Expired card  | 1    | Old expiry | Error             |
| 4       | PY-004 | Blank fields  | 1    | Empty      | Required warnings |

---

## 10. Security & Negative Test Cases

| Sl. No. | ID     | Name            | Input                     | Expected                 |
| ------- | ------ | --------------- | ------------------------- | ------------------------ |
| 1       | NG-001 | SQL injection   | "' OR 1=1 --" in fields   | Input rejected           |
| 2       | NG-002 | XSS attempt     | <script>alert()           | Sanitized, no script run |
| 3       | NG-003 | Session timeout | Idle session              | Auto logout              |
| 4       | NG-004 | Network failure | Disconnect during payment | Graceful recovery        |

---

## 11. Performance Test Cases

* Measure load time Hotel search
* Stress test multiple users hitting search
* Flight search response time under load
* Check memory usage & browser performance

---

If you want, I can break this into **four separate files**: User Management, Hotels, Flights, Admin, Payments.
