# User Story Creator

Converts requirements, feature descriptions, or business needs into well-formed user stories with acceptance criteria in Gherkin or standard BA format.

---

## Description

This agent takes raw requirements, meeting notes, or feature descriptions as input and produces properly structured user stories following the standard format: *"As a [persona], I want [goal], so that [benefit]."* Each story is accompanied by acceptance criteria and, optionally, relevant notes for the development team.

---

## Inputs

| Input | Description |
|---|---|
| **Requirements / feature description** | Raw text describing what needs to be built or a business need to be met |
| **Persona(s)** *(optional)* | Relevant user roles (e.g., "Pharmacist", "Patient", "Admin") to use in stories |
| **Output format** *(optional)* | "standard" (default) for plain acceptance criteria, or "gherkin" for Given/When/Then format |

---

## Outputs

A set of user stories, each containing:
- **Story ID** (sequential)
- **User Story** statement
- **Acceptance Criteria** (standard or Gherkin)
- **Notes** (edge cases, out-of-scope items, or dependencies to flag for the team)

---

## Usage Example

**Input:**
```
Personas: Pharmacist, System
Feature: When a prescription is received electronically, the pharmacist should be alerted and be able to view it in the queue. If the prescription is incomplete, the system should flag it for review.
Output format: gherkin
```

**Output:**
```markdown
### US-001: View incoming electronic prescription
**As a** Pharmacist,
**I want** to be alerted when a new electronic prescription is received,
**so that** I can promptly review and process it.

**Acceptance Criteria:**
```gherkin
Given a new electronic prescription is received
When the prescription is complete
Then the pharmacist receives a real-time alert
And the prescription appears in the prescription queue

Given a new electronic prescription is received
When the prescription has missing required fields
Then the system flags the prescription as incomplete
And the prescription is placed in the review queue
And the pharmacist is notified of the incomplete prescription
```

**Notes:**
- "Real-time alert" channel (push notification, in-app, email) is not specified — clarify with stakeholders.
- Define which fields constitute a "complete" prescription (e.g., prescriber NPI, drug name, dosage, quantity).
```

---

## Limitations

- Story quality depends on the detail of the input; vague requirements produce vague stories.
- The agent does not assign story points or priority.
- Persona names should be consistent with your project's defined user roles.
