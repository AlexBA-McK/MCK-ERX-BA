# MCK-ERX-BA

Shared artifacts — agents, prompts, and skills — reusable by Business Analysts and Product Owners on the EPAM-McKesson ERX project team.

---

## Overview

This repository is a central library of GitHub Copilot-compatible artifacts designed to accelerate BA/PO workflows on the McKesson ERX project. It provides:

- **Agents** — purpose-built AI agents for common BA/PO tasks (meeting notes, document analysis, story creation, etc.)
- **Prompts** — reusable prompt templates for recurring analysis and documentation tasks
- **Skills** — modular skill definitions that can be composed into agents or used standalone

---

## Repository Structure

```
MCK-ERX-BA/
├── agents/                          # Agent definitions
│   ├── README.md                    # Agent directory overview and usage guide
│   ├── meeting-notes-creator/       # Meeting transcript → structured notes
│   ├── document-analyzer/           # BRDs, PRDs, and spec analysis
│   ├── epics-analyzer/              # Epic breakdown and analysis
│   ├── user-story-creator/          # Requirements → user stories
│   ├── traceability-matrix-creator/ # Requirements traceability matrix
│   └── roadmap-creator/             # Product roadmap generator
├── prompts/                         # Reusable prompt templates
│   └── README.md
├── skills/                          # Reusable skill definitions
│   └── README.md
├── CONTRIBUTING.md                  # Guidelines for adding/updating artifacts
└── README.md                        # This file
```

---

## Quick Start

### Using an Agent

1. Navigate to the relevant agent directory under `agents/`.
2. Open the agent's `agent.md` (or `.yml`) definition file.
3. Copy the agent definition into your GitHub Copilot Chat or compatible AI assistant.
4. Follow the agent's usage instructions and provide the required inputs.

### Using a Prompt Template

1. Browse the `prompts/` directory for a template matching your task.
2. Copy the prompt, fill in the `{{placeholder}}` variables with your context.
3. Paste into your AI assistant or use it inside an agent workflow.

### Using a Skill

1. Browse the `skills/` directory for relevant skill definitions.
2. Reference or embed the skill in an agent definition or use it directly in a prompt.

---

## Available Agents

| Agent | Description |
|---|---|
| [meeting-notes-creator](./agents/meeting-notes-creator/) | Analyzes meeting transcripts and produces structured, actionable notes |
| [document-analyzer](./agents/document-analyzer/) | Reviews BRDs, PRDs, and technical specs for completeness and gaps |
| [epics-analyzer](./agents/epics-analyzer/) | Breaks down epics, identifies dependencies and missing acceptance criteria |
| [user-story-creator](./agents/user-story-creator/) | Converts requirements into well-formed user stories with acceptance criteria |
| [traceability-matrix-creator](./agents/traceability-matrix-creator/) | Generates requirements traceability matrices from project artifacts |
| [roadmap-creator](./agents/roadmap-creator/) | Produces structured product roadmaps from epics and business priorities |

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines on adding new agents, prompts, and skills, as well as naming conventions and review expectations.

---

## Team

EPAM-McKesson ERX BA/PO Team

