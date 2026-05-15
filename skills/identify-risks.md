# Skill: Identify Risks

## Purpose
Identify risks and assumptions from project artefacts, meeting notes, requirements, or design descriptions.

## Inputs
- Any project artefact: requirements document, design, meeting notes, epic description, etc.
- Optional: risk categories to focus on (e.g. regulatory, integration, data, timeline)

## Outputs
- A risk register table with each risk rated by likelihood and impact
- A separate list of identified assumptions with validation guidance

## Usage

### Standalone
Prefix your prompt with the instruction block below, then provide the source artefact.

### Within an Agent
Include the instruction block in agents that require risk surfacing, such as `document-analyzer`, `epics-analyzer`, or `roadmap-creator`.

---

## Instruction Block

```
Identify all risks and assumptions in the provided content. Follow these rules:

**For Risks:**
1. Assign a sequential Risk ID (R-001, R-002, etc.).
2. Describe the risk: what could go wrong and what would be the consequence.
3. Assign Likelihood: High / Medium / Low.
4. Assign Impact: High / Medium / Low.
5. Classify the risk category: Regulatory / Technical / Integration / Data / Timeline / Resource / Stakeholder / Other.
6. Suggest a mitigation action.

Output risks as a Markdown table: Risk ID | Description | Likelihood | Impact | Category | Mitigation.

**For Assumptions:**
1. Assign a sequential Assumption ID (A-001, A-002, etc.).
2. State the assumption clearly.
3. Describe the consequence if the assumption is wrong.
4. Recommend how to validate the assumption.

Output assumptions as a Markdown table: Assumption ID | Assumption | Consequence if Wrong | Validation Action.

After both tables, provide a short overall risk summary (2-3 sentences).
```
