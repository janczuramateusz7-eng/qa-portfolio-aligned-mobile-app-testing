
# Test Case Template

## Test Case Title

`[Project][Platform] Short test case title`

Example:

`[Aligned][Android] User cannot continue without selecting required answer`

---

## Objective

Describe what this test case verifies.

Example:

Verify that the user cannot continue to the next quiz screen without selecting a required answer.

---

## Preconditions

- User has access to the application.
- User is on the correct screen or flow.
- Required test data is available.
- User is in the correct state, for example logged in, logged out, or after email verification.

---

## Environment

| Area | Details |
|---|---|
| Application |  |
| Platform | Mobile App / Mobile Web / Web |
| Device |  |
| OS |  |
| Browser / App version |  |
| Environment | Test / Staging / Production |

---

## Test Data

| Field | Value |
|---|---|
| Email |  |
| Password |  |
| Name |  |
| Selected answer |  |
| Other data |  |

---

## Steps

| Step | Action | Data | Expected Result |
|---|---|---|---|
| 1 | Open the application | N/A | Application is opened successfully |
| 2 | Navigate to the tested screen or flow | N/A | Correct screen or flow is displayed |
| 3 | Enter or select test data | Test data | Data is entered or selected correctly |
| 4 | Tap the main action button | N/A | System processes the action |
| 5 | Observe the result | N/A | Actual behavior can be compared with expected result |

---

## Expected Result

Describe the final expected result of the test case.

Example:

User should not be able to continue without selecting a required answer.  
A clear validation message should be displayed or the Continue button should remain disabled.  
User should stay on the same quiz screen.

---

## Notes

Add any additional information if needed.

Example:

This test case should be executed on Android as part of mobile app testing.
