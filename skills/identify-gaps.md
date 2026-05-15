# Skill: Identify Gaps

## Purpose
Identify gaps in requirements, specifications, or designs — areas that are missing, incomplete, contradictory, or insufficiently detailed for implementation.

## Inputs
- A requirements document, user story set, specification, or design description
- Optional: a target completeness standard or checklist to measure against

## Outputs
- A numbered list of identified gaps, each with severity and recommended action
- A summary of overall completeness

## Usage

### Standalone
Prefix your prompt with the instruction block below, then provide the document or text to analyze.

### Within an Agent
Include the instruction block in the agent's `instructions.md` as a gap-checking step after requirements extraction.

---

## Instruction Block

```
Analyze the provided content and identify all gaps. A gap is:
- A requirement area that is mentioned but lacks sufficient detail for implementation
- A missing requirement that is implied by context but not explicitly stated
- A contradictory or conflicting statement between two or more requirements
- An assumption that has not been validated or documented

For each gap:
1. Assign a sequential Gap ID (G-001, G-002, etc.).
2. Describe the gap clearly and concisely.
3. Reference the source section or requirement ID it relates to.
4. Rate the severity: Critical (blocks delivery), High (significant risk), Medium (needs resolution before build), Low (minor clarification).
5. Recommend a specific action to close the gap.

Output as a Markdown table with columns: Gap ID | Description | Related To | Severity | Recommended Action.

After the table, provide a one-paragraph overall completeness assessment.
```
