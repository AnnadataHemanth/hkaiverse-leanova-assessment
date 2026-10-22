# Task 1 — Synthetic Test Plan

## Purpose

Evaluate whether the proposed placement workflow handles common cases safely. All test data must be artificial. No real student information or live placement activity is needed.

**Execution status:** Not yet executed against the application. Expected outcomes below are test criteria, not test results.

## TC-01 — Normal Placement

**Synthetic input:** A complete placement announcement with valid dates, eligibility criteria, and an application URL.

**Expected outcome:** The authorized administrator can submit the announcement; required information is validated; publication follows the intended approval process; the intended audience can access the announcement.

**Evidence to record:** Steps performed, resulting status, validation behavior, and a screenshot or sanitized log if useful.

## TC-02 — Missing Information

**Synthetic input:** A placement announcement missing a required field, such as an application deadline.

**Expected outcome:** The system blocks or clearly flags incomplete information before publication, according to its defined rules.

**Evidence to record:** Missing field, validation message, resulting status, and whether publication was prevented.

## TC-03 — Duplicate Announcement

**Synthetic input:** Submit the same synthetic placement identifier or equivalent announcement twice.

**Expected outcome:** The system detects the duplicate or handles it safely according to documented behavior. It should not silently create unintended duplicate notifications.

**Evidence to record:** Number of records created, notification behavior, and any duplicate warning.

## TC-04 — Unauthorized Action

**Synthetic input:** A test account without administrator permissions attempts to create or modify a placement.

**Expected outcome:** The restricted action is denied and protected information is not exposed.

**Safety note:** Use only an authorized local test environment and test accounts. Do not probe a live production system without permission.

**Evidence to record:** Account role, attempted action, response, and resulting system state.

## TC-05 — Failed Step or Notification

**Synthetic input:** Simulate a failed notification or unavailable application endpoint in a controlled test environment.

**Expected outcome:** The failure is visible, the system preserves a safe state, and an appropriate retry or escalation path exists if supported.

**Evidence to record:** Failure condition, displayed status, retry behavior, and whether duplicate actions occurred.

## Results Table

| Test | Expected outcome | Actual outcome | Status |
|---|---|---|---|
| TC-01 | Valid placement handled correctly | Pending execution | Not tested |
| TC-02 | Incomplete information handled safely | Pending execution | Not tested |
| TC-03 | Duplicate handled safely | Pending execution | Not tested |
| TC-04 | Unauthorized action denied | Pending execution | Not tested |
| TC-05 | Failure handled safely | Pending execution | Not tested |

## Acceptance Rule

Mark a test as passed only after observing its actual result and confirming that it meets the expected outcome. Document failures and limitations rather than changing the recorded outcome to match expectations.