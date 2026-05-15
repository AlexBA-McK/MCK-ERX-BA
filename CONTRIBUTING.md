# Contributing to MCK-ERX-BA

Thank you for helping improve the shared BA/PO artifact library for the EPAM-McKesson eRx project. This guide explains how to add or update agents, prompts, and skills.

---

## Table of Contents

1. [General Principles](#general-principles)
2. [Adding a New Agent](#adding-a-new-agent)
3. [Adding a New Prompt Template](#adding-a-new-prompt-template)
4. [Adding a New Skill](#adding-a-new-skill)
5. [Updating Existing Artifacts](#updating-existing-artifacts)
6. [Pull Request Process](#pull-request-process)
7. [Naming Conventions](#naming-conventions)

---

## General Principles

- **Reusability first** — artifacts should be generic enough to be used across different meetings, documents, or requirements, not hard-coded to one session.
- **Clear documentation** — every artifact must have a `README.md` explaining its purpose, inputs, outputs, and usage example.
- **Incremental improvement** — prefer small, focused pull requests over large rewrites.
- **Tested before merging** — run the artifact against at least one real or representative input before opening a PR.

---

## Adding a New Agent

1. Create a new folder under `agents/` using kebab-case naming (e.g. `agents/my-new-agent/`).
2. Inside the folder, create the following files:

   | File | Purpose |
   |---|---|
   | `README.md` | Description, inputs, outputs, usage example |
   | `instructions.md` | The full agent instruction/system prompt |
   | `example-input.md` *(optional)* | A sample input to demonstrate the agent |
   | `example-output.md` *(optional)* | The expected output for the sample input |

3. Update the Agent Catalogue table in the root [`README.md`](README.md).
4. Update [`agents/README.md`](agents/README.md) with an entry for the new agent.

### Agent `README.md` Template

```markdown
# <Agent Name>

## Purpose
One or two sentences describing what this agent does.

## Inputs
- **Required:** description of required input(s)
- **Optional:** description of optional input(s)

## Outputs
Description of what the agent produces.

## Usage
Step-by-step instructions for using the agent.

## Example
Brief example or link to example-input.md / example-output.md.
```

---

## Adding a New Prompt Template

1. Create a new `.md` file under `prompts/` using kebab-case naming (e.g. `prompts/stakeholder-interview.md`).
2. Use `{{placeholder}}` syntax for variable parts.
3. Include a header comment block documenting:
   - **Purpose** — what the prompt achieves
   - **Placeholders** — list and describe each `{{placeholder}}`
   - **Usage** — how to use the prompt

4. Update [`prompts/README.md`](prompts/README.md) with an entry for the new template.

---

## Adding a New Skill

1. Create a new `.md` file under `skills/` using kebab-case naming (e.g. `skills/gap-analysis.md`).
2. Include a header block describing:
   - **Purpose** — what this skill does
   - **Inputs** — what it expects
   - **Outputs** — what it produces
   - **Usage** — how to invoke it (standalone or within an agent)
3. Update [`skills/README.md`](skills/README.md) with an entry for the new skill.

---

## Updating Existing Artifacts

- Always update the artifact's own `README.md` to reflect the change.
- If the change affects the root `README.md` catalogue, update that too.
- For breaking changes (different input/output format), bump the version in the file header and note what changed.

---

## Pull Request Process

1. Branch off `main` using a descriptive branch name (e.g. `add-roadmap-creator-agent` or `update-user-story-prompt`).
2. Open a pull request with a clear title and description explaining:
   - What artifact was added or changed.
   - Why it was needed.
   - How you tested it.
3. Request a review from at least one other BA/PO team member.
4. Address any review comments before merging.
5. Squash-merge into `main` once approved.

---

## Naming Conventions

| Artifact | Convention | Example |
|---|---|---|
| Agent folder | kebab-case | `meeting-notes-creator` |
| Prompt file | kebab-case `.md` | `stakeholder-interview.md` |
| Skill file | kebab-case `.md` | `gap-analysis.md` |
| Placeholders | `{{snake_case}}` | `{{meeting_date}}` |
| Branch names | `verb-noun-artifact` | `add-epics-analyzer-agent` |

---

Questions? Open a GitHub issue or reach out on the project Slack channel.
