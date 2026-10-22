# Task 1 Report: Placement Communication and Application Tracking

## 1. Executive Summary

This assessment explores a possible improvement to the communication and application-tracking workflow for campus placements.

The initial workflow description comes from the student's existing understanding of how placement opportunities are shared. The proposed solution is a centralized process for recording opportunities, communicating eligibility requirements, tracking application progress, and handling exceptions.

**Investigation status: Hypothetical walkthrough only.** Permission to investigate the institutional process has not been received. No direct staff walkthrough, observation, timing study, or institutional-record review has been conducted.

This report provides a preliminary workflow hypothesis, proposed design, five synthetic test scenarios, an evidence-based limitations statement, and an illustrative effort calculation. It does not claim measured improvements, completed software tests, or proven institutional benefits.

## 2. Problem Statement

Based on the student's account, placement opportunities may be communicated through email and WhatsApp, while students apply through links provided by companies.

This raises questions requiring validation:

- Is placement information maintained in one authoritative location?
- How are changes to eligibility criteria and deadlines communicated?
- Can the placement team distinguish link clicks from actual application submissions?
- How are student queries, missing information, and duplicate records handled?
- How much staff time is spent on routine communication, follow-up, and rework?

These are investigation questions, not confirmed findings. The actual workload, error frequency, and limitations of the existing process remain unknown.

## 3. Scope and Method

The current assessment uses:

1. A process description provided by the student.
2. A conceptual review of the proposed PlacementHub workflow.
3. A hypothetical current-process map.
4. Five synthetic acceptance scenarios.
5. An illustrative effort and return-on-investment calculation.
6. A preliminary risk and decision-criteria review.

No direct institutional fieldwork has been completed. No real student records, company records, or confidential placement data have been used as evidence in this report.

If permission is granted, the workflow can be validated through an authorized staff walkthrough and a small, privacy-conscious sample. If permission is declined, the work must remain explicitly hypothetical.

## 4. Preliminary Current-Workflow Hypothesis

The following sequence is based on the student's description and has not been independently verified:

1. A company shares placement information and an application link with the placement cell.
2. Placement staff distribute the opportunity through channels such as email and WhatsApp.
3. Students review the opportunity and apply using the provided link.
4. Students may contact placement staff for clarification.
5. Staff may need to follow up on missing information, eligibility, deadlines, or application status.

The actual roles, handoffs, approval requirements, exceptions, and application-counting practices remain to be confirmed.

### Evidence limitations

- Direct observations: 0
- Verified timing observations: 0
- Verified institutional process records reviewed: 0
- Staff walkthroughs completed: 0
- Software test executions: 0

These counts describe the evidence collected for this assessment, not the institution's actual activity.

## 5. Proposed Workflow

The proposed workflow would:

1. Receive a placement opportunity and check whether required details are present.
2. Record the opportunity, eligibility criteria, deadline, application link, and accountable staff owner.
3. Require an authorized approval before publication.
4. Publish approved information in a central record and notify eligible students through supported channels.
5. Record notification attempts and failures where the system supports them.
6. Distinguish between publication, notification delivery, link opening, student-reported submission, and independently verified submission.
7. Route missing information, duplicate entries, eligibility questions, and deadline changes to an accountable staff member.
8. Maintain an audit trail of important changes and the authorized person responsible.
9. Provide a manual fallback when the application or notification system fails.

These are design recommendations. Existing PlacementHub capabilities must be verified before any feature is described as implemented or operational.

## 6. Synthetic Test Scenarios

Five synthetic scenarios have been designed for a future safe mock or test environment.

| Scenario | Expected result | Decision owner and recovery |
|---|---|---|
| Normal request | A complete opportunity proceeds through approval and is published only after authorization. | Authorized placement staff approve publication; the system records the outcome. |
| Missing information | The opportunity is held and marked as incomplete. | The opportunity owner supplies the missing details before resubmission. |
| Duplicate request | A possible duplicate is flagged rather than silently creating a second record. | Placement staff compare the records and decide whether to merge, retain, or reject the duplicate. |
| Unauthorized action | The action is blocked and an audit event is recorded where supported. | An authorized administrator reviews the event and resolves any access issue. |
| Failed step | The failure is surfaced, and a safe retry or manual fallback is available. | The designated process owner checks the outcome before retrying to avoid duplicate actions. |

**Execution status:** These are expected outcomes from a tabletop design review, not completed software test results. No successful execution is claimed. Actual results, defects, and recovery outcomes must be recorded after authorized testing.

## 7. Effort and Potential Value

### 7.1 Evidence status

No verified monthly request volumes, handling times, rework rates, or implementation effort measurements have been collected.

The following scenario demonstrates the calculation method only. All inputs are illustrative assumptions, not observed facts or guaranteed results.

### 7.2 Illustrative assumptions

| Input | Assumption |
|---|---:|
| Monthly requests | 20 |
| Current handling time per request | 25 minutes |
| Current rework rate | 20% |
| Additional rework time per affected request | 15 minutes |
| Proposed routine handling time per request | 12 minutes |
| Human review time per request | 5 minutes |
| Proposed exception rate | 10% |
| Additional handling time per exception | 10 minutes |
| Ongoing support effort | 60 minutes/month |
| One-time implementation effort | 8 hours |

