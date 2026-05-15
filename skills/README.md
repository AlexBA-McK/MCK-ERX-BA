# Skills

This directory contains reusable skill definitions — modular AI instructions that can be embedded into agent definitions or used directly in prompt templates to add specific capabilities.

---

## Available Skills

| File | Purpose |
|---|---|
| [extract-acceptance-criteria.md](./extract-acceptance-criteria.md) | Extract and structure acceptance criteria from unstructured requirements text |
| [identify-dependencies.md](./identify-dependencies.md) | Identify and classify dependencies between epics, stories, or system components |
| [classify-requirements.md](./classify-requirements.md) | Classify requirements as Functional, Non-Functional, or Constraint |
| [summarize-document.md](./summarize-document.md) | Produce a structured summary of any project document |

---

## How to Use a Skill

Skills are modular instruction blocks. You can:

1. **Embed into an agent**: Copy the skill's instruction block into an agent's `agent.md` under its `## Instructions` section.
2. **Use in a prompt**: Paste the skill instruction into any prompt before providing input.
3. **Chain skills**: Combine multiple skill instructions in a single prompt for compound tasks.

---

## Adding a New Skill

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines on adding new skills.
