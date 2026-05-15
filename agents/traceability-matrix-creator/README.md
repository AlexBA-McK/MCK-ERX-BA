# Traceability Matrix Creator

Generates a requirements traceability matrix (RTM) from project artifacts, mapping requirements to their sources, user stories, test cases, and design elements.

---

## Description

This agent takes a set of requirements (from a BRD, PRD, or feature list) and associated artifacts (user stories, test cases, design references) and produces a structured Requirements Traceability Matrix. The RTM ensures every requirement is accounted for and traceable forward to implementation and backward to its business source.

---

## Inputs

| Input | Description |
|---|---|
| **Requirements list** | Numbered or labeled requirements from a BRD, PRD, or spec |
| **User stories** *(optional)* | Story IDs and titles to map to requirements |
| **Test cases** *(optional)* | Test case IDs and descriptions to map to requirements |
| **Design/component references** *(optional)* | References to design artifacts, API specs, or components |

---

## Outputs

A Markdown traceability matrix table with columns for:
- **Requirement ID** — unique identifier for each requirement
- **Requirement Description** — brief description of the requirement
- **Source** — business objective, regulation, or stakeholder it traces back to
- **User Story / Feature** — linked user story ID(s)
- **Test Case(s)** — linked test case ID(s)
- **Design Reference** — related design artifact or component
- **Status** — coverage status: ✅ Covered, ⚠️ Partial, ❌ Not Covered

---

## Usage Example

**Input:**
```
Requirements:
REQ-001: The system shall allow pharmacists to submit prior authorization requests electronically.
REQ-002: The system shall notify prescribers of PA decisions within 24 hours.
REQ-003: The system shall log all PA submission attempts for audit purposes.

User Stories:
US-001: Submit PA request (covers REQ-001)
US-002: Prescriber PA decision notification (covers REQ-002)

Test Cases:
TC-001: Verify PA request submission (covers REQ-001)
TC-002: Verify prescriber notification timing (covers REQ-002)
```

**Output:**
```markdown
## Requirements Traceability Matrix

| Req ID | Requirement | Source | User Story | Test Case | Design Ref | Status |
|---|---|---|---|---|---|---|
| REQ-001 | Pharmacists can submit PA requests electronically | Business Req | US-001 | TC-001 | — | ✅ Covered |
| REQ-002 | Prescribers notified of PA decisions within 24 hrs | SLA Commitment | US-002 | TC-002 | — | ✅ Covered |
| REQ-003 | All PA submission attempts logged for audit | Compliance Req | — | — | — | ❌ Not Covered |

### Coverage Summary
- Total Requirements: 3
- Covered: 2 (67%)
- Partial: 0
- Not Covered: 1 (33%)

### Gaps
- REQ-003 has no user story, test case, or design reference. Action: create a story and test case for audit logging.
```

---

## Limitations

- The agent can only map artifacts you provide; it cannot access your Jira, Azure DevOps, or test management tools.
- If requirement IDs are not provided, the agent will assign them (REQ-001, REQ-002, etc.).
- Coverage status reflects only what is explicitly linked in the input — it does not perform automated coverage analysis.
