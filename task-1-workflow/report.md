# Task 1 — College Workflow Improvement Assessment

## 1. Objective

Investigate a real college workflow, identify avoidable effort and process failures, and evaluate a proposed improvement. The assessment will compare the existing process with the proposed workflow using documented evidence, synthetic tests, and a transparent return-on-investment calculation.

## 2. Workflow Selected

**Workflow:** College placement opportunity communication and coordination.

**Proposed solution:** PlacementHub, an existing placement application intended to help administrators communicate opportunities and students access relevant placement information.

**Scope:** Placement announcements, eligibility information, notifications, application instructions, administrative coordination, and exception handling.

The exact scope of the existing application and the current college process must be verified before making comparative claims.

## 3. Current-State Investigation

Document the current workflow only from permitted observations, interviews, or other legitimate evidence.

Capture:
- Trigger for a new placement opportunity
- Responsible roles and responsibilities
- Communication channels
- Handoffs and approvals
- Eligibility verification
- Duplicate or incomplete information
- Failed or missed communications
- Rework and escalation
- Typical handling time and monthly volume

If access is declined or unavailable, present this section as a hypothetical walkthrough, clearly identifying all assumptions.

## 4. Evidence and Methodology

Maintain an evidence log recording dates, methods, workflow steps, evidence sources, classifications, sample size, permission status, and limitations.

Classify every relevant claim as:
- **Measured:** Directly recorded or calculated from documented observations
- **Estimated:** An informed approximation with a stated method
- **Assumed:** A value used because direct evidence is unavailable
- **Synthetic:** Artificial data used for testing

Synthetic test results must not be presented as evidence of actual college performance.

## 5. Baseline Effort and Scale

Calculate baseline monthly effort from defensible inputs.

Include:
- Monthly number of workflow requests
- Average handling time per request
- Rework rate and rework time
- Administrative coordination effort
- Evidence of delays or errors, where available

If these values cannot be measured, provide a clearly labelled sensitivity analysis rather than claiming measured savings.

## 6. Proposed Workflow

Evaluate how PlacementHub could improve the documented process. Verify implemented functionality before describing it as an existing capability.

Consider required-field validation, eligibility information, authorized publishing, student notifications, duplicate handling, failure recovery, and human approval.

## 7. Testing

Use five synthetic scenarios:
1. Normal valid workflow
2. Missing required information
3. Duplicate placement or event
4. Unauthorized action
5. Failed workflow step or notification

For each test, document the inputs, steps, expected result, actual result, pass/fail outcome, evidence, and follow-up actions.

### Initial Testing Status

The developer reports that PlacementHub includes administrator functionality, placement announcements, eligibility rules, in-app notifications, unread notification status, application-related functionality and audit-related functionality. These capabilities remain subject to verification.

The five synthetic test scenarios have been designed but have not yet been executed. Therefore, no test is currently reported as passed or failed. The assessment will record actual results only after safe execution in an authorized test environment.

## 8. ROI and Net Time Saved

Include baseline handling and rework effort, proposed human review, exception handling, support, and one-time implementation effort.

Show formulas, units, assumptions, and sensitivity to uncertain inputs. Distinguish gross time saved from net time saved and state the period used for any payback calculation.

## 9. Risks and Safeguards

Assess privacy, access control, incorrect eligibility decisions, duplicate notifications, notification failures, inaccurate placement information, system availability, and operational support.

Define mitigation measures and the conditions that would trigger a redesign or abandonment.

## 10. Decision Criteria

Specify measurable criteria for continuing, changing, piloting, or abandoning the proposed workflow. Base the criteria on operational evidence, user needs, reliability, and net benefit.

## 11. Limitations

Describe access constraints, sample size, missing measurements, assumptions, testing limitations, and any functionality that has not been verified.

## 12. Conclusion

Complete this section after gathering evidence and testing the proposed workflow. State what the evidence supports, what remains uncertain, and what should happen next.