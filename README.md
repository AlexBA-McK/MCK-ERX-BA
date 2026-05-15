# MCK-ERX-BA

Shared artifacts — agents, prompts, and skills — to be reused by Business Analysts and Product Owners on the EPAM-McKesson eRx project team.

---

## Overview

This repository is the central library of reusable AI-assisted tooling for the eRx BA/PO discipline. It provides:

- **Agents** — purpose-built AI agents that automate common BA/PO tasks (e.g. turning meeting transcripts into structured notes, generating user stories from requirements).
- **Prompts** — reusable prompt templates that can be composed into agents or used directly in Copilot Chat / other LLM tooling.
- **Skills** — modular skill definitions that agents can reference to perform specific analytical or generative tasks.

The goal is to reduce repetitive work, ensure consistency across the team, and continuously improve our AI-assisted delivery practices.

---

## Repository Structure

```
MCK-ERX-BA/
├── README.md                          ← This file
├── CONTRIBUTING.md                    ← How to add or update artifacts
│
├── agents/                            ← Agent definitions
│   ├── README.md                      ← Agent catalogue & usage guide
│   ├── meeting-notes-creator/         ← Meeting transcript → structured notes
│   ├── document-analyzer/             ← BRDs, PRDs, specs analysis
│   ├── epics-analyzer/                ← Epic breakdown & analysis
│   ├── user-story-creator/            ← Requirements → user stories
│   ├── traceability-matrix-creator/   ← Requirements traceability
│   └── roadmap-creator/               ← Product roadmap generator
│
├── prompts/                           ← Reusable prompt templates
│   └── README.md
│
└── skills/                            ← Reusable skill definitions
    └── README.md
```

---

## Getting Started

### Prerequisites

- Access to GitHub Copilot (Chat or Agent mode) **or** any OpenAI-compatible LLM interface.
- Familiarity with the eRx domain and standard BA/PO artefact types.

### Using an Agent

1. Navigate to the relevant folder under `agents/` (e.g. `agents/meeting-notes-creator/`).
2. Open the agent's `README.md` to read its purpose, inputs, and outputs.
3. Copy the contents of the agent's instruction file (e.g. `agent.md` or `instructions.md`) into your Copilot Chat prompt, or use it as a custom agent definition in your IDE extension.
4. Provide the required input (e.g. paste a meeting transcript) and run.

### Using a Prompt Template

1. Browse `prompts/` and find the template that matches your need.
2. Fill in the `{{placeholder}}` variables described in the template.
3. Submit the completed prompt in Copilot Chat or your preferred LLM tool.

### Using a Skill

Skills are modular building blocks that agents reference internally. You can also call a skill directly:

1. Open the skill file in `skills/`.
2. Follow the usage instructions in the file header.
3. Combine multiple skills in a single prompt when needed.

---

## Agent Catalogue

| Agent | Purpose |
|---|---|
| [meeting-notes-creator](agents/meeting-notes-creator/) | Converts raw meeting transcripts into structured, shareable meeting notes |
| [document-analyzer](agents/document-analyzer/) | Analyzes BRDs, PRDs, and specification documents to extract key information |
| [epics-analyzer](agents/epics-analyzer/) | Breaks down and analyzes epics to identify scope, dependencies, and risks |
| [user-story-creator](agents/user-story-creator/) | Transforms high-level requirements into well-formed user stories |
| [traceability-matrix-creator](agents/traceability-matrix-creator/) | Generates requirements traceability matrices from source artefacts |
| [roadmap-creator](agents/roadmap-creator/) | Produces structured product roadmaps from epics and priorities |

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on adding new agents, prompts, or skills, and for the review process.

---

## Team

EPAM-McKesson eRx BA/PO team. Questions? Open an issue or reach out in the project Slack channel.
