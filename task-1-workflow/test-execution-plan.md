# PlacementHub — Task 1 Test Execution Plan

## 1. Objective

Evaluate five synthetic scenarios against the existing PlacementHub application without changing its source code or modifying production data.

## 2. Safety Conditions

Before testing:

- Obtain authorization for the test environment.
- Prefer a local instance or isolated staging environment.
- Use only synthetic placement records and designated test accounts.
- Do not send real student notifications or contact real applicants.
- Do not test unauthorized access against a live system.
- Avoid destructive operations and use reversible test records.
- Record the application version or commit tested, where available.
- Stop if a test risks changing production data or notifying real users.

If an isolated environment cannot be used safely, document the test as pending instead of executing it.

## 3. Synthetic Test Fixtures

Use artificial data such as:

**Placement A**
- Title: Synthetic Data Analyst Internship
- Eligibility threshold: CGPA 7.50
- Application deadline: 31 December 2026
- Application URL: A reserved example URL or local mock endpoint
- Record identifier: TEST-PLACEMENT-001

**Placement B**
- Title: Synthetic Software Engineering Internship
- Eligibility threshold: CGPA 8.00
- Application deadline: 31 December 2026
- Record identifier: TEST-PLACEMENT-002

Use designated test accounts with documented roles. Do not use real student names, identifiers, resumes or credentials.

## 4. Test Cases

### TC-01 — Normal Placement Creation

**Objective:** Determine whether a complete placement can be created and published by an authorized administrator.

**Procedure:**
1. Sign in using an authorized test administrator.
2. Enter Placement A using synthetic details.
3. Submit the form.
4. Inspect the resulting record and status.
5. Verify student visibility and in-app notification behavior using a designated test account, if the environment supports it.

**Expected outcome:** Required information is accepted, the placement reaches the intended state, and supported notification behavior is observable.

**Record:** Validation results, final status, student visibility and notification result.

### TC-02 — Missing Required Information

**Objective:** Determine how the application handles incomplete placement details.

**Procedure:**
1. Prepare a synthetic placement with a required field omitted, such as the deadline.
2. Submit it using the authorized test administrator.
3. Observe validation messages and record state.
4. Verify whether incomplete information can be published.

**Expected outcome:** The system clearly identifies the missing information and follows its intended validation rules.

**Record:** Missing field, displayed response, final state and whether publication was permitted.

### TC-03 — Duplicate Placement

**Objective:** Determine whether repeated submission creates duplicate records or notifications.

**Procedure:**
1. Create a synthetic placement in the isolated test environment.
2. Submit the same placement again using the same test data.
3. Inspect the resulting records and relevant notification events.
4. Record whether the system rejects, flags or accepts the second submission.

**Expected outcome:** Behavior is documented accurately. If duplicate prevention is a requirement, the application should prevent or explicitly flag the duplicate according to the defined design.

**Record:** Number of records, warning or error, notification count and resulting state.

**Important:** Do not claim duplicate prevention merely because an audit-related feature exists.

### TC-04 — Unauthorized Administrative Action

**Objective:** Determine whether restricted placement actions require appropriate authorization.

**Procedure:**
1. Use a designated test account without administrator privileges.
2. Attempt to access a restricted action through the normal test interface.
3. If authorized security testing permits it, verify the corresponding server-side authorization behavior in the isolated environment.
4. Check that the placement was not modified.

**Expected outcome:** Restricted actions are denied, and the unauthorized account cannot make administrative changes.

**Record:** Test role, attempted action, response, and resulting state.

**Safety:** Do not bypass controls on a production system or use another person's account.

### TC-05 — Notification or Workflow Failure

**Objective:** Determine how the application behaves when a notification or dependent step fails.

**Procedure:**
1. Use a controlled local or staging environment.
2. Simulate a supported failure condition, such as a mock notification failure or unavailable test endpoint.
3. Observe the status presented to the administrator.
4. Check whether the record remains consistent.
5. Test retry or recovery only if the application supports it.

**Expected outcome:** The failure is observable, system state remains safe, and any supported recovery behavior is documented.

**Record:** Failure setup, displayed status, retry result and duplicate side effects.

## 5. Results Register

| Test | Execution status | Outcome |
|---|---|---|
| TC-01 | Not executed | Pending |
| TC-02 | Not executed | Pending |
| TC-03 | Not executed | Pending |
| TC-04 | Not executed | Pending |
| TC-05 | Not executed | Pending |

## 6. Test Evidence Template

For every executed scenario, record:

- Test ID:
- Execution date:
- Environment:
- Application version or commit:
- Tester authorization:
- Synthetic inputs:
- Procedure followed:
- Expected result:
- Actual result:
- Pass, fail or blocked:
- Evidence reference:
- Defect or limitation:
- Retest result, if applicable:

## 7. Acceptance Criteria

A test passes only if the observed behavior satisfies the stated expected outcome. A blocked test is not a pass. If a required capability is absent, record that limitation rather than inventing a result.

## 8. Reporting

Summarize the number of tests passed, failed, blocked and not executed. Include significant limitations and unresolved defects in the final report. Do not generalize results from a small synthetic test set into claims of production reliability.