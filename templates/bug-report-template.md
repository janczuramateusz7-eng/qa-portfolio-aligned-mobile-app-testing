
# Bug Report Template

## Summary

`[Project][Platform] Short bug summary`

Example:

`[Aligned][Android] Name field accepts invalid characters during quiz flow`

---

## Description

Describe what happened and why it is a problem.

Example:

During the quiz flow on Android, the user enters invalid characters in the name field and tries to continue.

The app accepts the entered value and allows the user to proceed, even though the name field should validate invalid characters.

---

## Environment

| Area | Details |
|---|---|
| Environment | Test / Staging / Production |
| Application |  |
| Platform | Mobile App / Mobile Web / Web |
| Device |  |
| OS |  |
| Browser / App version |  |
| Area |  |

---

## Preconditions

- User is on the correct screen or flow.
- User has required test data.
- User is in the correct state, for example logged in, logged out, or after email verification.

---

## Steps to reproduce

1. Open the application.
2. Navigate to the tested screen or flow.
3. Enter or select required test data.
4. Perform the tested action.
5. Observe the result.

---

## Expected result

Describe what should happen.

Example:

User should not be able to continue with invalid input.  
A clear validation message should be displayed near the affected field.  
User should stay on the current screen and be able to correct the data.

---

## Actual result

Describe what actually happens.

Example:

User can continue after entering invalid input.  
No validation message is displayed.  
The app accepts data that should be rejected according to the test case.

---

## Severity

Low / Medium / High / Critical

Example:

`Severity: Medium`

---

## Priority

Low / Medium / High / Critical

Example:

`Priority: Medium`

---

## Attachments

Add screenshots or screen recordings if available.

Before adding attachments to a public portfolio, remove or hide:

- email addresses,
- account data,
- private Jira links,
- internal comments,
- sensitive test data,
- personal information.

---

## Notes

Add any additional information that may help reproduce or understand the issue.

Example:

Issue reproduced on Android during manual test execution.
