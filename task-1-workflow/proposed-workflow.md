# Proposed Workflow: Centralized Placement Communication and Tracking

## 1. Objective

Design a centralized workflow for managing placement opportunities, communicating eligibility requirements, handling student questions, and tracking application progress.

This proposal builds on the PlacementHub project concept. It is a proposed design, not evidence of an approved or deployed institutional system.

## 2. Proposed Workflow

### Step 1: Receive an Opportunity

The placement cell receives the company details, job description, eligibility criteria, deadline, and application link.

**Accountable owner:** Designated placement staff member.

**Required inputs:**
- Company and opportunity details.
- Job description and eligibility requirements.
- Application link and deadline.
- Source of the information.
- Any required approval or supporting documentation.

If required information is missing, the opportunity remains a draft until the missing details are supplied.

### Step 2: Validate and Approve

An authorized placement staff member checks the information for completeness and accuracy.

**Approval boundary:** Only a staff member with the appropriate authority may approve an opportunity for publication. Creating or editing a draft must not automatically publish it.

If information is unclear, contradictory, or unverified, the opportunity is held for clarification.

### Step 3: Publish the Opportunity

After approval, the authorized staff member publishes the opportunity in the central system.

The published record should include eligibility criteria, application instructions, the deadline, and the accountable staff contact or question channel.

**Accountable owner:** Authorized placement administrator.

**Audit record:** Where supported, record the opportunity ID, editor, approver, timestamps, status changes, and the reason for material changes.

### Step 4: Notify Students

The system makes the approved opportunity available to students and sends notifications through supported channels.

In-app notifications are the proposed baseline. Email or WhatsApp automation must not be claimed unless it has been implemented and tested.

If a notification fails, the system should record the failure where supported. Staff can then use an approved alternative communication channel.

### Step 5: Check Eligibility

The system displays the published eligibility requirements. If authorized student information is available, it may assist with preliminary eligibility checks.

Cases involving missing information, conflicting records, or disputed eligibility are referred to placement staff.

Automated checks must not silently override an authorized placement decision.

### Step 6: Track Application Progress

Application statuses must represent what is actually known.

| Status | Meaning |
|---|---|
| Draft | Opportunity information is being prepared. |
| Pending approval | The opportunity is awaiting authorized review. |
| Published | The opportunity has been approved and made available. |
| Link opened | A tracked application link was opened; submission is not confirmed. |
| Student-confirmed | The student reports submitting an application. |
| Submission verified | A reliable confirmation or authorized integration verifies submission. |
| Closed | The opportunity is no longer accepting applications or has been closed by an authorized staff member. |

Not every status applies to every opportunity. External application links may not provide submission confirmation.

**Important:** A link click must never be counted as proof of a completed application. Reports must distinguish confirmed, verified, and unknown application statuses.

### Step 7: Handle Student Questions

Students use a designated question channel. Each recorded query should have:

- A query reference ID.
- The related opportunity, where applicable.
- A category and date received.
- An assigned staff owner.
- A status and response record.

The designated owner reviews the query, requests clarification if needed, and records the resolution.

Sensitive student information should not be copied into unnecessary records or exposed to unauthorized users.

### Step 8: Handle Changes and Close Opportunities

Changes to eligibility, deadlines, application links, or other material details require review by an authorized staff member.

The system should preserve the previous value and record the reason for a material change where supported. Affected students should be notified through available channels.

An authorized staff member closes the opportunity when appropriate. The record should remain available for authorized review rather than being silently deleted.

## 3. Ownership and Approval Boundaries

| Activity | Responsible role | Approval or control |
|---|---|---|
| Submit company information | Company contact or placement staff | Information must be checked before publication. |
| Validate opportunity details | Designated placement staff | Missing or conflicting details must be resolved. |
| Publish or materially change an opportunity | Authorized placement administrator | Explicit authorization required. |
| View opportunities and eligibility | Student | Access limited to permitted information. |
| Report application submission | Student | Recorded as student-confirmed, not automatically verified. |
| Verify an external submission | Authorized staff or reliable integration | Mark verified only when supporting evidence exists. |
| Resolve disputed eligibility | Authorized placement staff | Human decision required. |
| Review failures and exceptions | Designated placement staff or system administrator | Follow the approved recovery process. |

