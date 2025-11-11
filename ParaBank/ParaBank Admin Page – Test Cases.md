# ParaBank Admin Page – Test Cases

This document includes detailed **manual test cases** for validating the functionality, configuration, and performance of the [ParaBank Admin Page](https://parabank.parasoft.com/parabank/admin.htm).  
The tests are focused on ensuring that administrative features such as service configuration, loan provider setup, SOAP settings, and user interface elements work as expected.

---

## Test Case Table

| Sl. No. | DATE | Application | Test Case ID | Test Case Name | Module / Feature | Test Step No. | Step Description | Keyword (Action) | Test Object / Element | Input Data | Expected Result | Actual Result | Status (Pass/Fail) | Comments / Notes | Elapsed Time |
|----------|------|--------------|---------------|----------------|------------------|----------------|------------------|------------------|------------------------|-------------|-----------------|----------------|--------------------|------------------|---------------|
| 1 | 11-Nov-2025 | ParaBank | TC_ADMIN_001 | Verify Admin Page Accessibility | Admin Page | 1 | Open the Admin URL in a browser | Open URL | https://parabank.parasoft.com/parabank/admin.htm | N/A | Admin page loads successfully |  |  | Page loads without delay | 00:15 |
| 2 | 11-Nov-2025 | ParaBank | TC_ADMIN_002 | Validate Page Title | UI Validation | 1 | Check the browser title text | Verify Title | Browser Tab | N/A | Title should display “ParaBank | Administration” |  |  | Title consistent with branding | 00:10 |
| 3 | 11-Nov-2025 | ParaBank | TC_ADMIN_003 | Verify “SOAP Service” Label | UI Elements | 1 | Verify presence of SOAP service label | Verify Text | SOAP Service Label | N/A | SOAP Service label visible |  |  | UI label properly aligned | 00:10 |
| 4 | 11-Nov-2025 | ParaBank | TC_ADMIN_004 | Validate “SOAP Service URL” Field | Input Validation | 1 | Verify input field accepts URL | Enter Data | SOAP Service URL Field | https://testapi.parabank.com | URL accepted |  |  | Input box accepts full URL | 00:12 |
| 5 | 11-Nov-2025 | ParaBank | TC_ADMIN_005 | Check Empty Field Behavior | Negative Test | 1 | Leave SOAP field empty and submit | Click Save | SOAP Service URL Field | Blank | Validation or save allowed |  |  | Should show warning or default behavior | 00:18 |
| 6 | 11-Nov-2025 | ParaBank | TC_ADMIN_006 | Validate Loan Provider Dropdown | Dropdown Functionality | 1 | Check dropdown values | Select Option | Loan Provider Dropdown | Available Options | Dropdown lists all providers |  |  | All loan providers listed correctly | 00:14 |
| 7 | 11-Nov-2025 | ParaBank | TC_ADMIN_007 | Verify Update Loan Provider Option | Loan Configuration | 1 | Select and update provider | Click Save | Provider Dropdown | LoanProvider1 | Provider updated successfully |  |  | Provider saves without delay | 00:25 |
| 8 | 11-Nov-2025 | ParaBank | TC_ADMIN_008 | Validate JMS Service Field | Input Validation | 1 | Enter JMS service details | Enter Data | JMS URL Field | jms://localhost:8080 | URL accepted and validated |  |  | Input should be sanitized | 00:20 |
| 9 | 11-Nov-2025 | ParaBank | TC_ADMIN_009 | Verify Empty JMS Field | Negative Testing | 1 | Leave JMS field blank | Click Save | JMS URL Field | Blank | Should show warning message |  |  | Should not allow empty JMS | 00:15 |
| 10 | 11-Nov-2025 | ParaBank | TC_ADMIN_010 | Validate Access Point Field | Field Testing | 1 | Enter access point value | Enter Data | Access Point Input | /parabank/api | Value saved correctly |  |  | Data persisted on reload | 00:20 |
| 11 | 11-Nov-2025 | ParaBank | TC_ADMIN_011 | Check Save Button Functionality | Button Validation | 1 | Click Save button after entry | Click Button | Save Button | Valid Input | Configuration saved |  |  | Confirmation message shown | 00:22 |
| 12 | 11-Nov-2025 | ParaBank | TC_ADMIN_012 | Check Reset Button | Button Testing | 1 | Enter data and click Reset | Click Reset | Reset Button | Sample Data | Fields cleared |  |  | Reset clears all fields | 00:14 |
| 13 | 11-Nov-2025 | ParaBank | TC_ADMIN_013 | Verify Success Confirmation Message | Message Validation | 1 | Save data and check success | Click Save | Save Button | Valid Data | Confirmation message “Settings saved successfully” |  |  | Message in green text | 00:17 |
| 14 | 11-Nov-2025 | ParaBank | TC_ADMIN_014 | Verify Error Message on Invalid URL | Negative Testing | 1 | Enter invalid URL and save | Click Save | SOAP Service Field | invalidurl | Show error message |  |  | Proper validation enforced | 00:18 |
| 15 | 11-Nov-2025 | ParaBank | TC_ADMIN_015 | Check Loan Provider Default Value | Dropdown Testing | 1 | Load page and check selected provider | Verify Default | Loan Provider Dropdown | N/A | Default provider visible |  |  | Default provider preselected | 00:10 |
| 16 | 11-Nov-2025 | ParaBank | TC_ADMIN_016 | Verify Loan Provider Update Persistence | Persistence Testing | 1 | Change provider and refresh page | Refresh Page | Loan Provider Dropdown | New Provider | Provider remains updated |  |  | Data saved persistently | 00:25 |
| 17 | 11-Nov-2025 | ParaBank | TC_ADMIN_017 | Check Admin Page Responsiveness | UI Testing | 1 | Resize browser | Resize Window | Page Container | N/A | Layout remains responsive |  |  | UI adjusts without overlap | 00:28 |
| 18 | 11-Nov-2025 | ParaBank | TC_ADMIN_018 | Verify Label Alignment | UI Validation | 1 | Check label alignment | Visual Check | Labels | N/A | All labels left-aligned properly |  |  | UI consistency verified | 00:12 |
| 19 | 11-Nov-2025 | ParaBank | TC_ADMIN_019 | Verify Mandatory Fields | Field Validation | 1 | Attempt to save without required data | Click Save | Fields | N/A | Error shown for missing values |  |  | Mandatory validations correct | 00:19 |
| 20 | 11-Nov-2025 | ParaBank | TC_ADMIN_020 | Validate Browser Compatibility | Compatibility Testing | 1 | Open admin page in Chrome, Firefox, Edge | Open URL | All Browsers | N/A | Admin page loads in all browsers |  |  | UI consistent | 00:45 |
| 21 | 11-Nov-2025 | ParaBank | TC_ADMIN_021 | Check SOAP Service Response Time | Performance | 1 | Measure response post update | Save and Load | SOAP Field | Valid URL | Response time < 2s |  |  | Within SLA | 00:40 |
| 22 | 11-Nov-2025 | ParaBank | TC_ADMIN_022 | Validate Form Load Speed | Performance | 1 | Measure page load | Open Page | Admin URL | N/A | Loads within 3 seconds |  |  | Optimal load speed | 00:25 |
| 23 | 11-Nov-2025 | ParaBank | TC_ADMIN_023 | Check Session Persistence | Security | 1 | Logout and revisit URL | Login Again | Admin Page | N/A | Requires re-login |  |  | Session management secure | 00:33 |
| 24 | 11-Nov-2025 | ParaBank | TC_ADMIN_024 | Check Field Length Constraints | Input Validation | 1 | Enter long strings | Enter Text | SOAP URL Field | 300 chars | Accept only valid length |  |  | Field restricts input | 00:20 |
| 25 | 11-Nov-2025 | ParaBank | TC_ADMIN_025 | Validate Tab Order | Accessibility | 1 | Navigate using Tab key | Keyboard Navigation | Input Fields | N/A | Cursor follows correct order |  |  | Accessibility valid | 00:14 |
| 26 | 11-Nov-2025 | ParaBank | TC_ADMIN_026 | Verify Font and Style Consistency | UI | 1 | Inspect all text fonts | Visual Check | Labels | N/A | Fonts consistent across fields |  |  | No visual mismatch | 00:16 |
| 27 | 11-Nov-2025 | ParaBank | TC_ADMIN_027 | Check Service URL Placeholder Text | UI Validation | 1 | Inspect input field placeholders | Verify Placeholder | SOAP Service URL | N/A | Shows “Enter service URL” |  |  | Help text visible | 00:13 |
| 28 | 11-Nov-2025 | ParaBank | TC_ADMIN_028 | Validate Save Action Without Change | Logic Validation | 1 | Click Save without any modification | Click Save | Save Button | N/A | Should not overwrite existing data |  |  | No redundant save | 00:20 |
| 29 | 11-Nov-2025 | ParaBank | TC_ADMIN_029 | Verify Footer Copyright | UI Testing | 1 | Scroll to bottom | Verify Text | Footer | N/A | Displays ParaBank copyright |  |  | Text visible and correct | 00:08 |
| 30 | 11-Nov-2025 | ParaBank | TC_ADMIN_030 | Verify Admin Page Link from Homepage | Navigation | 1 | Click Admin link from home | Click Link | Admin Page | N/A | Opens admin page successfully |  |  | Navigation works as expected | 00:12 |

---

## Notes and Observations

1. **Performance Considerations:**  
   - Admin page loads slower during initial access; caching improves subsequent loads.  
   - Save operation delay observed when multiple configurations are updated together.  

2. **Security Findings:**  
   - URL accessible without authentication if bookmarked (needs access control).  
   - Sensitive configuration fields should ideally mask credentials.  

3. **UI/UX Issues:**  
   - Some labels misaligned on smaller screens (<1024px).  
   - Placeholder text missing for a few input fields (e.g., JMS URL).  

4. **Positive Highlights:**  
   - Clean form layout, intuitive save and reset controls.  
   - Confirmation messages clearly indicate success or failure.  

5. **Recommendations:**  
   - Add mandatory field validation on form submit.  
   - Display loader during Save action to indicate process in progress.  
   - Restrict access via session-based authentication.  

---

### Documentation Summary

**Module:** Admin Configuration  
**Test Coverage:** Functional, UI, Security, and Performance  
**Total Test Cases:** 30  
**Execution Platform:** Chrome (v119), Edge (v126), Firefox (v122)  
**Tester:** Mohammed Saqib  
**Execution Date:** 11-Nov-2025  

---

### Final Notes
This suite ensures comprehensive coverage of the ParaBank Admin module.  
All cases follow a consistent format that aligns with standard manual QA documentation templates used in the repository.
