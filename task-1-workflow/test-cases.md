# Synthetic Test Cases and Tabletop Walkthrough

## 1. Purpose and Limitations

This document defines five fictional scenarios for evaluating the proposed placement communication and application-tracking workflow.

The scenarios have been reviewed against the proposed design as a tabletop exercise. No tests have been executed against the actual PlacementHub application or an institutional system.

All scenarios use fictional data. The walkthrough outcomes below describe whether the proposed design specifies an appropriate response; they do not demonstrate that the software implements that response.

## TC-01 — Normal Opportunity Flow

**Scenario:** An authorized administrator receives a complete placement opportunity.

**Synthetic setup:**
- Company: Example Systems Ltd.
- Role: Software Engineering Intern.
- Eligibility: Illustrative minimum CGPA of 7.0.
- Deadline: A fictional future date.
- Application link: A safe placeholder.

**Walkthrough:**
1. Placement staff receive the opportunity details.
2. An authorized staff member checks the required information.
3. The opportunity is submitted for approval.
4. An authorized administrator publishes it.
5. A student views the opportunity and opens the application link.
6. The system records only the status supported by available evidence.

**Expected result:**
- Required information is present.
- Publication requires authorization.
- The published opportunity displays its eligibility criteria and deadline.
- Opening the link does not count as a completed application.
- Application status reflects the available evidence.

**Tabletop review outcome:** The proposed workflow specifies validation, approval, publication, and separate application-status categories. Actual software behaviour remains unverified.

**Software execution:** Not performed.

## TC-02 — Missing Required Information

**Scenario:** An opportunity is missing its application deadline.

**Synthetic setup:** A fictional opportunity contains company details and an application link but no deadline.

**Walkthrough:**
1. A placement staff member prepares the opportunity.
2. The opportunity is submitted for publication.
3. The proposed validation process checks the required fields.
4. The staff member supplies the missing deadline and resubmits it.

**Expected result:**
- The incomplete opportunity remains a draft or is flagged for correction.
- The missing field is identified.
- The opportunity is not published as complete before the required correction and approval.

**Tabletop review outcome:** The proposed design specifies that incomplete opportunities should be held for correction. The actual validation rules and error messages have not been tested.

**Software execution:** Not performed.

## TC-03 — Duplicate Opportunity

**Scenario:** A second opportunity resembles an existing record.

**Synthetic setup:** Two fictional records have similar company names, job titles, and deadlines.

**Walkthrough:**
1. An administrator creates the first opportunity.
2. A second similar opportunity is submitted.
3. The proposed workflow flags the possible duplicate where detection is supported.
4. An authorized staff member reviews both records.
5. The staff member decides whether to retain, merge, or close a record according to the approved procedure.

**Expected result:**
- A possible duplicate is flagged where the capability exists.
- No record is silently deleted or merged.
- If automated duplicate detection is unavailable, the limitation is documented and manual review is used.

**Tabletop review outcome:** The proposed design specifies human review of possible duplicates. Automated detection has not been verified.

**Software execution:** Not performed.

## TC-04 — Unauthorized Publication

**Scenario:** A user without publication permission attempts to publish an opportunity.

**Synthetic setup:** A fictional user account has student-level access and no publishing permission.

**Walkthrough:**
1. The user attempts a restricted publication action in the hypothetical workflow.
2. The access-control rule is evaluated.
3. The proposed system denies the action.
4. The system records a security event where audit logging is supported.
5. An authorized administrator reviews the event if necessary.

**Expected result:**
- The unauthorized action is denied.
- No unauthorized publication is persisted.
- Audit logging is claimed only if it is implemented and the event can be observed.

**Tabletop review outcome:** The proposed design requires authorization checks and appropriate audit records. Actual access controls and audit logging have not been tested.

**Software execution:** Not performed.

## TC-05 — Notification Failure or Unverified Application

**Scenario:** A notification fails, or a student opens an external application link but the submission cannot be verified.

**Synthetic setup:** A fictional notification service reports a failure, or an external application destination provides no submission confirmation.

**Walkthrough:**
1. The proposed workflow encounters the notification failure or unknown submission status.
2. The system identifies the failure or retains the application as unverified.
3. Staff use an approved fallback where available.
4. Any retry is handled without assuming the original action failed completely or succeeded.
5. The application count is reviewed to ensure that a link click is not counted as a verified submission.

**Expected result:**
- The notification failure is surfaced where supported.
- An approved alternative communication method is available to staff.
- An unverified application remains unverified.
- Reports distinguish link clicks, student-confirmed applications, and verified submissions.

**Tabletop review outcome:** The proposed design specifies failure handling and status distinctions. Notification recovery and external submission verification have not been tested.

**Software execution:** Not performed.

## 2. Tabletop Review Summary

| Test case | Design-level outcome | Actual software execution |
|---|---|---|
| TC-01: Normal flow | Required stages are specified | Not performed |
| TC-02: Missing information | Correction before publication is specified | Not performed |
| TC-03: Duplicate opportunity | Human review is specified | Not performed |
| TC-04: Unauthorized action | Access denial is required by the design | Not performed |
| TC-05: Failure or unverified submission | Fallback and status distinctions are specified | Not performed |

The tabletop review identifies expected behaviour and remaining implementation questions. It does not establish a software pass rate or confirm that any feature works in the current application.

## 3. Future Execution Record

If authorization is granted to test the application, record the following for each test:

- Date and environment.
- Tester role.
- Application version or commit, where relevant.
- Steps actually completed.
- Actual result.
- Evidence reference, using only non-sensitive synthetic data.
- Status: Pass, Fail, Blocked, or Not Tested.
- Limitations and corrective actions.

Do not record a test as passed until its acceptance criteria have actually been verified. Do not use real student information, credentials, or confidential company data in synthetic tests.
