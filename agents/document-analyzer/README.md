# Document Analyzer

Analyzes Business Requirements Documents (BRDs), Product Requirements Documents (PRDs), technical specifications, and other project artifacts for completeness, clarity, consistency, and potential gaps.

---

## Description

This agent reviews BA/PO documentation and provides a structured analysis report. It identifies missing sections, ambiguous or untestable requirements, internal inconsistencies, and areas where additional stakeholder input is needed. It is particularly tuned for healthcare/pharmacy domain documents on the ERX platform.

---

## Inputs

| Input | Description |
|---|---|
| **Document text** | The full or partial text of the BRD, PRD, or spec |
| **Document type** *(optional)* | E.g., "BRD", "PRD", "Technical Spec", "API Spec" |
| **Review focus** *(optional)* | Specific areas to prioritize (e.g., "focus on acceptance criteria" or "check for regulatory requirements") |

---

## Outputs

A structured analysis report containing:
- **Document Summary** — brief overview of what the document covers
- **Completeness Assessment** — which standard sections are present vs. missing
- **Requirement Quality Issues** — ambiguous, untestable, or conflicting requirements
- **Gaps & Open Questions** — missing information that must be resolved
- **Assumptions & Dependencies** — flagged assumptions and undocumented dependencies
- **Recommendations** — prioritized list of suggested improvements

---

## Usage Example

**Input:**
```
Document Type: BRD
Document: ERX Prior Authorization Flow

1. Introduction
The system shall support prior authorization (PA) for specialty medications.

2. Requirements
- The system must submit PA requests to payers.
- Payers will respond within some timeframe.
- Users should be notified.
```

**Output:**
```markdown
## Document Analysis Report — ERX Prior Authorization Flow
**Type:** BRD

### Document Summary
Describes requirements for submitting and receiving prior authorization responses for specialty medications.

### Completeness Assessment
| Section | Status |
|---|---|
| Business Objective | ❌ Missing |
| Stakeholders | ❌ Missing |
| Functional Requirements | ⚠️ Partial |
| Non-Functional Requirements | ❌ Missing |
| Acceptance Criteria | ❌ Missing |
| Assumptions & Constraints | ❌ Missing |

### Requirement Quality Issues
- "Payers will respond within some timeframe" — vague; no SLA defined. Recommend specifying a numeric SLA (e.g., 72 hours).
- "Users should be notified" — untestable; who are the users? What notification channel? What triggers it?

### Gaps & Open Questions
1. What payer integration methods are supported (API, fax, portal)?
2. What happens if a PA is denied? Is appeal flow in scope?
3. Are there regulatory deadlines (e.g., CMS mandates) that govern PA response times?

### Assumptions & Dependencies
- Assumes payer connectivity infrastructure is already in place.
- Dependency on payer API availability not documented.

### Recommendations
1. Add a Business Objective section explaining the problem being solved.
2. Define SLAs for PA response times.
3. Specify notification recipients, channels, and triggers.
4. Add acceptance criteria for each requirement.
```

---

## Limitations

- Analysis quality depends on the completeness of the input document.
- The agent does not have access to external standards unless provided in the prompt.
- Domain-specific regulatory requirements (e.g., HIPAA, CMS) are flagged when relevant language is detected but should be verified by a compliance SME.
