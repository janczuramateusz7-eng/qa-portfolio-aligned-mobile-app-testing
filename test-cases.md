# Test Cases — Aligned Mobile App

## Overview

This file contains example manual test cases created for the **Aligned mobile app**.

The main focus was testing the quiz-based onboarding flow on Android.

Test cases are written in a clear manual QA format:

* **Action** — what the tester does,
* **Data** — what test data is used,
* **Expected Result** — what should happen.

## Environment

| Area                 | Details        |
| -------------------- | -------------- |
| Application          | Aligned        |
| Platform             | Mobile App     |
| Device               | Android        |
| Test Management Tool | Xray           |
| Test Type            | Manual testing |

---

# Test Case 1: User can open quiz flow after email verification

## Objective

Verify that the user can open the quiz flow after successful email verification.

## Preconditions

* User has access to the Aligned app.
* User has a valid test email address.
* User can complete email verification.

## Steps

| Step | Action                      | Data                    | Expected Result                                            |
| ---- | --------------------------- | ----------------------- | ---------------------------------------------------------- |
| 1    | Open Aligned app on Android | N/A                     | App is opened successfully                                 |
| 2    | Enter valid email address   | Valid test email        | Email address is entered correctly                         |
| 3    | Submit email form           | N/A                     | Verification code screen is displayed                      |
| 4    | Enter verification code     | Valid verification code | Code is accepted successfully                              |
| 5    | Verify quiz flow start      | N/A                     | “See your progress and stay motivated” screen is displayed |
| 6    | Verify Continue button      | N/A                     | Continue button is visible and tappable                    |

---

# Test Case 2: User can continue from progress intro screen

## Objective

Verify that the user can continue from the quiz intro screen to the first quiz question.

## Preconditions

* User has completed email verification.
* User is on the intro / progress screen.

## Steps

| Step | Action                     | Data | Expected Result                                            |
| ---- | -------------------------- | ---- | ---------------------------------------------------------- |
| 1    | Verify intro screen        | N/A  | “See your progress and stay motivated” screen is displayed |
| 2    | Verify Continue button     | N/A  | Continue button is visible and tappable                    |
| 3    | Tap Continue button        | N/A  | User is moved to the first quiz question                   |
| 4    | Verify first quiz question | N/A  | First quiz question is displayed correctly                 |

---

# Test Case 3: User can answer single-choice quiz questions

## Objective

Verify that the user can select an answer in single-choice quiz questions and continue to the next screen.

## Dataset example

| Question                                                | Selected Answer               |
| ------------------------------------------------------- | ----------------------------- |
| What do you believe is key to realizing your potential? | Consistency                   |
| How old are you?                                        | 25-34                         |
| What gender do you identify with?                       | Prefer not to say             |
| Does stress affect your mood or productivity?           | Sometimes                     |
| Do you feel anxious about the future?                   | Sometimes                     |
| What motivates you the most on your journey?            | The need for self-improvement |

## Steps

| Step | Action                                                                 | Data                         | Expected Result                                                  |
| ---- | ---------------------------------------------------------------------- | ---------------------------- | ---------------------------------------------------------------- |
| 1    | Continue through quiz flow until a single-choice question is displayed | N/A                          | Single-choice question is displayed                              |
| 2    | Verify question text                                                   | Question from dataset        | Question text is displayed correctly                             |
| 3    | Verify answer options                                                  | N/A                          | Answer options are visible and tappable                          |
| 4    | Select answer option                                                   | Selected Answer from dataset | Selected answer is highlighted or marked as selected             |
| 5    | Tap Continue button                                                    | N/A                          | User is moved to the next quiz screen                            |
| 6    | Verify quiz flow continues                                             | N/A                          | Next question or informational screen is displayed without error |

---

# Test Case 4: User cannot continue without selecting required answer

## Objective

Verify that the user cannot continue from a required single-choice question without selecting an answer.

## Preconditions

* User is in the quiz flow.
* User is on a required single-choice question screen.

## Steps

| Step | Action                                      | Data | Expected Result                                                     |
| ---- | ------------------------------------------- | ---- | ------------------------------------------------------------------- |
| 1    | Open a required single-choice quiz question | N/A  | Question and answer options are displayed                           |
| 2    | Do not select any answer                    | N/A  | No answer option is selected                                        |
| 3    | Tap Continue button                         | N/A  | User is not moved to the next quiz screen                           |
| 4    | Verify validation behavior                  | N/A  | Validation message is displayed or Continue button remains disabled |
| 5    | Verify current screen                       | N/A  | User stays on the same quiz question screen                         |

