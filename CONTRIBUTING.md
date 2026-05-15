# Contributing to MCK-ERX-BA

Thank you for contributing to this shared artifact library. This guide covers how to add or update agents, prompts, and skills so the repository stays consistent and easy to use for the whole BA/PO team.

---

## Table of Contents

- [General Guidelines](#general-guidelines)
- [Adding an Agent](#adding-an-agent)
- [Adding a Prompt Template](#adding-a-prompt-template)
- [Adding a Skill](#adding-a-skill)
- [Naming Conventions](#naming-conventions)
- [Review Process](#review-process)

---

## General Guidelines

- Keep artifact definitions **focused and single-purpose**. An agent should do one job well.
- Use clear, plain language. These artifacts are used by people with varying levels of AI/prompt engineering experience.
- Always include a `README.md` in every new directory you create.
- Test your artifact with real or realistic sample inputs before submitting.
- Do not include project-confidential data (PII, client secrets, credentials) in any artifact file.

---

## Adding an Agent

1. **Create a new directory** under `agents/` using the agent's kebab-case name:
   ```
   agents/my-new-agent/
   ```

2. **Create the required files**:

   | File | Purpose |
   |---|---|
   | `README.md` | Human-readable description, inputs, outputs, and usage example |
   | `agent.md` | The agent definition (system prompt, instructions, and behavior rules) |

3. **README.md must include**:
   - A one-line description of what the agent does
   - **Inputs**: what the user must provide
   - **Outputs**: what the agent produces
   - **Usage example**: a short worked example
   - **Limitations / known gaps** (if any)

4. **agent.md structure**:
   ```markdown
   # Agent Name

   ## Role
   Brief description of the agent's purpose and persona.

   ## Instructions
   Step-by-step behavior rules and processing logic.

   ## Input Format
   Description of expected input.

   ## Output Format
   Description of expected output format (tables, bullet points, Markdown sections, etc.).

   ## Constraints
   Any hard rules (e.g., "Do not invent requirements not present in the source material").
   ```

5. **Update** `agents/README.md` to include your new agent in the summary table.

6. **Update** the root `README.md` agent table as well.

---

## Adding a Prompt Template

1. Create a new `.md` file under `prompts/` using a descriptive kebab-case name:
   ```
   prompts/gap-analysis-template.md
   ```

2. **Structure**:
   ```markdown
   # Prompt Title

   ## Purpose
   One-sentence description of what this prompt is for.

   ## When to Use
   Describe the scenario or task this prompt is best suited for.

   ## Template

   \```
   [Prompt text here. Use {{double_braces}} for variables the user must fill in.]
   \```

   ## Variables

   | Variable | Description |
   |---|---|
   | `{{variable_name}}` | What to replace it with |

   ## Example Output
   A short example of the output this prompt typically produces.
   ```

3. **Update** `prompts/README.md` to list the new template.

---

## Adding a Skill

1. Create a new `.md` file under `skills/` using a descriptive kebab-case name:
   ```
   skills/extract-acceptance-criteria.md
   ```

2. **Structure**:
   ```markdown
   # Skill Name

   ## Purpose
   What capability this skill provides.

   ## When to Use
   In which agents or prompts this skill is useful.

   ## Skill Definition

   \```
   [Skill instruction text — can be embedded directly into an agent or prompt]
   \```

   ## Example
   A short example showing the skill applied to sample input.
   ```

3. **Update** `skills/README.md` to list the new skill.

---

## Naming Conventions

| Item | Convention | Example |
|---|---|---|
| Agent directories | `kebab-case` | `user-story-creator` |
| Prompt files | `kebab-case.md` | `gap-analysis-template.md` |
| Skill files | `kebab-case.md` | `extract-acceptance-criteria.md` |
| Placeholder variables in prompts | `{{snake_case}}` | `{{project_name}}` |

---

## Review Process

1. **Branch**: Create a feature branch from `main` using the format `feat/artifact-name` (e.g., `feat/risk-analyzer-agent`).
2. **Pull Request**: Open a PR with a clear title and description explaining what artifact you're adding and why.
3. **Review**: At least one other BA/PO team member must review and approve the PR.
4. **Merge**: Squash-merge into `main` after approval.

### PR Checklist

- [ ] New directory/file follows the naming convention
- [ ] `README.md` is present and complete
- [ ] Root `README.md` updated (if adding an agent)
- [ ] Agent/prompt/skill tested with realistic sample input
- [ ] No confidential or sensitive data included
- [ ] Relevant `README.md` index updated
