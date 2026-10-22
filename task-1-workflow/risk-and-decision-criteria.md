
# Risks and Decision Criteria

## 1. Risks and Mitigations

| Risk | Potential impact | Mitigation |
|---|---|---|
| Inaccurate application counts | Link clicks may be mistaken for submissions | Separate click, student-confirmed, and verified-submission statuses |
| Outdated opportunity details | Students may follow old deadlines or eligibility criteria | Maintain one authoritative record and record updates |
| Unauthorized edits | Incorrect details may be published | Use access controls, review, and audit logging where supported |
| Notification failure | Students may miss opportunities | Show delivery status where available and provide an approved fallback |
| Additional administrative work | Review and support may offset time savings | Measure end-to-end handling, exceptions, and support |
| Personal-data exposure | Student details and resumes may be disclosed | Minimize collection, restrict access, obtain consent, and limit retention |
| AI score bias or false confidence | Candidates may be unfairly assessed | Explain evidence, evaluate bias, allow review, and never auto-reject solely by score |
| Unsupported ROI assumptions | Benefits may be overstated | Separate measurements, estimates, and assumptions |

## 2. Proceed Criteria

Recommend a limited pilot only when:
- The current workflow and responsible owner are confirmed.
- Authorization and data-handling boundaries are clear.
- Required fields, roles, and status definitions are agreed.
- Critical synthetic tests pass or mitigations are accepted.
- ROI inputs are measured or clearly labelled as scenario assumptions.
- Staff can correct records and handle exceptions.

## 3. Change Criteria

Revise the proposal if:
- Application status cannot be reliably verified.
- Staff must duplicate substantial work across tools.
- Students cannot understand eligibility or application status.
- Notification failure has no practical fallback.
- Review and support effort removes the expected time savings.
- Tests reveal confusing or inconsistent status handling.

## 4. Stop Criteria

Do not proceed to a live pilot if:
- Required authorization is absent.
- The workflow requires unnecessary exposure of student personal data.
- Unauthorized publication remains unmitigated.
- Unverified applications are presented as verified submissions.
- Risk or effort exceeds likely benefit and no practical mitigation exists.

## 5. Current Decision

**Recommendation:** Continue process validation and synthetic testing. Do not claim proven ROI or production readiness while baseline measurements and test results remain unavailable.