---

# Test Case 5: User can enter name and see personalized screen

## Objective

Verify that the app displays personalized content after the user enters a valid name.

## Test data

| Field | Value |
| ----- | ----- |
| Name  | Mark  |

## Steps

| Step | Action                                                      | Data | Expected Result                                             |
| ---- | ----------------------------------------------------------- | ---- | ----------------------------------------------------------- |
| 1    | Continue through quiz flow until name question is displayed | N/A  | “What is your name?” screen is displayed                    |
| 2    | Tap name input field                                        | N/A  | Name input field is focused and keyboard is displayed       |
| 3    | Enter valid name                                            | Mark | Name is entered correctly                                   |
| 4    | Tap Continue button                                         | N/A  | User is moved to the next quiz screen                       |
| 5    | Verify personalized screen                                  | Mark | Screen with text “Mark, you are in good hands” is displayed |

---

# Test Case 6: User cannot continue without entering name

## Objective

Verify that the user cannot continue from the name screen without entering a name.

## Preconditions

* User is in the quiz flow.
* User is on the “What is your name?” screen.

## Steps

| Step | Action                        | Data | Expected Result                                                     |
| ---- | ----------------------------- | ---- | ------------------------------------------------------------------- |
| 1    | Open the name question screen | N/A  | “What is your name?” screen is displayed                            |
| 2    | Leave name input field empty  | N/A  | Name field remains empty                                            |
| 3    | Tap Continue button           | N/A  | User is not moved to the next quiz screen                           |
| 4    | Verify validation behavior    | N/A  | Validation message is displayed or Continue button remains disabled |
| 5    | Verify current screen         | N/A  | User stays on the name screen                                       |

---

# Test Case 7: Name field validates invalid characters

## Objective

Verify that the name field validates invalid characters.

## Test data

| Field        | Value      |
| ------------ | ---------- |
| Invalid name | Mark123!@# |
| Valid name   | Mark       |

## Steps

| Step | Action                                                      | Data       | Expected Result                                                            |
| ---- | ----------------------------------------------------------- | ---------- | -------------------------------------------------------------------------- |
| 1    | Continue through quiz flow until name question is displayed | N/A        | “What is your name?” screen is displayed                                   |
| 2    | Tap name input field                                        | N/A        | Name input field is focused                                                |
| 3    | Enter name with invalid characters                          | Mark123!@# | Invalid value is entered or blocked                                        |
| 4    | Tap Continue button                                         | N/A        | User is not moved to the next screen if invalid characters are not allowed |
| 5    | Verify validation behavior                                  | N/A        | Validation message is displayed or invalid characters are prevented        |
| 6    | Clear name field                                            | N/A        | Name field is empty                                                        |
| 7    | Enter valid name                                            | Mark       | Valid name is accepted                                                     |
| 8    | Tap Continue button                                         | N/A        | User is moved to the personalized screen                                   |

---

# Test Case 8: User can select life areas to improve

## Objective

Verify that the user can select life areas during the quiz flow.

## Test data

| Field     | Value  |
| --------- | ------ |
| Life area | Health |

## Steps

| Step | Action                                                          | Data   | Expected Result                                                                                           |
| ---- | --------------------------------------------------------------- | ------ | --------------------------------------------------------------------------------------------------------- |
| 1    | Continue through quiz flow until life areas screen is displayed | N/A    | “What life areas would you like to improve?” screen is displayed                                          |
| 2    | Verify available life area options                              | N/A    | Options such as Health, Career, Finances, Growth, Relationships, Family, Fun and Spirituality are visible |
| 3    | Select one life area                                            | Health | Selected life area is highlighted or marked as selected                                                   |
| 4    | Verify Continue button                                          | N/A    | Continue button is visible and tappable after selecting at least one life area                            |
| 5    | Tap Continue button                                             | N/A    | User is moved to the next quiz step                                                                       |

---

# Test Case 9: Life area option icons and labels are displayed correctly

## Objective

Verify that life area icons and labels are displayed correctly on Android.

