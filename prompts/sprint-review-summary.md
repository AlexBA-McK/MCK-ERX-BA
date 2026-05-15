<!--
Purpose:    Generate a structured sprint review summary from rough sprint notes, completed stories, and demo highlights.
Placeholders:
  {{sprint_number}}       - Sprint number or name (e.g. Sprint 12)
  {{sprint_dates}}        - Start and end dates of the sprint
  {{team_name}}           - Team or squad name
  {{sprint_goal}}         - The stated sprint goal
  {{completed_stories}}   - List of completed user stories (IDs and titles)
  {{incomplete_stories}}  - Stories that were not completed and why
  {{demo_highlights}}     - Key items demonstrated in the sprint review
  {{stakeholder_feedback}} - Summary of feedback received during the review (write "None captured" if none)
Usage: Fill in all placeholders and submit as a single message in Copilot Chat or your LLM tool.
-->

I am a Business Analyst preparing a sprint review summary. Please generate a clean, structured summary from the information below.

**Sprint:** {{sprint_number}}
**Dates:** {{sprint_dates}}
**Team:** {{team_name}}
**Sprint Goal:** {{sprint_goal}}

**Completed Stories:**
{{completed_stories}}

**Incomplete Stories:**
{{incomplete_stories}}

**Demo Highlights:**
{{demo_highlights}}

**Stakeholder Feedback:**
{{stakeholder_feedback}}

Please produce a sprint review summary with the following sections:

1. **Sprint Summary** — 2-3 sentence overview of the sprint, whether the goal was met, and overall health
2. **Sprint Goal Assessment** — clearly state whether the sprint goal was achieved (Yes / Partial / No) and why
3. **Completed Work** — table of completed stories with ID, title, and story points (if known)
4. **Incomplete Work** — table of incomplete stories with reason and planned action (carry over / re-prioritize / cancel)
5. **Demo Highlights** — bullet list of key features or fixes demonstrated
6. **Stakeholder Feedback & Actions** — feedback received and any resulting action items
7. **Metrics** — velocity, completion rate, any notable quality indicators (fill in what is known; use TBD for unknowns)
8. **Next Sprint Preview** — brief note on priorities for the next sprint (if known)
