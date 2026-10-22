
# Synthetic Test Cases

All data in these scenarios is fictional. Expected results are acceptance criteria, not completed test outcomes.

## TC-01 — Normal Opportunity Flow

**Setup:** An authorized administrator has a complete, non-duplicate opportunity.

**Steps:**
1. Prepare the opportunity with job details, eligibility criteria, deadline, and application link.
2. Publish it through the authorized workflow.
3. View it as a student.
4. Open the external application link.
5. Record the status using the available confirmation mechanism.

**Expected result:**
- Opportunity details and deadline are visible.
- The opportunity is shown to the intended audience.
- A link click is not counted as a confirmed application.
- Application status is clearly identified.

**Actual result:** Not executed.
**Evidence:** Pending.
**Status:** Pending.

## TC-02 — Missing Required Information

**Setup:** A synthetic opportunity is missing a required field, such as the deadline or application link.

**Steps:**
1. Attempt to publish the opportunity.
2. Observe the validation response.
3. Add the missing information and retry.

**Expected result:**
- Publication is blocked or the missing information is clearly flagged.
- The required correction is identified.
- No misleading notification is sent.

**Actual result:** Not executed.
**Evidence:** Pending.
**Status:** Pending.

## TC-03 — Duplicate Opportunity

**Setup:** A second synthetic record resembles an existing opportunity by company, role, and deadline.

**Steps:**
1. Create the first opportunity.
2. Attempt to create the similar record.
3. Observe whether a duplicate warning appears.
4. Review the records manually.

**Expected result:**
- A likely duplicate is flagged if that capability exists.
- No record is silently deleted.
- If duplicate detection is unavailable, document the limitation.

**Actual result:** Not executed.
**Evidence:** Pending.
**Status:** Pending.

## TC-04 — Unauthorized Action

**Setup:** A test user without publishing permission attempts to publish or edit an opportunity.

**Steps:**
1. Use a safe test environment or mock.
2. Attempt the restricted action.
3. Observe the response and any audit record.

**Expected result:**
- The unauthorized action is denied.
- No unauthorized change is persisted.
- An audit event is claimed only if the feature exists and the event is observed.

**Actual result:** Not executed.
**Evidence:** Pending.
**Status:** Pending.

## TC-05 — Notification or Application-Status Failure

**Setup:** A safe test or mock simulates notification failure, or an external submission cannot be verified.

**Steps:**
1. Trigger the simulated failure.
2. Observe the status shown to the user.
3. Try the approved fallback, if available.
4. Check whether an external-link click is incorrectly treated as a submission.

**Expected result:**
- The failure is visible.
- A safe fallback or retry path is provided where supported.
- An unverified submission remains unverified.

**Actual result:** Not executed.
**Evidence:** Pending.
**Status:** Pending.

## Execution Record

For each test, record the date, environment, tester role, steps completed, actual result, Pass/Fail/Blocked/Not Tested status, evidence reference, and any limitation.

Do not include credentials or personal data.
