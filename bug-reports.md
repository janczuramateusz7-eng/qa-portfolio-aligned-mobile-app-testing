# Bug Reports — Aligned Mobile App

## Overview

This file contains example bug reports created during manual testing of the **Aligned mobile app** on Android.

The reported issues were found during test execution of the quiz flow.

Each bug report includes:

* summary,
* description,
* environment,
* preconditions,
* steps to reproduce,
* expected result,
* actual result,
* severity,
* priority.

---

# Bug 1: Name field accepts invalid characters during quiz flow

## Summary

`[Aligned][Android] Name field accepts invalid characters during quiz flow`

## Severity

Medium

## Priority

Medium

## Description

During the quiz flow on Android, the user enters invalid characters in the name field and tries to continue.

The app accepts the entered value and allows the user to proceed, even though the name field should validate invalid characters.

## Environment

| Area        | Details                 |
| ----------- | ----------------------- |
| Environment | Test                    |
| Application | Aligned                 |
| Platform    | Mobile App              |
| Device      | Android                 |
| Area        | Quiz flow / Name screen |

## Preconditions

* User is logged in or has completed email verification.
* User is in the Aligned quiz flow.
* User is on the “What is your name?” screen.

## Steps to reproduce

1. Open Aligned app on Android.
2. Complete email verification if required.
3. Continue through the quiz flow until the “What is your name?” screen is displayed.
4. Tap the name input field.
5. Enter a name with invalid characters, for example: `Mark123!@#`.
6. Tap the **Continue** button.
7. Observe the result.

## Expected result

User should not be able to continue with a name that contains invalid characters.

A clear validation message should be displayed near the name field, informing the user that the entered name is not valid.

User should stay on the “What is your name?” screen and be able to correct the name.

## Actual result

User can continue after entering a name with invalid characters.

No validation message is displayed near the name field.

The app accepts invalid characters in the name field during the quiz flow.

---

# Bug 2: Life area option icons and labels are not displayed correctly in quiz flow

## Summary

`[Aligned][Android] Life area option icons and labels are not displayed correctly in quiz flow`

## Severity

Medium

## Priority

Medium

## Description

During the quiz flow on Android, the user reaches the life areas selection screen.

Some life area option icons and labels are not displayed correctly, which may make it difficult for the user to understand or select the correct option.

## Environment

| Area        | Details                       |
| ----------- | ----------------------------- |
| Environment | Test                          |
| Application | Aligned                       |
| Platform    | Mobile App                    |
| Device      | Android                       |
| Area        | Quiz flow / Life areas screen |

## Preconditions

* User is logged in or has completed email verification.
* User is in the Aligned quiz flow.
* User has continued through the quiz until the life areas selection screen is displayed.

## Steps to reproduce

1. Open Aligned app on Android.
2. Complete email verification if required.
3. Continue through the quiz flow until the “What life areas would you like to improve?” screen is displayed.
4. Observe the life area options.
5. Check icons and labels for available options, such as Health, Career, Finances, Growth, Relationships, Family, Fun and Spirituality.
6. Observe the result.

## Expected result

All life area options should be displayed correctly.

Each option should have a visible icon and a readable label.

Icons and labels should be properly aligned and should not overlap, be cut off, missing or visually broken.

User should be able to clearly understand and select each life area option.

## Actual result

Life area option icons and/or labels are not displayed correctly on the life areas selection screen.

Some icons or labels are missing, cut off, misaligned, overlapping or difficult to read.

This may make it difficult for the user to understand or select the correct life area option.

---

# Bug 3: Quiz answers from one account are preselected for another account

## Summary

`[Aligned][Android] Quiz answers from one account are preselected for another account`

## Severity

High

## Priority

High

## Description

During the quiz flow on Android, answers selected on one account are preselected when using another account.

The second user sees answers that were previously selected by a different account, even though quiz answers should be stored separately for each user account.

## Environment

| Area        | Details                             |
| ----------- | ----------------------------------- |
| Environment | Test                                |
| Application | Aligned                             |
| Platform    | Mobile App                          |
| Device      | Android                             |
| Area        | Quiz flow / Account data separation |

## Preconditions

* User has access to two different test accounts.
* Account A has already started or completed part of the quiz flow.
* Account B is a separate account.

## Steps to reproduce

1. Open Aligned app on Android.
2. Log in or complete email verification using Account A.
3. Go through several quiz questions and select answers.
4. Exit the quiz flow or close the app.
5. Open Aligned app again.
6. Log in or complete email verification using Account B.
7. Navigate to the same quiz questions.
8. Observe the selected answers.

## Expected result

Answers selected by Account A should not be preselected for Account B.

Each account should have its own separate quiz state and quiz answers.

Account B should start with clean quiz answers or only with data saved for Account B.

## Actual result

Answers previously selected by Account A are preselected when using Account B.

The app displays quiz answers from another account.

Quiz state is not properly separated between different user accounts.

---

# Bug 4: Text below life area slider is hidden behind Continue button

## Summary

`[Aligned][Android] Text below life area slider is hidden behind Continue button`

## Severity

Medium

## Priority

Medium

## Description

During the quiz flow on Android, the user selects a life area and is redirected to the rating screen with a slider.

After moving the slider, additional text appears below the slider, but it is not visible because it is covered by the **Continue** button.

As a result, the user cannot read the information displayed below the slider.

## Environment

| Area        | Details                             |
| ----------- | ----------------------------------- |
| Environment | Test                                |
| Application | Aligned                             |
| Platform    | Mobile App                          |
| Device      | Android                             |
| Area        | Quiz flow / Life area rating screen |

## Preconditions

* User is logged in or has completed email verification.
* User is in the Aligned quiz flow.
* User has reached the life areas selection screen.

## Steps to reproduce

1. Open Aligned app on Android.
2. Complete email verification if required.
3. Continue through the quiz flow until the “What life areas would you like to improve?” screen is displayed.
4. Select any life area, for example Health.
5. On the life area rating screen, move the slider.
6. Observe the text displayed below the slider and near the **Continue** button.

## Expected result

Text displayed after moving the slider should be fully visible and readable.

The **Continue** button should not overlap or cover any text or content on the screen.

User should be able to read the slider-related text before continuing.

## Actual result

After moving the slider, text appears below the slider, but it is hidden behind the **Continue** button.

The user cannot fully read the text because it is covered by the button.

The screen layout does not adjust properly after the slider text is displayed.

---

# Bug Summary Table

| Bug Summary                                                                | Severity | Priority |
| -------------------------------------------------------------------------- | -------- | -------- |
| Name field accepts invalid characters during quiz flow                     | Medium   | Medium   |
| Life area option icons and labels are not displayed correctly in quiz flow | Medium   | Medium   |
| Quiz answers from one account are preselected for another account          | High     | High     |
| Text below life area slider is hidden behind Continue button               | Medium   | Medium   |

---

# Notes

These bug reports were created for portfolio purposes based on manual QA work.

The main focus was to demonstrate:

* clear bug reporting,
* reproducible steps,
* expected result vs actual result analysis,
* severity and priority assessment,
* mobile app testing,
* UI/UX issue reporting,
* account state and data separation testing.

