# Task 1 Report: Placement Communication and Application Tracking

## 1. Executive Summary

This assessment explores a proposed improvement to the communication and application-tracking workflow used for campus placements.

The initial workflow description comes from the student's existing understanding of how placement opportunities are shared. The proposed solution is a centralized workflow for recording opportunities, communicating eligibility requirements, tracking application progress, and handling exceptions.

**Investigation status: Hypothetical walkthrough only.** Permission to investigate the institutional process has not been received. No direct staff walkthrough, observation, timing study, or institutional-record review has been conducted. The current process description is therefore unverified.

This report presents a preliminary process hypothesis, a proposed design, five synthetic test scenarios, an evidence log, and a framework for estimating effort. It does not claim measured improvements, completed tests, or proven institutional benefits.

## 2. Problem Statement

Based on the student's account, placement opportunities may be communicated through email and WhatsApp, while students apply using links provided by companies.

This raises questions that require validation:

- Is placement information recorded in one authoritative location?
- How are changes to eligibility criteria and deadlines communicated?
- Can the placement team distinguish students who opened an application link from those who actually submitted an application?
- How are student queries, missing information, and duplicate records handled?
- How much staff time is spent on routine communication and follow-up?

These are investigation questions, not confirmed findings. The current level of fragmentation, workload, and error frequency is unknown.

## 3. Scope and Method

The assessment currently uses:

1. A process description provided by the student.
2. A review of the proposed PlacementHub concept.
3. A hypothetical workflow map.
4. Five synthetic acceptance scenarios.
5. An unpopulated effort and return-on-investment calculator.

No direct institutional fieldwork has been completed. No real student records, company records, or confidential placement data have been used as evidence in this report.

If permission is granted later, the process can be validated through an authorized staff walkthrough and a small, privacy-conscious sample. If permission is declined, the report will remain a hypothetical analysis.

## 4. Preliminary Current-Workflow Hypothesis

The following sequence is based on the student's description and has not been independently verified:

1. A company shares placement information and an application link with the placement cell.
2. Placement staff distribute the opportunity to students through communication channels such as email and WhatsApp.
3. Students review the opportunity and apply through the provided link.
4. Students may contact placement staff with questions or for clarification.
5. Placement staff may need to follow up on information, eligibility, deadlines, or application status.

The actual roles, handoffs, approval requirements, exceptions, and application-counting practices remain to be confirmed.

## 5. Proposed Workflow

The proposed workflow would:

1. Receive a placement opportunity and check that required details are present.
2. Record the opportunity, eligibility criteria, deadline, application link, and accountable staff owner.
3. Require authorized approval before publishing the opportunity.
4. Publish the approved information in a central record and notify eligible students through supported channels.
5. Record notification attempts and failures where the system supports them.
6. Distinguish clearly between an opportunity being published, a notification being sent, a link being opened, a student reporting submission, and a submission being independently verified.
7. Route missing information, duplicate entries, eligibility questions, and deadline changes to an accountable staff member.
8. Maintain an audit trail of important changes and their authorized owners.
9. Provide a fallback procedure if the system or notification service fails.

These are design recommendations. Existing PlacementHub capabilities must be tested before any feature is described as implemented or operational.

## 6. Synthetic Test Scenarios

Five scenarios have been specified:

| Scenario | Expected behaviour |
|---|---|
| Normal request | A complete opportunity follows the approval process and is published only after authorization. |
| Missing information | The opportunity is held for correction rather than published as complete. |
| Duplicate request | A possible duplicate is flagged for review instead of silently creating another record. |
| Unauthorized action | The action is blocked and an appropriate audit event is recorded, where supported. |
| Failed step | The failure is surfaced, a safe retry or manual fallback is available, and duplicate actions are avoided. |

**Execution status:** These are planned synthetic acceptance tests, not completed test results. No successful execution is claimed. Actual results must be recorded after testing in a safe mock or test environment.

## 7. Effort and Potential Value

### 7.1 Evidence Status

