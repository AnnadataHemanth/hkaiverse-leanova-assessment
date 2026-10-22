# Task 1 — Risk Assessment and Decision Criteria

## 1. Key Risks and Mitigations

| Risk | Potential impact | Proposed mitigation | Validation method |
|---|---|---|---|
| Incorrect eligibility rules | Eligible students may be excluded or ineligible students may receive an opportunity | Require administrator review and clear eligibility criteria before publication | Test boundary cases with synthetic student profiles |
| Incorrect placement information | Students may act on inaccurate deadlines or requirements | Validate required fields and maintain an authorized correction process | Test incomplete and corrected announcements |
| Notification failure | Students may miss an opportunity or deadline | Display notification status where supported and provide a documented recovery process | Simulate a controlled notification failure |
| Duplicate announcements | Confusion and repeated notifications | Detect duplicates using a suitable identifier or defined matching rules | Submit the same synthetic opportunity twice |
| Unauthorized modification | Incorrect or malicious placement changes | Enforce role-based authorization on the server | Test restricted actions with a non-admin test account |
| Exposure of student data | Privacy harm and loss of trust | Minimize collected data, restrict access, and avoid sensitive data in assessment evidence | Review data flows, permissions and stored fields |
| Service interruption | Students or administrators may lose access | Document failure handling, backups and recovery responsibilities appropriate to the deployment | Test a controlled failure and recovery procedure |
| Unverified time savings | Investment or adoption decisions may be based on misleading ROI | Label assumptions, measure representative cases, and run sensitivity analysis | Compare model inputs with permitted observations |
| Excessive administrative overhead | The proposed system may add work instead of reducing it | Include review, exceptions, troubleshooting and ongoing support in the ROI model | Measure end-to-end effort during a pilot |

## 2. Human Oversight

The system should support administrators rather than silently make consequential placement decisions. Authorized staff should verify opportunity details, eligibility rules, publication decisions and corrections.

Automated checks must clearly identify missing or invalid information and provide a path for resolving exceptions.

## 3. Pilot Evaluation

Before recommending wider adoption, define a pilot with the authorized process owner.

Record:
- Baseline handling and rework effort.
- Proposed workflow effort, including review and support.
- Completion and notification failures.
- Duplicate and unauthorized-action test outcomes.
- User-reported issues through an appropriate, consent-based process.
- Sample size, measurement period and known limitations.

Do not claim that the proposed workflow is better merely because the application operates successfully.

## 4. Decision Rules

### Proceed to a limited pilot when
- Required permission and access controls are in place.
- Critical synthetic tests pass.
- The workflow and data handling are acceptable to the process owner.
- The ROI model includes all material recurring effort.

### Change the design when
- Tests reveal fixable validation, duplication, authorization or recovery problems.
- The workflow adds avoidable steps.
- Support or review effort is materially higher than expected.
- Users cannot reliably understand notification or application status.

### Pause or abandon when
- Serious privacy or authorization risks cannot be mitigated.
- Critical failures remain unresolved.
- A permitted pilot shows no meaningful net benefit and no credible improvement path.
- The process owner determines that the proposed system does not meet operational needs.

## 5. Evidence Required for a Final Recommendation

No final adoption recommendation should be based solely on hypothetical data. State the observed results, sample size, unresolved risks, uncertainty in the ROI inputs and any conditions attached to the recommendation.

The decision rules above are proposed evaluation criteria, not findings from an actual college pilot.