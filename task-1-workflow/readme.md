# Task 1: AI-Assisted Mentor–Parent Communication Workflow

**HKAIVERSE × Leanova Assessment**

## 1. Introduction

This task focuses on analyzing a real-world academic communication workflow and proposing how Artificial Intelligence (AI) could make it more structured, efficient, and manageable.

Academic mentors often need to communicate with parents regarding student progress, attendance, academic concerns, and follow-up actions. When these activities are handled manually, they can involve repetitive calls, information collection, record maintenance, and follow-up coordination.

The objective of this task is to examine the existing workflow, identify opportunities for improvement, and design a proposed AI-assisted workflow with appropriate human oversight, privacy safeguards, and measurable evaluation criteria.

The proposed solution builds on concepts from an existing voice-based receptionist project, Receptionist.AI, and explores their potential adaptation to an academic communication setting.

## 2. Problem Statement

Manual communication workflows can create several operational challenges:

- **Repetitive communication:** Mentors may need to make multiple calls and communicate similar types of information.
- **Information management:** Important details and follow-up actions need to be recorded consistently.
- **Follow-up coordination:** Unresolved concerns may require additional communication or action.
- **Limited process visibility:** Without a structured tracking mechanism, it may be difficult to review the status of communication requests.
- **Administrative effort:** Time spent on repetitive coordination can reduce the time available for other mentoring responsibilities.

These are the problem areas considered in the proposed analysis. Their actual frequency and impact would need to be measured during a real institutional study.

## 3. Project Objective

The objective is to design a workflow in which AI assists with routine information handling while mentors retain responsibility for sensitive communication and important decisions.

The proposed workflow aims to:

1. Document the current communication process.
2. Identify repetitive activities that could benefit from automation.
3. Design a structured AI-assisted alternative.
4. Define input requirements, expected outputs, and failure-handling procedures.
5. Establish human approval and privacy controls.
6. Estimate potential operational benefits using an illustrative ROI model.
7. Define test scenarios and evaluation criteria for a future prototype.

## 4. Existing Workflow

The working model of the current process follows these stages:

1. **Identify the communication need:** A mentor determines that a parent needs to be contacted.
2. **Prepare information:** Relevant information is collected before the interaction.
3. **Contact the parent:** The mentor communicates by phone or another available channel.
4. **Discuss the concern:** Information is shared and questions are addressed.
5. **Record the outcome:** Important notes or follow-up requirements may be recorded.
6. **Complete follow-up:** Additional action is taken when required.

This process is used as a working description for the assessment. The exact institutional procedure and the time spent at each stage have not been established through formal observation.

## 5. Proposed AI-Assisted Workflow

The proposed workflow introduces structured information processing and AI assistance into the communication process.

### Proposed sequence

1. **Request or case creation:** A communication request is created with the required information.
2. **Information validation:** The system checks whether required fields are present and flags incomplete records.
3. **AI-assisted preparation:** AI can help organize notes, summarize information, or prepare a draft communication.
4. **Human review:** The mentor checks the generated content for accuracy, context, and appropriateness.
5. **Approved communication:** Any consequential message or action proceeds only after the required human approval.
6. **Outcome recording:** The communication status and follow-up requirements are recorded.
7. **Exception handling:** Ambiguous information, low-confidence output, or system failures are routed to a human.

AI is intended to assist with repetitive tasks, not replace the mentor's judgment or independently make consequential decisions about students.

## 6. Related Project: Receptionist.AI

**GitHub repository:** [AnnadataHemanth/receptionist.ai](https://github.com/AnnadataHemanth/receptionist.ai)

Receptionist.AI is an existing voice-based receptionist project developed using Python, FastAPI, Twilio, and database-backed appointment workflows.

The project provides a technical reference for exploring voice interactions, webhook-based communication, structured conversation flows, and information collection.

The mentor–parent communication system described in this task is a proposed adaptation. It should not be interpreted as a claim that the existing Receptionist.AI application already implements the complete academic workflow.

## 7. Technology Context

| Technology | Potential role |
|---|---|
| Python | Application logic and workflow processing |
| FastAPI | Backend APIs and webhook endpoints |
| Twilio | Voice communication integration |
| SQL database | Structured record and status management |
| AI/LLM component | Drafting, summarization, and structured information processing |
| ngrok | Local development and webhook testing |

The exact architecture and AI integration would depend on the implementation selected for a future prototype.

## 8. Evidence and Evaluation Approach

The assessment distinguishes the existing workflow description, proposed changes, and illustrative scenarios.

The proposed evaluation includes:

- A current-workflow description and proposed-workflow design.
- An evidence log that distinguishes available information from assumptions.
- Five synthetic test scenarios covering representative inputs and expected outcomes.
- An illustrative ROI calculator.
- A risk analysis covering privacy, inaccurate AI output, authorization, and system failures.

The synthetic scenarios are intended to define how a prototype could be tested. They are not presented as results from completed live testing.

## 9. Illustrative ROI Analysis

The ROI model demonstrates how the potential value of the proposed workflow could be estimated.

Relevant variables include:

- Number of communication cases per month.
- Average manual handling time per case.
- Time spent on corrections or repeated work.
- Review time required for AI-assisted outputs.
- Percentage of cases requiring escalation.
- Initial development and ongoing support effort.

The calculations use hypothetical inputs to demonstrate the method. They do not establish actual institutional savings, implementation costs, or measured performance improvements.

A real evaluation should compare observed baseline performance with measured prototype performance.

## 10. Risks and Safeguards

| Risk | Proposed safeguard |
|---|---|
| Incorrect AI-generated information | Verify generated content against source records |
| Missing or ambiguous input | Request clarification rather than inventing details |
| Exposure of sensitive information | Minimize data collection and restrict access |
| Unauthorized communication | Require authentication and appropriate approval |
| Service or model failure | Provide a safe error response and manual fallback |
| Unrecorded actions | Maintain appropriate audit logs |
| Overreliance on AI | Keep human review for consequential decisions |

Any real implementation would require suitable institutional permission, privacy protections, access controls, and testing before deployment.

## 11. Expected Outcomes

If developed and validated successfully, the proposed workflow could help:

- Structure communication requests and records.
- Reduce repetitive information preparation.
- Improve consistency in communication drafts.
- Make follow-up requirements easier to track.
- Provide clearer visibility into workflow status.
- Establish measurable criteria for evaluating efficiency and reliability.

These are expected benefits to investigate, not confirmed results.

## 12. Deliverables

The Task 1 report covers:

- Current and proposed workflow analysis.
- Evidence and assumptions log.
- Synthetic test cases and expected outcomes.
- Illustrative ROI calculations.
- Risk assessment and safeguards.
- Proposed implementation and evaluation plan.

## 13. Conclusion

This task explores how an existing voice-receptionist concept could inform the design of an AI-assisted academic communication workflow. The main principle is to combine automation with structured records, appropriate safeguards, and human accountability.

The proposal provides a foundation for future prototyping and evaluation while clearly distinguishing hypothetical analysis from verified operational outcomes.

## Author

**Annadata Hemanth**  
B.Tech in Artificial Intelligence and Data Science  
ICFAI Foundation for Higher Education (IFHE), Hyderabad

**Assessment:** HKAIVERSE × Leanova