No verified monthly request volumes, handling times, rework rates, or implementation effort measurements have been collected. The following example demonstrates how potential time savings would be calculated; it is not a measurement of the placement cell's actual workload or a forecast of guaranteed results.

### 7.2 Illustrative Scenario

For calculation purposes only, assume the following values:

| Input | Illustrative assumption |
|---|---:|
| Monthly requests | 20 |
| Current handling time per request | 25 minutes |
| Current rework rate | 20% |
| Additional rework time per affected request | 15 minutes |
| Proposed routine handling time per request | 12 minutes |
| Human review time per request | 5 minutes |
| Proposed exception rate | 10% |
| Additional handling time per exception | 10 minutes |
| Ongoing monthly support effort | 60 minutes |
| One-time implementation effort | 8 hours |

These assumptions have not been validated with institutional staff and must not be presented as observed facts.

### 7.3 Calculation

**A. Current monthly effort**

Routine handling:

20 requests × 25 minutes = 500 minutes

Expected rework:

20 requests × 20% × 15 minutes = 60 minutes

Total current effort:

500 + 60 = **560 minutes/month**

**B. Proposed monthly effort**

Routine handling and human review:

20 requests × (12 + 5) minutes = 340 minutes

Expected exception handling:

20 requests × 10% × 10 minutes = 20 minutes

Add ongoing support:

340 + 20 + 60 = **420 minutes/month**

**C. Illustrative net time saved**

560 − 420 = 140 minutes/month

140 ÷ 60 = **approximately 2.33 hours/month**

**D. Illustrative simple payback**

8 implementation hours ÷ 2.33 hours saved per month = **approximately 3.43 months**

This simple payback calculation considers time only. It excludes monetary costs, discounting, changes in workload, and uncertainty in the assumptions.

### 7.4 Interpretation and Limitations

Under this hypothetical scenario, the proposed workflow would save approximately 2.33 staff-hours per month before accounting for uncertainty in the estimates.

The result is highly sensitive to request volume, actual handling time, review effort, exception frequency, and ongoing support requirements. If the proposed workflow requires more effort than it saves, the net benefit may be zero or negative.

The example demonstrates the calculation method only. It does not establish that the proposed workflow will save time, that implementation will pay back within 3.43 months, or that the institution should adopt the solution.

A reliable estimate requires authorized baseline measurements and comparable pilot measurements. Until those data exist, the ROI result must remain explicitly illustrative.

## 8. Risks and Limitations

Key risks include:

- Inaccurate application counts if link clicks are treated as completed submissions.
- Incorrect or outdated opportunity information.
- Unauthorized publication or changes.
- Notification failures or students missing updates.
- Additional staff work caused by duplicate records and exceptions.
- Exposure of student or company information.
- Bias or misleading recommendations if AI-based resume matching is introduced without validation.
- Unsupported claims about time savings or return on investment.

The proposal should not automatically reject students based on an AI-generated score. Any future resume-matching feature should be advisory, explainable, privacy-conscious, and subject to human review.

## 9. Decision Criteria

**Proceed to a limited, authorized pilot only if:**

- The placement team grants permission and confirms the real workflow.
- Required roles, approvals, and application-status definitions are agreed.
- Access controls, audit records, privacy safeguards, and a manual fallback are defined.
- Synthetic acceptance tests pass in a safe test environment.
- Baseline and pilot measurements can be collected consistently.

**Change or stop the proposal if:**

- Staff identify a simpler process that achieves the same outcome.
- The proposed workflow adds more work than it removes.
- Application status cannot be verified reliably.
- Privacy, access-control, or operational risks cannot be managed.
- Testing shows repeated failures or no credible benefit.

## 10. Conclusion

A centralized placement communication and tracking workflow is a plausible improvement worth evaluating, but its value has not yet been demonstrated.

At this stage, the deliverable is a preliminary design and evaluation plan, not a verified institutional process study. The next steps are to obtain permission, validate the current workflow, collect a small authorized evidence sample, execute the synthetic tests, and calculate effort using measured inputs.

No claim of institutional approval, direct observation, successful testing, or measured time saving is made in this report.
