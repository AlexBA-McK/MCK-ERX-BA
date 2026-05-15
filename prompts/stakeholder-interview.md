<!--
Purpose:    Generate targeted interview questions for a stakeholder based on their role and the domain area being explored.
Placeholders:
  {{stakeholder_name}}    - Full name of the stakeholder
  {{stakeholder_role}}    - Job title or role (e.g. Pharmacy Director, IT Architect)
  {{domain_area}}         - The subject area or feature being explored (e.g. eRx workflow, medication reconciliation)
  {{project_context}}     - Brief description of the project and its goals
  {{known_pain_points}}   - Any pain points or challenges already known (write "None known" if none)
Usage: Fill in all placeholders and submit as a single message in Copilot Chat or your LLM tool.
-->

I am a Business Analyst preparing for a stakeholder interview. Please generate a structured list of interview questions for the following stakeholder.

**Stakeholder:** {{stakeholder_name}}
**Role:** {{stakeholder_role}}
**Domain Area:** {{domain_area}}
**Project Context:** {{project_context}}
**Known Pain Points:** {{known_pain_points}}

Generate questions across these categories:
1. **Current State** — how they work today, tools they use, and pain points
2. **Goals & Outcomes** — what success looks like from their perspective
3. **Requirements** — what capabilities or changes they need
4. **Constraints** — regulatory, technical, timeline, or resource constraints they are aware of
5. **Risks & Concerns** — what worries them about the proposed change
6. **Stakeholder Influence** — who else should I talk to, and who has decision-making authority

Format the output as numbered questions grouped by category. Include a note after each question explaining *why* it is valuable to ask.