## Preconditions

* User is in the quiz flow.
* User has reached the life areas selection screen.

## Steps

| Step | Action                              | Data   | Expected Result                                                  |
| ---- | ----------------------------------- | ------ | ---------------------------------------------------------------- |
| 1    | Open life areas selection screen    | N/A    | “What life areas would you like to improve?” screen is displayed |
| 2    | Verify life area options            | N/A    | Life area options are visible                                    |
| 3    | Verify icons for life area options  | N/A    | Each life area option has a visible icon                         |
| 4    | Verify labels for life area options | N/A    | Each label is readable and matches the correct life area         |
| 5    | Verify icon and label alignment     | N/A    | Icons and labels are properly aligned and do not overlap         |
| 6    | Select one life area option         | Health | Selected option is highlighted without layout issues             |

---

# Test Case 10: User can rate selected life area using slider

## Objective

Verify that the user can rate a selected life area using a slider.

## Test data

| Field        | Value               |
| ------------ | ------------------- |
| Life area    | Health              |
| Slider value | Any available value |

## Steps

| Step | Action                   | Data                | Expected Result                                               |
| ---- | ------------------------ | ------------------- | ------------------------------------------------------------- |
| 1    | Select life area         | Health              | Rating screen for selected life area is displayed             |
| 2    | Verify rating screen     | N/A                 | “Rate your health” screen is displayed                        |
| 3    | Verify slider            | N/A                 | Slider is visible and usable                                  |
| 4    | Move slider              | Any available value | Slider position changes successfully                          |
| 5    | Verify text below slider | N/A                 | Text related to selected slider value is visible and readable |
| 6    | Tap Continue button      | N/A                 | User is moved to the next quiz step                           |

---

# Test Case 11: User can select coach

## Objective

Verify that the user can select a coach during the quiz flow.

## Preconditions

* User is in the quiz flow.
* User has reached the coach selection screen.

## Steps

| Step | Action                                                               | Data                | Expected Result                                               |
| ---- | -------------------------------------------------------------------- | ------------------- | ------------------------------------------------------------- |
| 1    | Continue through quiz flow until coach selection screen is displayed | N/A                 | “Choose your coach” screen is displayed                       |
| 2    | Verify available coach options                                       | N/A                 | Coach options are visible and displayed correctly             |
| 3    | Scroll coach list if available                                       | N/A                 | User can browse available coach options without layout issues |
| 4    | Select one coach                                                     | Any available coach | Selected coach is highlighted or marked as selected           |
| 5    | Tap “Select and continue” button                                     | N/A                 | Selected coach is saved                                       |
| 6    | Verify next screen                                                   | N/A                 | User is moved to the next quiz step                           |

---

# Test Case 12: User can change selected coach

## Objective

Verify that the user can change coach selection before continuing.

## Preconditions

* User is in the quiz flow.
* User is on the coach selection screen.
* At least two coach options are available.

## Steps

| Step | Action                           | Data                      | Expected Result                                  |
| ---- | -------------------------------- | ------------------------- | ------------------------------------------------ |
| 1    | Open coach selection screen      | N/A                       | Coach options are displayed                      |
| 2    | Select first coach               | Any available coach       | First coach is highlighted or marked as selected |
| 3    | Select another coach             | Different available coach | New coach is highlighted or marked as selected   |
| 4    | Verify previous coach selection  | N/A                       | Previously selected coach is no longer selected  |
| 5    | Tap “Select and continue” button | N/A                       | Updated coach selection is saved                 |
| 6    | Verify next screen               | N/A                       | User is moved to the next quiz step              |

---

# Test Case 13: Personalized user plan is generated after quiz answers

## Objective

Verify that the app generates a personalized plan after the user completes the quiz flow.

## Preconditions

* User is in the quiz flow.
* User can complete all required quiz steps.

## Steps

