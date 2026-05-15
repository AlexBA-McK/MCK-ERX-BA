# Agents

This directory contains purpose-built AI agent definitions for common BA/PO tasks on the McKesson ERX project. Each agent is designed to be used with GitHub Copilot Chat or a compatible AI assistant.

---

## Available Agents

| Agent | Description |
|---|---|
| [meeting-notes-creator](./meeting-notes-creator/) | Analyzes meeting transcripts and produces structured, actionable notes |
| [document-analyzer](./document-analyzer/) | Reviews BRDs, PRDs, and technical specs for completeness and gaps |
| [epics-analyzer](./epics-analyzer/) | Breaks down epics, identifies dependencies and missing acceptance criteria |
| [user-story-creator](./user-story-creator/) | Converts requirements into well-formed user stories with acceptance criteria |
| [traceability-matrix-creator](./traceability-matrix-creator/) | Generates requirements traceability matrices from project artifacts |
| [roadmap-creator](./roadmap-creator/) | Produces structured product roadmaps from epics and business priorities |

---

## How to Use an Agent

1. Open the agent directory and read its `README.md` to understand inputs and outputs.
2. Open `agent.md` and copy its full contents.
3. Paste the contents into GitHub Copilot Chat as a system-level instruction, or use it in your AI assistant's "custom instructions" or "system prompt" field.
4. Provide the required input as described in the agent's README.

---

## Adding a New Agent

See [CONTRIBUTING.md](../CONTRIBUTING.md) for the full guide on adding new agents.
