# Epics Analyzer

Breaks down product epics, assesses their completeness, identifies dependencies, and surfaces missing or unclear acceptance criteria.

---

## Description

This agent analyzes one or more epics from your backlog and produces a structured breakdown report. It evaluates whether each epic is well-defined, estimates relative complexity, uncovers hidden dependencies between epics, and flags stories or criteria that need further refinement before sprint planning.

---

## Inputs

| Input | Description |
|---|---|
| **Epic definition(s)** | Text of one or more epics (title, description, and any existing stories) |
| **Project context** *(optional)* | Product area, release goal, or constraints to improve analysis |

---

## Outputs

A structured analysis report containing:
- **Epic Summary** — concise restatement of each epic's goal
- **Breakdown Assessment** — evaluation of how well the epic is decomposed into stories
- **Missing / Incomplete Areas** — gaps in coverage or undefined edge cases
- **Dependencies** — upstream/downstream dependencies between epics or external systems
- **Acceptance Criteria Review** — evaluation of existing criteria; suggestions for missing ones
- **Recommendations** — what needs to be done before the epic is sprint-ready

---

## Usage Example

**Input:**
```
Project: ERX Platform — Q3 Release

Epic 1: Pharmacy Onboarding
Description: Enable new pharmacies to register and onboard to the ERX platform.
Stories:
- As a pharmacy admin, I want to create an account so that I can access the platform.
- As a pharmacy admin, I want to upload my DEA license.
```

**Output:**
```markdown
## Epic Analysis — Pharmacy Onboarding

### Epic Summary
Covers the end-to-end process for a new pharmacy to register, verify credentials, and gain access to the ERX platform.

### Breakdown Assessment
- 2 stories identified. Likely incomplete for a full onboarding flow.
- Missing stories: identity verification, approval workflow, account activation, error handling for rejected documents.

### Missing / Incomplete Areas
- No story for pharmacy admin receiving confirmation after submission.
- No story for internal admin reviewing/approving onboarding requests.
- Edge cases not covered: duplicate registration attempts, expired licenses, unsupported file formats.

### Dependencies
- Depends on: Identity/Auth service, Document Storage service
- Potential blocker: DEA license verification — is there a 3rd-party integration in scope?

### Acceptance Criteria Review
- "Upload DEA license" story has no acceptance criteria defined.
- Suggested criteria: supported file types, max file size, confirmation message on successful upload, error message on failure.

### Recommendations
1. Add stories for the admin approval and pharmacy notification flows.
2. Define acceptance criteria for all existing stories before sprint planning.
3. Clarify DEA verification integration with the technical team.
4. Consider splitting into two sub-epics: Self-Service Registration and Admin Review & Approval.
```

---

## Limitations

- Analysis is based solely on the provided text; the agent has no access to your Jira/Azure DevOps backlog.
- Complexity estimates are qualitative (High/Medium/Low), not story-point estimates.
- Dependencies on external systems are flagged only when mentioned in the epic text or inferable from context.
