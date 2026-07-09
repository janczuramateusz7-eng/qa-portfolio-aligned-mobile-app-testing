
# Xray Dataset Example — Aligned Quiz App

## Overview

This file shows an example of using an **Xray Dataset** for manual test cases.

The Dataset was used for the test case:

**[Aligned] User can answer single-choice quiz questions**

The main goal was to avoid creating a separate test case for every similar single-choice question in the quiz flow.

Instead of duplicating test cases, one parameterized test case was used with different test data.

---

## Why Dataset was useful

The Aligned quiz flow contains many similar single-choice questions.

Each question follows the same logic:

1. The question is displayed.
2. Answer options are visible.
3. User selects one answer.
4. Selected answer is marked as selected.
5. User taps **Continue**.
6. User is moved to the next quiz screen.

Because the behavior is repeated, using a Dataset helped reduce duplication and made the test case easier to maintain.

---

## Dataset parameters

The Dataset used two parameters:

| Parameter         | Meaning                                                  |
| ----------------- | -------------------------------------------------------- |
| `Question`        | The quiz question that should be displayed               |
| `Selected_Answer` | The answer that should be selected during test execution |

In Xray steps, parameters can be used like this:

```text id="bdv3nk"
${Question}
${Selected_Answer}
```

---

## Test case example

## Test Case: User can answer single-choice quiz questions

### Objective

Verify that the user can answer single-choice quiz questions and continue through the quiz flow.

### Steps

| Step | Action                                                                 | Data                 | Expected Result                                                  |
| ---- | ---------------------------------------------------------------------- | -------------------- | ---------------------------------------------------------------- |
| 1    | Continue through quiz flow until a single-choice question is displayed | N/A                  | Single-choice question is displayed                              |
| 2    | Verify question text                                                   | `${Question}`        | Question from Dataset is displayed correctly                     |
| 3    | Verify answer options                                                  | N/A                  | Answer options are visible and tappable                          |
| 4    | Select answer option                                                   | `${Selected_Answer}` | Selected answer is highlighted or marked as selected             |
| 5    | Tap Continue button                                                    | N/A                  | User is moved to the next quiz screen                            |
| 6    | Verify quiz flow continues                                             | N/A                  | Next question or informational screen is displayed without error |

---

## Dataset example

| Question                                                          | Selected_Answer                 |
| ----------------------------------------------------------------- | ------------------------------- |
| What do you believe is key to realizing your potential?           | Consistency                     |
| How old are you?                                                  | 25-34                           |
| What gender do you identify with?                                 | Prefer not to say               |
| What is stopping you from reaching your goals?                    | I don’t know where to start     |
| Does stress affect your mood or productivity?                     | Sometimes                       |
| Do you feel anxious about the future?                             | Sometimes                       |
| Does self-doubt hold you back?                                    | Often                           |
| Is it hard for you to say no and set boundaries?                  | Rarely                          |
| Do you ever feel like your past experiences are holding you back? | Sometimes                       |
| How often do you feel energized by your daily activities?         | Often                           |
| Are you comfortable reflecting on your past for growth?           | Maybe                           |
| What story do you tell yourself about achieving your goals?       | I need to be perfect to succeed |
| What motivates you the most on your journey?                      | The need for self-improvement   |
| Need help staying focused?                                        | Yes, keep me on track           |

---

## How this Dataset is executed manually

This is still a **manual test case**.

The Dataset does not click or select answers automatically.

During test execution, the tester uses each Dataset row as test data.

Example:

For this row:

| Question                                                | Selected_Answer |
| ------------------------------------------------------- | --------------- |
| What do you believe is key to realizing your potential? | Consistency     |

The tester should:

1. Navigate to the question:
   `What do you believe is key to realizing your potential?`
2. Check that the question is displayed correctly.
3. Select the answer:
   `Consistency`
4. Verify that the selected answer is highlighted.
5. Tap **Continue**.
6. Verify that the quiz continues to the next screen.

---

## Benefits of using Dataset

Using Dataset helped to:

* reduce duplicate test cases,
* keep one reusable test case for similar questions,
* improve test maintainability,
* make test execution more structured,
* cover multiple quiz questions with different test data,
* keep the test case shorter and easier to review.

---

## What this demonstrates

This example demonstrates practical knowledge of:

* Xray Dataset usage,
* parameterized manual testing,
* test data management,
* single-choice question testing,
* manual test execution,
* Action / Data / Expected Result format,
* reducing duplication in test documentation.

---

## Notes

This Dataset example was created for portfolio purposes.

It shows how a tester can use parameterized data in Xray to cover repeated quiz question behavior without creating unnecessary duplicate test cases.
