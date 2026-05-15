<!--
Purpose:    Review existing acceptance criteria for a user story and improve them for clarity, completeness, and testability.
Placeholders:
  {{story_title}}             - Title of the user story
  {{user_story_statement}}    - The "As a / I want / So that" statement
  {{existing_criteria}}       - The acceptance criteria to be reviewed (paste as-is)
  {{context}}                 - Any additional context about the feature (write "None" if none)
Usage: Fill in all placeholders and submit as a single message in Copilot Chat or your LLM tool.
-->

I am a Business Analyst reviewing acceptance criteria for a user story. Please review the criteria below and produce an improved version.

**Story Title:** {{story_title}}

**User Story:**
{{user_story_statement}}

**Existing Acceptance Criteria:**
{{existing_criteria}}

**Additional Context:**
{{context}}

Please:
1. **Assess** the existing criteria — identify any that are vague, untestable, duplicated, or missing.
2. **Rewrite** each criterion using Given/When/Then (BDD) format.
3. **Add** any missing edge cases, error states, or boundary conditions.
4. **Remove** or merge any duplicate or redundant criteria.
5. **Flag** any criteria that require stakeholder clarification before they can be finalized.

Output the improved criteria as a numbered list of Given/When/Then scenarios, followed by a short list of flagged items.
