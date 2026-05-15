# Skill: Generate Acceptance Criteria

## Purpose
Generate clear, testable acceptance criteria for a user story or feature description using Given/When/Then (BDD) format.

## Inputs
- User story statement (As a / I want / So that)
- Feature description or requirement (if no formal user story exists)
- Optional: edge cases or constraints to include

## Outputs
- A numbered list of Given/When/Then acceptance criteria scenarios
- Coverage of happy path, alternative paths, and error/edge cases

## Usage

### Standalone
Prefix your prompt with the instruction block below, then provide the user story or feature description.

### Within an Agent
Include the instruction block in the `user-story-creator` agent or any agent that produces user stories.

---

## Instruction Block

```
Generate acceptance criteria for the user story or feature description provided. Follow these rules:

1. Write all criteria in Given/When/Then (BDD) format.
2. Cover the happy path (the primary success scenario) first.
3. Add at least two alternative path scenarios (different valid inputs or workflows).
4. Add at least two error/edge case scenarios (invalid inputs, system failures, boundary conditions).
5. Each scenario must be independently testable — avoid compound scenarios that test multiple things at once.
6. Use present tense and active voice.
7. Do not reference implementation details (no mentions of buttons, database fields, or code).

Format each scenario as:

**Scenario N: [Descriptive name]**
- **Given** [precondition or context]
- **When** [action or event]
- **Then** [expected outcome]

After the scenarios, list any assumptions you made and any edge cases that need stakeholder clarification.
```
