# Summarize Document

## Purpose
Produce a structured, concise summary of any project document, capturing purpose, scope, key content, and open items.

## When to Use
- Inside the `document-analyzer` agent as the first step before detailed analysis
- Standalone when onboarding to a new document or feature area quickly
- When preparing to share a document overview in a meeting or stakeholder update

---

## Skill Definition

```
Read the provided document and produce a structured summary using the following format:

1. **Document Title & Type**: State the document's title (inferred if not stated) and type (BRD, PRD, Technical Spec, Meeting Notes, etc.).

2. **Purpose**: One to two sentences describing what problem or need the document addresses.

3. **Scope**: What is explicitly in scope and, if stated, what is out of scope.

4. **Key Content**: A bullet-point summary of the main sections or findings. Group related points. Use plain language — avoid jargon unless the document defines it.

5. **Stakeholders / Audience**: Who is named as a stakeholder, owner, or intended audience.

6. **Open Items / TBDs**: List any items explicitly marked as TBD, under discussion, or requiring future decisions.

7. **Document Status**: State whether the document appears to be Draft, In Review, or Final, based on any version or status markers. If not stated, note "Status not specified."

Keep the summary concise. Aim for a summary that can be read in under 2 minutes.
Do not add interpretation or analysis beyond what is present in the document.
```

---

## Example

**Input:** *(a BRD excerpt for ERX PA Automation)*

**Output:**
```markdown
## Document Summary

**Title:** ERX Prior Authorization Automation — Business Requirements Document
**Type:** BRD
**Status:** Draft (v0.3)

### Purpose
Defines the business requirements for automating the prior authorization (PA) submission and tracking process for specialty medications on the ERX platform, replacing the current manual fax/phone workflow.

### Scope
**In scope:** Electronic PA submission to payers, real-time status tracking, prescriber notifications, audit logging.
**Out of scope:** PA appeal workflow, integration with pharmacy benefit managers (PBMs).

### Key Content
- Business drivers: reduce PA turnaround time from 5 days (manual) to under 72 hours.
- 12 functional requirements covering submission, status tracking, notifications, and logging.
- Non-functional requirements include 99.9% availability and HIPAA compliance.
- Integration with 3 payer APIs identified; 2 additional payers TBD.

### Stakeholders
- Business Owner: McKesson Specialty Health
- Technical Lead: EPAM Integration Team
- Compliance: McKesson Legal & Compliance

### Open Items / TBDs
- Payer list not finalized (2 of 5 payers TBD).
- SLA for PA response time not yet confirmed with payers.
- Appeal workflow deferred — may be added in a future phase.
```
