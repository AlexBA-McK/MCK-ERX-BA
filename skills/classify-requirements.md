# Classify Requirements

## Purpose
Classify a list of requirements as Functional, Non-Functional, or Constraint to support structured analysis and documentation.

## When to Use
- Inside the `document-analyzer` agent to categorize requirements in a BRD/PRD
- Standalone when reviewing a mixed-format requirements list before refinement
- When preparing input for a traceability matrix that separates requirement types

---

## Skill Definition

```
For each requirement provided, classify it into one of the following categories:

- **Functional (F)**: Describes what the system must do — a specific behavior, feature, or capability. Example: "The system shall allow users to submit a prescription electronically."

- **Non-Functional (NF)**: Describes how the system must perform — quality attributes such as performance, security, availability, scalability, usability, or compliance. Example: "The system must process prescription submissions within 2 seconds under normal load."

- **Constraint (C)**: Describes a limitation or boundary condition on the system or project — technology choices, regulatory mandates, or business rules that are fixed and non-negotiable. Example: "The system must comply with HIPAA data privacy regulations." or "The system must be built on the existing cloud infrastructure."

For each requirement, output:
| Req ID | Requirement | Type | Rationale |
|---|---|---|---|

If a requirement spans multiple categories, classify it as the primary type and note the secondary type in the Rationale column.
Flag any requirements that are unclear or do not fit cleanly into any category with ⚠️ and a note.
```

---

## Example

**Input:**
```
REQ-001: The system shall allow pharmacists to submit prior authorization requests.
REQ-002: PA submission responses must be returned within 72 hours.
REQ-003: The system must comply with CMS prior authorization interoperability rules.
REQ-004: The system should be easy to use.
```

**Output:**
```markdown
| Req ID | Requirement | Type | Rationale |
|---|---|---|---|
| REQ-001 | Pharmacists can submit PA requests | Functional | Describes a system capability (submit action) |
| REQ-002 | PA responses returned within 72 hours | Non-Functional | Performance/SLA requirement |
| REQ-003 | Must comply with CMS PA interoperability rules | Constraint | Regulatory mandate; non-negotiable |
| REQ-004 | System should be easy to use | ⚠️ Non-Functional | Too vague to be testable — recommend replacing with a specific usability criterion (e.g., task completion rate or SUS score target) |
```
