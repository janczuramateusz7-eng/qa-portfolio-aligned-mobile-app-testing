# Aligned Mobile App Testing — Manual QA Portfolio

## Project overview

This repository contains manual QA testing documentation for **Aligned**, a mobile application with a quiz-based onboarding flow.

The project was created as part of a QA internship / training portfolio and focuses on manual testing of the quiz flow on Android.

The main goal was to design and execute test cases, verify expected result vs actual result, report bugs, and document testing results in a clear QA format.

## Application under test

**Aligned**
Mobile application tested on Android.

## Tools used

* Jira
* Xray
* Android device
* Manual testing
* Test documentation
* Bug reporting

## Testing types covered

* Functional testing
* Mobile testing
* UI/UX testing
* Validation testing
* Regression testing
* Exploratory testing
* Test case design
* Test execution
* Bug reporting

## My role

**Junior QA Tester / Manual QA Tester**

My responsibilities included:

* creating manual test cases in Xray,
* preparing test cases in Action / Data / Expected Result format,
* using Dataset for single-choice quiz questions,
* executing existing test cases on Android,
* comparing expected result with actual result,
* marking tests as Passed or Failed,
* documenting actual results for failed tests,
* creating bug reports in Jira,
* assigning severity and priority,
* reviewing test execution results.

## Main tested areas

The main focus was the **Aligned quiz flow** on Android.

Tested areas included:

* email verification,
* quiz intro screen,
* single-choice questions,
* required answer validation,
* name input field,
* name field validation,
* personalized screen after entering name,
* life areas selection,
* life area rating slider,
* coach selection,
* personalized plan generation,
* quiz state after leaving and reopening the app,
* quiz answers separation between different accounts,
* UI issues on Android.

## Test case design

Test cases were created in a clear manual QA format:

* **Action** — what the tester does,
* **Data** — what test data is used,
* **Expected Result** — what should happen.

For single-choice quiz questions, I used an Xray Dataset to avoid creating separate test cases for each similar question.

Example Dataset parameters:

* `Question`
* `Selected_Answer`

This helped reduce duplication and made test cases easier to maintain.

## Example bugs found

* Name field accepts invalid characters during quiz flow.
* Life area option icons and labels are not displayed correctly in quiz flow.
* Quiz answers from one account are preselected for another account.
* Text below life area slider is hidden behind the Continue button.

## Repository structure

README.md
test-cases.md
test-execution-summary.md
bug-reports.md
xray-dataset-example.md
templates/test-case-template.md
templates/bug-report-template.md

## QA skills demonstrated

* Manual test case design
* Manual test execution
* Bug reporting
* Expected result vs actual result comparison
* Xray Dataset usage
* Severity and priority assessment
* Jira/Xray workflow
* Mobile app testing
* UI/UX testing
* Validation testing
* Test documentation
* Account state and data separation testing

## Notes

This repository is a QA portfolio case study based on manual testing tasks.

No private user data, internal Jira links, credentials, or sensitive project information are included.
