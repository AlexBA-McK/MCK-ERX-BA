# Epics Analyzer

## Purpose

Breaks down and analyzes product epics to identify scope, feature boundaries, dependencies, risks, and sizing guidance. Helps BA/PO teams assess epics before sprint planning and roadmap commitments.

## Inputs

| Input | Required | Description |
|---|---|---|
| Epic title & description | ✅ Yes | The epic name and its full description or acceptance criteria |
| Related context | ⬜ Optional | Links to related epics, stories, or documents for cross-reference |
| Constraints | ⬜ Optional | Known technical, regulatory, or timeline constraints |

## Outputs

A structured Markdown analysis containing:
- **Epic Summary** — concise restatement of the epic
- **Scope** — what is included and explicitly excluded
- **Key Features / Capabilities** — breakdown of deliverables within the epic
- **Dependencies** — upstream and downstream dependencies on other epics or systems
- **Risks & Assumptions**
- **Suggested User Stories** — high-level story candidates to be refined further
- **Sizing Estimate** — rough T-shirt size (S / M / L / XL) with rationale
- **Open Questions** — items requiring stakeholder clarification

## Usage

1. Copy the contents of [`instructions.md`](instructions.md).
2. Paste into Copilot Chat (or your LLM tool) as the first message.
3. Provide the epic title, description, and any relevant context.
4. Use the output in backlog refinement, PI planning, or roadmap discussions.

## Example

See [`example-input.md`](example-input.md) and [`example-output.md`](example-output.md) for a worked example.
