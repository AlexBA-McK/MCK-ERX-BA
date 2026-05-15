# Skill: Extract Requirements

## Purpose
Extract and classify requirements from unstructured text such as meeting notes, emails, workshop outputs, or stakeholder descriptions.

## Inputs
- Unstructured text containing requirements (implicit or explicit)
- Document type hint (optional) — e.g. meeting notes, email thread, workshop output

## Outputs
- A numbered list of extracted requirements, each classified as Functional (FR) or Non-Functional (NFR)
- Confidence indicator: High (explicitly stated), Medium (strongly implied), Low (inferred)

## Usage

### Standalone
Prefix your prompt with the instruction block below, then provide the source text.

### Within an Agent
Include the instruction block in the agent's `instructions.md` as a processing step.

---

## Instruction Block

```
Extract all requirements from the text provided. For each requirement:
1. Assign a sequential ID (FR-001 for functional, NFR-001 for non-functional).
2. Write the requirement as a clear, atomic statement in the format: "The system shall [action]" or "The system must [action]".
3. Classify it as Functional (FR) or Non-Functional (NFR).
4. Assign a confidence level: High (explicitly stated), Medium (strongly implied), Low (inferred from context).
5. Note the source snippet that led to this requirement.

Output as a Markdown table with columns: ID | Type | Requirement Statement | Confidence | Source Snippet.

After the table, list any statements you could NOT classify as requirements and explain why.
```
