# Document Analyzer

## Purpose

Analyzes Business Requirements Documents (BRDs), Product Requirements Documents (PRDs), functional specifications, and other structured documents. Extracts key information, identifies gaps, flags ambiguities, and produces a structured summary for BA/PO review.

## Inputs

| Input | Required | Description |
|---|---|---|
| Document content | ✅ Yes | Full text of the BRD, PRD, or specification document |
| Document type | ✅ Yes | Type of document (e.g. BRD, PRD, Functional Spec, User Requirement Spec) |
| Analysis focus | ⬜ Optional | Specific aspects to focus on (e.g. gaps, ambiguities, acceptance criteria completeness) |

## Outputs

A structured Markdown report containing:
- **Document Summary** — title, type, version, purpose
- **Scope** — what is and is not in scope
- **Key Requirements** — numbered list of core functional and non-functional requirements
- **Assumptions & Constraints**
- **Gaps & Missing Information** — items that need clarification
- **Ambiguities** — vague or contradictory statements
- **Risks & Concerns** — potential delivery or compliance risks
- **Recommended Next Steps**

## Usage

1. Copy the contents of [`instructions.md`](instructions.md).
2. Paste into Copilot Chat (or your LLM tool) as the first message.
3. Follow up by pasting or attaching the document content.
4. Optionally specify: *"Focus on gaps in acceptance criteria"* or *"Highlight compliance risks."*
5. Use the output to guide requirement refinement sessions with the team.

## Example

See [`example-input.md`](example-input.md) and [`example-output.md`](example-output.md) for a worked example.
