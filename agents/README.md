# Agents

This directory contains purpose-built AI agent definitions for common BA/PO tasks on the EPAM-McKesson eRx project.

---

## What is an Agent?

An agent is a packaged set of instructions (a system prompt) that directs an LLM to perform a specific, repeatable task. Each agent folder contains:

- `README.md` — purpose, inputs, outputs, and usage instructions
- `instructions.md` — the full agent instruction/system prompt to copy into your tool
- `example-input.md` *(where applicable)* — a representative sample input
- `example-output.md` *(where applicable)* — the expected output for the sample input

---

## Agent Catalogue

| Agent | Purpose |
|---|---|
| [meeting-notes-creator](meeting-notes-creator/) | Converts raw meeting transcripts into structured, shareable meeting notes |
| [document-analyzer](document-analyzer/) | Analyzes BRDs, PRDs, and specification documents to extract key information |
| [epics-analyzer](epics-analyzer/) | Breaks down and analyzes epics to identify scope, dependencies, and risks |
| [user-story-creator](user-story-creator/) | Transforms high-level requirements into well-formed user stories |
| [traceability-matrix-creator](traceability-matrix-creator/) | Generates requirements traceability matrices from source artifacts |
| [roadmap-creator](roadmap-creator/) | Produces structured product roadmaps from epics and priorities |

---

## How to Use an Agent

1. Open the agent folder and read its `README.md`.
2. Copy the contents of `instructions.md`.
3. Paste it as the system prompt (or first message) in Copilot Chat, ChatGPT, or your LLM tool of choice.
4. Provide the required input as described in the agent's README.
5. Review and refine the output.

---

## Adding a New Agent

See [CONTRIBUTING.md](../CONTRIBUTING.md) for detailed instructions on adding a new agent.
