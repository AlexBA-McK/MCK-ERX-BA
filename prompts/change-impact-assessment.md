<!--
Purpose:    Assess the impact of a proposed change on people, processes, systems, and data.
Placeholders:
  {{change_title}}        - Short name for the proposed change
  {{change_description}}  - Full description of what is being changed and why
  {{affected_systems}}    - Systems or integrations affected (write "Unknown" if not yet known)
  {{affected_teams}}      - Teams or roles impacted by the change
  {{constraints}}         - Known constraints (go-live date, regulatory requirements, etc.)
Usage: Fill in all placeholders and submit as a single message in Copilot Chat or your LLM tool.
-->

I am a Business Analyst assessing the impact of a proposed change. Please produce a structured change impact assessment based on the information below.

**Change Title:** {{change_title}}

**Change Description:**
{{change_description}}

**Affected Systems / Integrations:** {{affected_systems}}

**Affected Teams / Roles:** {{affected_teams}}

**Constraints:** {{constraints}}

Please produce a change impact assessment with the following sections:

1. **Change Summary** — one paragraph restating the change and its business driver
2. **Impact Areas** — table with columns: Area | Impact Description | Severity (High/Med/Low) | Affected Stakeholders
   - Include: People & Roles, Processes & Workflows, Systems & Integrations, Data, Compliance & Regulatory
3. **Risks** — risks introduced by the change
4. **Dependencies** — what must be in place before this change can be implemented
5. **Change Readiness** — assessment of how prepared the organization is for this change
6. **Recommended Next Steps** — actions for the BA/PO and project team