| Step | Action                               | Data                   | Expected Result                                      |
| ---- | ------------------------------------ | ---------------------- | ---------------------------------------------------- |
| 1    | Complete quiz questions              | Valid quiz answers     | Answers are accepted successfully                    |
| 2    | Select at least one life area        | Health                 | Selected life area is saved                          |
| 3    | Rate selected life area using slider | Any valid slider value | Rating is saved successfully                         |
| 4    | Select focus area                    | Health                 | Focus area is selected                               |
| 5    | Select coach                         | Any available coach    | Selected coach is saved                              |
| 6    | Answer final support question        | Yes, keep me on track  | Answer is selected successfully                      |
| 7    | Continue after final quiz question   | N/A                    | App starts generating personalized user plan         |
| 8    | Wait until generation is completed   | N/A                    | Personalized user plan or result screen is displayed |
| 9    | Verify generated plan content        | N/A                    | Plan content is displayed without error              |

---

# Test Case 14: User name is preserved after going back to name screen

## Objective

Verify that the entered name is preserved after the user goes back to the name screen.

## Test data

| Field | Value |
| ----- | ----- |
| Name  | Mark  |

## Steps

| Step | Action                                                      | Data | Expected Result                                             |
| ---- | ----------------------------------------------------------- | ---- | ----------------------------------------------------------- |
| 1    | Continue through quiz flow until name question is displayed | N/A  | “What is your name?” screen is displayed                    |
| 2    | Enter valid name                                            | Mark | Name is entered correctly                                   |
| 3    | Tap Continue button                                         | N/A  | User is moved to the personalized screen                    |
| 4    | Verify personalized screen                                  | N/A  | Screen with text “Mark, you are in good hands” is displayed |
| 5    | Tap Back button                                             | N/A  | User is returned to the name screen                         |
| 6    | Verify name field value                                     | N/A  | Previously entered name “Mark” is still displayed           |
| 7    | Tap Continue button again                                   | N/A  | User can continue without entering the name again           |

---

# Test Case 15: Quiz answers from one account are not preselected for another account

## Objective

Verify that quiz answers are stored separately for different user accounts.

## Preconditions

* User has access to two different test accounts.
* Account A and Account B are separate accounts.
* App data or session can be changed between accounts if needed.

## Steps

| Step | Action                                                | Data                      | Expected Result                                                            |
| ---- | ----------------------------------------------------- | ------------------------- | -------------------------------------------------------------------------- |
| 1    | Open Aligned app on Android                           | N/A                       | App is opened successfully                                                 |
| 2    | Log in or complete email verification using Account A | Account A                 | Account A is logged in or verified                                         |
| 3    | Complete several quiz questions using Account A       | Example answers           | Answers are selected and saved for Account A                               |
| 4    | Exit quiz flow or close the app                       | N/A                       | User leaves the quiz flow                                                  |
| 5    | Open Aligned app again                                | N/A                       | App is opened successfully                                                 |
| 6    | Log in or complete email verification using Account B | Account B                 | Account B is logged in or verified                                         |
| 7    | Navigate to the same quiz questions                   | N/A                       | Quiz questions are displayed for Account B                                 |
| 8    | Verify selected answers                               | N/A                       | Answers previously selected by Account A are not preselected for Account B |
| 9    | Select answers using Account B                        | Different example answers | Answers are saved only for Account B                                       |

---

# Test Case 16: Quiz state is handled correctly after leaving and reopening quiz flow

## Objective

Verify that the quiz state is handled correctly after the user leaves and reopens the app.

## Preconditions

* User is in the quiz flow.
* User has completed at least a few quiz steps.

## Steps

| Step | Action                               | Data                         | Expected Result                                                                                                                 |
| ---- | ------------------------------------ | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 1    | Complete several quiz steps          | Example answers              | Selected answers are accepted                                                                                                   |
| 2    | Exit the quiz flow                   | Close app or leave quiz page | User leaves the quiz flow                                                                                                       |
| 3    | Reopen Aligned app                   | Same account / same session  | App is opened successfully                                                                                                      |
| 4    | Observe quiz state after reopening   | N/A                          | Quiz state is handled consistently                                                                                              |
| 5    | Verify saved progress or clean state | N/A                          | User either continues from saved step with previous answers preserved, or starts from beginning with no old answers preselected |
| 6    | Continue quiz flow                   | N/A                          | User can continue without errors, broken layout, duplicated answers or mixed data                                               |

---

# Notes

These test cases were created for portfolio purposes based on manual QA work.

The main focus was to demonstrate:

* mobile app testing,
* test case design,
* Action / Data / Expected Result format,
* validation testing,
* UI/UX testing,
* account state testing,
* expected result vs actual result analysis,
* clear QA documentation.

