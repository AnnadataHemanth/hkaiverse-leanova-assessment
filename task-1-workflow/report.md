
# Task 1 Report: Placement Communication and Application Tracking

## 1. Executive Summary

This assessment examines the campus placement opportunity communication and application-tracking workflow.

Based on the student's account, companies share job details and application links with the placement cell, which distributes the information through email and WhatsApp. Students apply through the supplied links, while communication between students and the placement cell is not centralized.

The proposed improvement is a centralized opportunity record with consistent eligibility criteria, deadlines, student notifications, a defined question channel, and clear application-status tracking.

A company-specific AI resume-matching assistant is proposed as a possible future extension.

This assessment is preliminary. No measured processing times, monthly volumes, rework rates, or executed test outcomes have been supplied. Therefore, no numerical time-saving or ROI claim is made.

## 2. Problem Statement

Fragmented announcements and follow-up may make it harder for students to find current opportunity information and for placement staff to maintain a reliable view of questions and application status.

The frequency, effort, and impact of these issues must be established through authorized observations.

## 3. Scope

### Included
- Current workflow mapping.
- Roles and handoffs.
- Proposed improved workflow.
- Five synthetic test cases.
- ROI calculation model.
- Risks and decision criteria.

### Excluded
- Modifications to the existing PlacementHub application.
- Production deployment or external integrations.
- Unverified claims about notification delivery or application submissions.
- Automatic candidate rejection based on an AI score.
- Use of real student personal data in synthetic tests.

## 4. Evidence and Method

The current workflow is based on the student's account. This repository currently contains no structured observations, recorded timing observations, or verified process records.

The student indicated that permission was handled, but no dated permission or observation record is included here.

Further validation should record:
- Observation date and relevant role.
- Number of cases observed and sampling method.
- Handling times, where measurement is authorized.
- Rework cases and reasons.
- How external application submissions are counted.
- Exceptions and how they are handled.
- Limitations and any assumptions.

Measurements, estimates, and assumptions must be clearly distinguished.

## 5. Current Workflow

1. Company shares job details and an application link.
2. Placement staff distribute the information through email and WhatsApp.
3. Students review the opportunity and apply through an external link.
4. Students may need to contact placement staff for clarification.
5. The method used to confirm actual external submissions and count applications remains unverified.

## 6. Proposed Improvement

Use one authoritative opportunity record, consistent eligibility criteria and deadlines, central student visibility, notifications, a defined question channel, and clear application-status categories.

Distinguish link opened, student-confirmed, and verified submitted. An external application should only be called verified when reliable confirmation is available.

## 7. Test Plan

Five synthetic cases are specified:
1. Normal opportunity flow.
2. Missing required information.
3. Duplicate opportunity.
4. Unauthorized action.
5. Notification failure or unverified application status.

These are planned tests, not completed tests. Actual outcomes must be recorded after execution.

## 8. ROI Approach

The calculator estimates current monthly effort as routine handling plus expected rework.

Proposed effort includes routine handling, human review, expected exception handling, and ongoing support.

Net monthly time saved is converted into hours. Simple payback is calculated by dividing one-time implementation effort by positive monthly hours saved.

All input cells remain blank pending evidence. Scenario values may be used only when clearly labelled as assumptions. If proposed effort equals or exceeds current effort, report no time saving or added effort.

## 9. Risks and Limitations

- The current workflow has not been independently observed in this repository.
- The external application-counting method remains unknown.
- No quantitative baseline or executed test result is available.
- PlacementHub capabilities are developer-reported and not independently verified here.
- AI resume matching may produce inaccurate or biased scores.
- Resume processing requires appropriate consent, access restrictions, and data-retention controls.

## 10. Conclusion

Centralizing placement communication and application tracking is a plausible workflow improvement. Its benefits must be demonstrated rather than assumed.

The next steps are to validate the process, record a small authorized sample, execute the synthetic tests, and calculate ROI using supported inputs before recommending a wider pilot.
