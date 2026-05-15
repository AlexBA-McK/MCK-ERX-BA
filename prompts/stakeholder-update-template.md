# Stakeholder Update Template

## Purpose
Draft clear, concise stakeholder update communications from project status information, tailored to a non-technical audience.

## When to Use
- Weekly or bi-weekly stakeholder status updates
- Escalation communications when there is a risk or blocker
- End-of-milestone communications summarizing progress

---

## Template

```
You are a Business Analyst drafting a stakeholder update for the {{project_name}} project.

Update Details:
- Reporting Period: {{reporting_period}}
- Audience: {{audience}} (e.g., "Executive sponsors", "Product leadership", "McKesson business stakeholders")
- Tone: {{tone}} (e.g., "Formal", "Conversational", "Concise bullet-point")

Current Status: {{overall_status}} (Green / Amber / Red)

Progress This Period:
{{progress_this_period}}

Upcoming Milestones:
{{upcoming_milestones}}

Risks / Issues:
{{risks_and_issues}}

Decisions Needed from Stakeholders (if any):
{{decisions_needed}}

Additional Context (optional):
{{additional_context}}

Please draft a stakeholder update email / document that:
1. Opens with a brief headline summary of status and the most important news.
2. Summarizes progress in plain language (no Jira IDs or technical jargon).
3. Highlights upcoming milestones and their expected dates.
4. Clearly communicates any risks or issues, their impact, and mitigation steps.
5. Makes any required stakeholder decisions explicit and easy to action.
6. Closes with next steps and the date of the next update.

Adapt the level of detail and formality to match the stated audience and tone.
```

---

## Variables

| Variable | Description |
|---|---|
| `{{project_name}}` | Name of the project or product area |
| `{{reporting_period}}` | Period covered by the update (e.g., "Week of May 12, 2026") |
| `{{audience}}` | Who will receive this update |
| `{{tone}}` | Desired communication style |
| `{{overall_status}}` | Green (on track), Amber (at risk), or Red (off track) |
| `{{progress_this_period}}` | Key progress made; completed milestones or deliverables |
| `{{upcoming_milestones}}` | Key upcoming dates and deliverables |
| `{{risks_and_issues}}` | Current risks or blockers and their impact |
| `{{decisions_needed}}` | Any decisions stakeholders need to make |
| `{{additional_context}}` | Any other relevant context or background |

---

## Example Output

```markdown
**Subject:** ERX Platform — Weekly Status Update | Week of May 12, 2026 | 🟡 Amber

Hi team,

**Status: Amber — Payer API dependency at risk of delaying prescriber notification feature.**

---

**Progress This Week**
- PA Automation core submission flow is complete and in QA testing.
- Pharmacy onboarding portal discovery kicked off; first workshop scheduled for May 19.

**Upcoming Milestones**
| Milestone | Expected Date | Status |
|---|---|---|
| PA Automation QA sign-off | May 16, 2026 | On Track |
| Pharmacy Onboarding Portal kick-off workshop | May 19, 2026 | On Track |
| Prescriber Notification feature release | May 30, 2026 | ⚠️ At Risk |

**Risks & Issues**
- **Prescriber Notification (Amber):** Payer API credentials required for the notification flow have not been received. If not resolved by May 16, the May 30 release date is at risk. Mitigation: escalation to payer integration team initiated by the technical lead.

**Decision Needed**
- If payer API credentials are not available by May 16, should we release PA Automation without the prescriber notification feature and deliver notification in a subsequent patch? Please confirm by **May 16**.

**Next Steps**
- QA testing of PA Automation to complete by May 16.
- Escalation on payer API credentials ongoing.
- Next update: May 19, 2026.

Best regards,
[Your name]
```