These are proposed responsibilities. Actual institutional roles and authorization rules must be confirmed before implementation.

## 4. Exception Handling and Fallbacks

| Exception | System response | Human owner or fallback |
|---|---|---|
| Missing company or job details | Keep the record in draft and identify missing fields. | Placement staff contact the information provider. |
| Possible duplicate opportunity | Flag the potential duplicate; do not silently delete records. | Authorized staff decide whether to merge, retain, or close the duplicate. |
| Unauthorized publication or edit | Deny the action and record the security event where supported. | Administrator reviews the incident. |
| External submission cannot be verified | Retain an unverified status. | Student or authorized staff may provide reliable confirmation. |
| Notification failure | Record the failure where supported and avoid claiming successful delivery. | Staff use an approved alternative channel. |
| System outage | Do not assume that a failed action succeeded. | Use an approved temporary process and reconcile records after recovery. |
| Deadline or eligibility changes | Require authorization and preserve a change record. | Placement staff review the change and communicate it to affected students. |
| Conflicting eligibility information | Flag the case for review. | Authorized placement staff make the decision. |

A fallback must not bypass approval, access control, or privacy requirements.

## 5. Auditability and Data Protection

The proposed system should maintain an audit record for significant actions, where supported:

- Record creation and publication.
- Approval and rejection of publication requests.
- Changes to deadlines, eligibility, and application links.
- Status changes and their supporting evidence.
- Access-control failures and relevant system errors.
- Exception resolution and recovery after a failure.

Audit records should identify the actor, action, timestamp, relevant record ID, and reason where appropriate. Access should be restricted to authorized users.

Only necessary information should be collected and retained. Real student resumes and personal records must not be used in synthetic testing.

These controls are requirements for the proposed design; their presence in the current application has not been independently verified.

## 6. Proposed AI Extension: Company-Specific Resume Matching

A future extension could compare a student's resume with a specific job description and provide explainable suggestions.

### Proposed steps

1. Obtain the student's consent before processing the resume.
2. Extract resume text and allow the student to correct extraction errors.
3. Identify required and preferred skills from the job description.
4. Compare the requirements against evidence actually present in the resume.
5. Explain matched requirements, missing evidence, and possible improvements.
6. Allow the student to review suggestions before making changes.

### Responsible use

- Do not invent skills, qualifications, or work experience.
- Do not guarantee an ATS score or interview outcome.
- Do not automatically reject a student based on an AI-generated score.
- Evaluate accuracy, consistency, and potential bias.
- Restrict access to resumes and avoid unnecessary retention.
- Keep human review available for consequential decisions.

AI should be used only if it provides a measurable benefit over simpler rules or a checklist. Basic validation, duplicate detection, status tracking, and approval workflows can generally begin with ordinary software and deterministic rules.

The AI extension is outside the core workflow scope and has not been validated.

## 7. Evaluation Measures

If permission is granted and a pilot becomes possible, collect comparable baseline and pilot measurements for:

- Staff handling time per opportunity or request.
- Frequency and duration of rework.
- Time taken to resolve student questions.
- Percentage of applications with clearly defined statuses.
- Notification failures and exception frequency.
- Additional review and support effort.
- Staff and student feedback.

Use the same definitions and comparable samples when evaluating before-and-after performance.

No measured improvement or return on investment is currently claimed.

## 8. Acceptance Criteria

The proposed workflow should be considered ready for a limited, authorized pilot only when:

1. The actual workflow and staff responsibilities have been validated with permission.
2. Required fields and publication approvals are defined.
3. Application statuses accurately represent the available evidence.
4. Access controls, auditability, and fallback procedures are specified and tested.
5. Synthetic acceptance scenarios pass in a safe test environment.
6. Baseline measurements and a method for assessing additional workload are available.
7. Privacy and operational risks have been reviewed.

## 9. Current Limitations

Permission to investigate the institutional process has not been received. No direct walkthrough, institutional observation, timing study, or real-record review has been conducted.

The current workflow remains hypothetical. The proposed workflow is a design recommendation, not a verified description of the institution's practices or the application's implemented capabilities.

If permission is declined, the assessment must remain a hypothetical analysis and must not present invented observations or test results as evidence.