These values have not been validated with institutional staff.

### 7.3 Current monthly effort

Routine handling:

20 requests × 25 minutes = 500 minutes

Expected rework:

20 requests × 20% × 15 minutes = 60 minutes

Total:

500 + 60 = **560 minutes/month**, or approximately **9.33 hours/month**.

### 7.4 Proposed monthly effort

Routine handling plus human review:

20 requests × (12 + 5) minutes = 340 minutes

Expected exception handling:

20 requests × 10% × 10 minutes = 20 minutes

Add monthly support:

340 + 20 + 60 = **420 minutes/month**, or **7 hours/month**.

### 7.5 Illustrative net savings and payback

Net time saved:

560 − 420 = 140 minutes/month

140 ÷ 60 = **approximately 2.33 hours/month**.

Simple time-based payback:

8 implementation hours ÷ 2.33 hours saved/month = **approximately 3.43 months**.

This is a simple illustrative calculation. It excludes monetary costs, discounting, changes in workload, and uncertainty in the assumptions.

### 7.6 Sensitivity analysis

To demonstrate the effect of request volume, keep the per-request assumptions constant:

- Current effort: 25 routine minutes + 3 expected rework minutes = 28 minutes/request.
- Proposed effort before monthly support: 12 routine minutes + 5 review minutes + 1 expected exception minute = 18 minutes/request.
- Ongoing support: 60 minutes/month.
- One-time implementation: 8 hours.

| Requests/month | Current effort | Proposed effort including support | Net savings/month | Simple payback |
|---:|---:|---:|---:|---:|
| 10 | 280 min | 240 min | 40 min (0.67 h) | 12.00 months |
| 20 | 560 min | 420 min | 140 min (2.33 h) | 3.43 months |
| 40 | 1,120 min | 780 min | 340 min (5.67 h) | 1.41 months |

These figures are scenario calculations, not confidence intervals, measured outcomes, or predictions of actual institutional performance.

### 7.7 Interpretation

The illustrative scenario suggests that request volume is an important factor because ongoing support effort is assumed to remain fixed each month. At low volumes, the savings may not justify implementation effort. At higher volumes, the same per-request reduction can produce greater monthly savings.

Actual results could be lower, zero, or negative if handling and review take longer than assumed, exceptions are more frequent, or support requirements increase.

A credible ROI assessment requires authorized baseline measurements and comparable pilot measurements. Until then, the calculations must remain explicitly illustrative.

## 8. AI Versus Ordinary Software

The initial workflow can largely be managed with ordinary software: required-field validation, role-based access, approval states, duplicate checks, notifications, and audit logs.

AI is not necessary for these deterministic steps. It may be useful as an optional later enhancement for extracting details from unstructured job descriptions or suggesting resume-to-job matches. Such outputs should be advisory, explainable, privacy-conscious, and subject to human review.

An AI-generated score should not automatically reject a student. Any AI feature should be tested separately against agreed criteria and should not be presented as accurate or beneficial without evidence.

## 9. Risks and Limitations

Key risks include:

- Incorrect application counts if link clicks are treated as completed submissions.
- Inaccurate or outdated opportunity details.
- Unauthorized publication or changes.
- Notification failures or missed updates.
- Additional staff work caused by duplicates and exceptions.
- Exposure of student or company information.
- Misleading recommendations from an unvalidated AI feature.
- Unsupported claims about time savings or return on investment.

Mitigations should include explicit application-status definitions, authorized approvals, access controls, audit records, safe retry logic, a manual fallback, data minimization, and human oversight.

## 10. Decision Criteria

### Proceed to a limited, authorized pilot only if

- The placement team grants permission and confirms the actual workflow.
- Roles, approvals, and application-status definitions are agreed.
- Access controls, audit records, privacy safeguards, and manual fallback procedures are defined.
- Synthetic acceptance tests pass in a safe test environment.
- Baseline and pilot measurements can be collected consistently.
- The measured benefit justifies implementation and ongoing support effort.

### Change or stop the proposal if

- Staff identify a simpler process that achieves the same outcome.
- The proposed workflow adds more work than it removes.
- Application status cannot be verified reliably.
- Privacy, access-control, or operational risks cannot be managed.
- Testing shows repeated failures or no credible benefit.

## 11. Next Steps and Conclusion

The proposed centralized placement workflow is a plausible improvement worth evaluating, but its value has not been demonstrated.

The next steps are to:

1. Obtain permission before investigating the institutional process.
2. Conduct an authorized staff walkthrough and validate roles, handoffs, approvals, and exceptions.
3. Record a small, privacy-conscious sample of timings and process counts, if permitted.
4. Run the five synthetic acceptance tests in a safe test environment and document actual outcomes.
5. Replace illustrative ROI inputs with measured values and reassess the decision criteria.

**Task 1 deliverable status:** Preliminary hypothetical analysis, proposed workflow, synthetic test design, and illustrative effort calculations prepared. Institutional investigation and software validation remain incomplete because permission has not been received and no software tests have been executed.

No claim of institutional approval, direct observation, successful testing, or measured time saving is made in this report.