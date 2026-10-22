
# Proposed Workflow: Centralized Placement Communication and Tracking

## 1. Objective

Create a consistent workflow for publishing placement opportunities, communicating eligibility criteria, answering student questions, and tracking application status.

The proposal builds on the PlacementHub project concept. This document does not claim that every proposed capability has been implemented or tested.

## 2. Proposed Process

### Step 1: Receive and Validate Opportunity
The placement cell receives company details, job description, eligibility requirements, deadline, and application link.

### Step 2: Publish a Central Opportunity Record
An authorized administrator creates one opportunity record containing the approved details. This becomes the primary reference for students and placement staff.

### Step 3: Communicate Eligibility
The system displays the documented eligibility criteria. If authorized student data is available, the system may assist with preliminary eligibility checks. Exceptions should be reviewed by placement staff.

### Step 4: Notify Students
Students access opportunities through a central dashboard. In-app notifications are the proposed baseline. Email or WhatsApp integrations should only be claimed if implemented and tested.

### Step 5: Track Applications Accurately
For applications handled inside the platform, the system can record the relevant submission status.

For external applications, the system must distinguish between:
- Link opened.
- Student-confirmed application.
- Verified application submission, where a reliable confirmation or authorized integration exists.

Opening a link alone must never be treated as proof that an application was submitted.

### Step 6: Handle Questions
Provide a defined channel for student questions, with a clear process for assigning, answering, and closing queries.

### Step 7: Monitor Progress
Placement staff can review available counts by status and identify cases requiring follow-up.

### Step 8: Manage Changes
Changes to deadlines, eligibility, or opportunity details should be recorded and communicated to affected students.

## 3. Minimum Viable Scope

- Centralized opportunity details.
- Consistent eligibility criteria and deadlines.
- Student-facing opportunity list.
- In-app notifications where supported.
- Clear application-status categories.
- A defined question and follow-up process.
- Aggregate counts that distinguish clicks from confirmed applications.
- Access control and audit records where implemented.

## 4. Proposed AI Extension: Company-Specific Resume Matching

A future extension could compare a student's resume with a specific company's job description.

### Suggested workflow
1. Extract text from an uploaded PDF or DOCX resume.
2. Identify required and preferred skills from the job description.
3. Compare resume evidence against those requirements.
4. Generate an explainable match score using a transparent scoring rubric and semantic matching.
5. Show matched skills, missing evidence, and suggested resume improvements.
6. Allow the student to review the suggestions and correct extraction errors.

### Responsible use
- Do not invent skills, qualifications, or experience.
- Do not treat the score as a guarantee of ATS performance.
- Do not automatically reject students based on the score.
- Obtain appropriate consent before processing resumes.
- Restrict access and avoid unnecessary retention of personal data.
- Evaluate the scoring approach for errors and bias.

This AI extension is a proposal, not a validated feature. It is excluded from the core workflow ROI until separately implemented and evaluated.

## 5. Exception Handling

| Scenario | Proposed response |
|---|---|
| Missing job details | Keep the opportunity in draft or flag it for correction |
| Possible duplicate opportunity | Flag for human review rather than silently deleting |
| Unauthorized edit or publication | Deny the action and log it where supported |
| External application cannot be verified | Keep the status unverified |
| Notification failure | Show the failure and use an approved fallback where available |
| Deadline or eligibility change | Record the change and notify affected students |

## 6. Success Measures

Measure before and after:
- Staff handling time per opportunity or application.
- Rework frequency and time.
- Time taken to answer student questions.
- Percentage of applications with a clear status.
- Notification failures and exceptions.
- Staff and student feedback.

No improvement should be claimed until comparable results have been measured.
