# Requirement Clarification Template

## Purpose
Generate a structured list of clarifying questions for ambiguous, incomplete, or unclear requirements before refinement or development begins.

## When to Use
- Preparing for a requirements refinement session with stakeholders
- Reviewing a BRD/PRD before a sprint and identifying blockers
- Onboarding to a new feature area with incomplete documentation

---

## Template

```
You are a senior Business Analyst preparing for a requirements clarification session on the {{project_name}} project.

Review the following requirement(s) and produce a structured list of clarifying questions that must be answered before development can begin.

Requirements:
{{requirements_text}}

For each question, include:
- The specific requirement or statement it relates to
- The question itself
- Why it matters (what risk does it address if left unanswered?)
- The type of stakeholder best positioned to answer it (e.g., Business Owner, Technical Lead, Compliance, End User)

Group questions by category: Functional, Non-Functional, Compliance/Regulatory, Integration, and Data.
```

---

## Variables

| Variable | Description |
|---|---|
| `{{project_name}}` | Name of the project or product area |
| `{{requirements_text}}` | The raw requirement text to be analyzed |

---

## Example Output

```markdown
## Clarifying Questions — ERX Refill Authorization

### Functional
| Requirement | Question | Why It Matters | Ask: |
|---|---|---|---|
| "Users should be notified of refill approval" | Who are the "users" — patient, pharmacist, prescriber, or all three? | Determines notification channels and workflow design | Business Owner |
| "The system must process refill requests automatically" | What criteria determine automatic approval vs. manual review? | Core business rule needed before any automation can be built | Business Owner + Clinical SME |

### Non-Functional
| Requirement | Question | Why It Matters | Ask: |
|---|---|---|---|
| "System must be performant" | What is the acceptable response time for refill processing? (e.g., < 2 seconds) | Without an SLA, this requirement is untestable | Technical Lead |

### Compliance / Regulatory
| Requirement | Question | Why It Matters | Ask: |
|---|---|---|---|
| "System must log all refill attempts" | What is the required retention period for these logs? | HIPAA and state regulations may specify minimum retention | Compliance / Legal |

### Integration
| Requirement | Question | Why It Matters | Ask: |
|---|---|---|---|
| "Integrate with payer systems" | Which payers are in scope for the initial release? | Scoping integration work and API availability timelines | Business Owner + Technical Lead |
```
