# Skills

This directory contains reusable skill definitions that can be referenced by agents or used standalone.

---

## What is a Skill?

A skill is a modular, focused instruction block that performs one specific analytical or generative task. Skills are the building blocks that agents are composed from.

You can use a skill directly in a prompt, or reference it within a custom agent instruction set.

---

## Skill Catalogue

| Skill | Purpose |
|---|---|
| [extract-requirements.md](extract-requirements.md) | Extract and classify requirements from unstructured text |
| [identify-gaps.md](identify-gaps.md) | Identify gaps in requirements or specifications |
| [generate-acceptance-criteria.md](generate-acceptance-criteria.md) | Generate acceptance criteria for a user story or feature |
| [identify-risks.md](identify-risks.md) | Identify risks and assumptions from project artefacts |
| [prioritize-backlog.md](prioritize-backlog.md) | Apply MoSCoW or WSJF prioritization to a backlog |

---

## How to Use a Skill

### Standalone
1. Open the skill file and copy the instruction block.
2. Prefix your prompt with the skill instructions.
3. Provide the input content and submit.

### Within an Agent
Reference the skill by including its instruction block in the agent's `instructions.md`. Skills compose naturally — include multiple skill blocks in sequence for multi-step processing.

---

## Adding a New Skill

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines on adding skills.
