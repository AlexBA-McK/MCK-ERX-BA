# User Story Creator

## Purpose

Transforms high-level requirements, epic descriptions, or feature requests into well-formed, consistently structured user stories with acceptance criteria. Follows the standard "As a… I want… So that…" format.

## Inputs

| Input | Required | Description |
|---|---|---|
| Requirement or feature description | ✅ Yes | The requirement, feature request, or epic excerpt to decompose |
| Persona / user role | ⬜ Optional | The user role(s) the stories should be written for (defaults to inferred from context) |
| Acceptance criteria style | ⬜ Optional | Preferred style: Given/When/Then (BDD) or bullet-point list |
| Story sizing | ⬜ Optional | Whether to include story point estimates or T-shirt sizes |

## Outputs

One or more user stories in Markdown, each containing:
- **Story Title**
- **User Story Statement** — *As a [persona], I want [capability], so that [benefit]*
- **Acceptance Criteria** — in the specified style (BDD or bullet-point)
- **Out of Scope** — what this story explicitly does not cover
- **Dependencies** — other stories or components this story relies on
- **Notes / Open Questions**

## Usage

1. Copy the contents of [`instructions.md`](instructions.md).
2. Paste into Copilot Chat (or your LLM tool) as the first message.
3. Provide the requirement text and any persona or format preferences.
4. Iterate: ask the agent to *"split this story further"* or *"add edge-case acceptance criteria"*.
5. Copy finalized stories into your backlog tool (e.g. Jira, Azure DevOps).

## Example

See [`example-input.md`](example-input.md) and [`example-output.md`](example-output.md) for a worked example.
