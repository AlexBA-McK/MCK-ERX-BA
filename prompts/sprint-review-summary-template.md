# Sprint Review Summary Template

## Purpose
Summarize sprint outcomes, completed user stories, carry-over items, and key learnings into a concise sprint review communication.

## When to Use
- Preparing the sprint review presentation for stakeholders
- Creating a written summary after the sprint review meeting
- Producing a record of sprint outcomes for project documentation

---

## Template

```
You are a Business Analyst summarizing the outcomes of a completed sprint for the {{project_name}} project.

Sprint Details:
- Sprint: {{sprint_name_or_number}}
- Sprint Goal: {{sprint_goal}}
- Dates: {{start_date}} to {{end_date}}

Completed Stories:
{{completed_stories}}

Carry-Over / Incomplete Stories:
{{carryover_stories}}

Key Issues or Blockers Encountered:
{{issues_and_blockers}}

Additional Notes (optional):
{{additional_notes}}

Please produce a structured sprint review summary containing:
1. Sprint goal and whether it was achieved (Yes / Partial / No).
2. Summary of completed work grouped by theme or epic.
3. Carry-over items with a brief reason for each.
4. Key issues and blockers encountered, with resolution or next steps.
5. A brief "what went well / what to improve" section.
6. Recommended focus areas for the next sprint.
```

---

## Variables

| Variable | Description |
|---|---|
| `{{project_name}}` | Name of the project or product area |
| `{{sprint_name_or_number}}` | Sprint identifier (e.g., "Sprint 12" or "Sprint - May 5") |
| `{{sprint_goal}}` | The goal set at the start of the sprint |
| `{{start_date}}` | Sprint start date |
| `{{end_date}}` | Sprint end date |
| `{{completed_stories}}` | List of completed story IDs/titles and brief descriptions |
| `{{carryover_stories}}` | List of stories not completed, with reason if known |
| `{{issues_and_blockers}}` | Any blockers, impediments, or issues encountered |
| `{{additional_notes}}` | Any other context (demos, stakeholder feedback, etc.) |

---

## Example Output

```markdown
## Sprint Review Summary — Sprint 12
**Project:** ERX Platform
**Dates:** April 28 – May 9, 2026
**Sprint Goal:** Complete PA Automation core submission flow

### Goal Achievement: ✅ Achieved

### Completed Work
**PA Automation**
- US-041: Submit PA request via API — ✅ Done
- US-042: PA status polling — ✅ Done
- US-043: PA decision webhook handler — ✅ Done

**Bug Fixes**
- BUG-017: Fixed session timeout on pharmacy dashboard — ✅ Done

### Carry-Over Items
| Story | Reason |
|---|---|
| US-044: Prescriber PA notification | External API credentials not available until next sprint |

### Issues & Blockers
- Payer sandbox API was unavailable for 2 days (May 3–4); team pivoted to unit testing. Resolved May 5.

### What Went Well
- Strong collaboration between BA and dev on PA submission edge cases.
- All core PA stories delivered within sprint.

### What to Improve
- Identify external dependencies earlier in sprint planning to avoid mid-sprint blockers.

### Recommended Focus for Next Sprint
- Complete US-044 (prescriber notification) now that API credentials are available.
- Begin pharmacy onboarding portal spike.
```
