# Traceability Matrix Creator

## Purpose

Generates a requirements traceability matrix (RTM) from source artifacts (BRDs, user stories, test cases, epics). Maps requirements to their origin, related user stories, test coverage, and implementation status to support compliance, audit, and QA activities.

## Inputs

| Input | Required | Description |
|---|---|---|
| Requirements source | ✅ Yes | BRD, PRD, or list of requirements to trace |
| User stories / backlog items | ⬜ Optional | Existing user stories to map requirements to |
| Test cases | ⬜ Optional | Test case identifiers or descriptions for coverage mapping |
| Traceability direction | ⬜ Optional | Forward (req → story → test) or backward (test → story → req) |

## Outputs

A Markdown traceability matrix table containing columns such as:

| Req ID | Requirement Description | Source Document | User Story / Epic | Test Case(s) | Status | Notes |
|---|---|---|---|---|---|---|

Additional sections:
- **Coverage Summary** — percentage of requirements with linked stories and tests
- **Gaps** — requirements with no linked story or test
- **Orphaned Items** — stories or tests with no linked requirement

## Usage

1. Copy the contents of [`instructions.md`](instructions.md).
2. Paste into Copilot Chat (or your LLM tool) as the first message.
3. Provide the requirements list and any related user stories or test cases.
4. Specify the traceability direction if needed.
5. Export the Markdown table to your project documentation or compliance artifacts.

## Example

See [`example-input.md`](example-input.md) and [`example-output.md`](example-output.md) for a worked example.
