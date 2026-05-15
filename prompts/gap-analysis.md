<!--
Purpose:    Identify gaps between a described current state and a desired target state, and recommend actions to close them.
Placeholders:
  {{subject_area}}        - The domain or feature area being analyzed (e.g. eRx order workflow)
  {{current_state}}       - Description of how things work today
  {{target_state}}        - Description of the desired future state or requirements
  {{constraints}}         - Known constraints (regulatory, technical, timeline). Write "None known" if none.
Usage: Fill in all placeholders and submit as a single message in Copilot Chat or your LLM tool.
-->

I am a Business Analyst conducting a gap analysis. Please analyze the current state and target state descriptions below and produce a structured gap analysis.

**Subject Area:** {{subject_area}}

**Current State:**
{{current_state}}

**Target State:**
{{target_state}}

**Constraints:**
{{constraints}}

Please produce a gap analysis with the following sections:

1. **Summary** — brief overview of the key differences between current and target state
2. **Gap Table** — a table with columns: Gap ID | Gap Description | Impact (High/Med/Low) | Effort to Close (High/Med/Low) | Recommended Action
3. **Priority Gaps** — the top 3 gaps that should be addressed first and why
4. **Risks** — risks of not closing each gap
5. **Next Steps** — recommended immediate actions for the BA/PO team
