
# Test Execution Summary — Aligned Mobile App

## Project

**Aligned Mobile App**

## Task

**Aligned quiz app — Execute TCs Android**

## Objective

The objective of this task was to execute existing manual test cases for the Aligned quiz flow on Android.

The main goal was to verify whether the quiz flow works correctly on Android and whether the actual app behavior matches the expected results defined in the test cases.

## Scope

The test execution focused on the **quiz-based onboarding flow** in the Aligned mobile app.

Tested areas included:

* email verification,
* quiz intro screen,
* single-choice quiz questions,
* required answer validation,
* name input field,
* name field validation,
* personalized screen after entering name,
* life areas selection,
* life area rating slider,
* coach selection,
* personalized plan generation,
* quiz state handling,
* account data separation,
* UI behavior on Android.

## Environment

| Area                 | Details        |
| -------------------- | -------------- |
| Application          | Aligned        |
| Platform             | Mobile App     |
| Device               | Android        |
| Test Management Tool | Xray           |
| Bug Tracking Tool    | Jira           |
| Test Type            | Manual testing |

## Test execution approach

Each test case was executed manually on Android.

For every test case, I followed the steps defined in Xray:

* **Action** — what should be done,
* **Data** — what test data should be used,
* **Expected Result** — what should happen after the action.

During execution, I compared the **Expected Result** with the **Actual Result**.

## Test status rules

| Status | Meaning                                              |
| ------ | ---------------------------------------------------- |
| Passed | Actual result matched the expected result            |
| Failed | Actual result was different from the expected result |

## Main focus during execution

The main focus was to verify the full quiz flow from the user perspective.

I checked whether the app correctly handles:

* navigation between quiz screens,
* selecting answers,
* required fields,
* name input validation,
* life area selection,
* slider behavior,
* UI layout on Android,
* account state and stored quiz answers,
* separation of data between different accounts.

## Main findings

During test execution, several issues were found in the quiz flow.

The most important findings were:

1. Name field accepted invalid characters.
2. Life area option icons and labels were not displayed correctly.
3. Quiz answers from one account were preselected for another account.
4. Text below the life area slider was hidden behind the Continue button.

## Reported bugs

| Bug Summary                                                                | Severity | Priority |
| -------------------------------------------------------------------------- | -------- | -------- |
| Name field accepts invalid characters during quiz flow                     | Medium   | Medium   |
| Life area option icons and labels are not displayed correctly in quiz flow | Medium   | Medium   |
| Quiz answers from one account are preselected for another account          | High     | High     |
| Text below life area slider is hidden behind Continue button               | Medium   | Medium   |

## Example actual results

Example 1:

```text
User can continue after entering a name with invalid characters.

No validation message is displayed near the name field.

The app accepts invalid characters in the name field during the quiz flow.
```

Example 2:

```text
After moving the life area rating slider, additional text appears below the slider, but it is hidden behind the Continue button.

The user cannot fully read the displayed text because it is covered by the button.
```

Example 3:

```text
Answers previously selected by Account A are preselected when using Account B.

The app displays quiz answers from another account.

Quiz state is not properly separated between different user accounts.
```

## QA observations

The test execution showed several risks in the quiz flow.

From a QA perspective, the most important risks were:

* incorrect validation of user input,
* UI elements not displayed correctly on Android,
* content hidden behind fixed buttons,
* possible issue with account data separation,
* quiz answers being reused between different accounts,
* inconsistent app state between sessions or accounts.

## Most important issue

The most important bug found during execution was:

**Quiz answers from one account are preselected for another account**

This issue was rated as:

* **Severity:** High
* **Priority:** High

Reason:

This bug may affect user privacy, account data separation and the correctness of quiz personalization.

## What I practiced

During this task, I practiced:

* manual mobile app testing,
* working with existing test cases,
* using Xray Test Execution,
* comparing expected result with actual result,
* documenting actual results for failed tests,
* creating bug reports in Jira,
* assigning severity and priority,
* UI/UX testing on Android,
* validation testing,
* account state testing,
* clear QA documentation.

## Summary

This test execution helped verify the Aligned quiz flow on Android.

The main outcome was identifying issues related to input validation, UI layout and account data separation.

All found issues were documented as bug reports with clear steps to reproduce, expected results, actual results, severity and priority.
