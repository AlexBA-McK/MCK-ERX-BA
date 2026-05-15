# Gap Analysis Template

## Purpose
Identify gaps between the current state and desired state in any project artifact, feature, or process.

## When to Use
- Comparing a draft BRD/PRD against a set of business objectives
- Reviewing a feature against acceptance criteria to find what's missing
- Assessing where a current system falls short of a future-state vision

---

## Template

```
You are a senior Business Analyst reviewing the following {{document_type}} for the {{project_name}} project.

Current State:
{{current_state_description}}

Desired State / Business Objective:
{{desired_state_description}}

Please perform a gap analysis and produce a structured report with:
1. A summary of the key differences between the current and desired state.
2. A table of identified gaps, each with: Gap ID, Description, Impact (High/Medium/Low), and Recommended Action.
3. Any assumptions you made in your analysis.
4. A prioritized list of next steps to close the most critical gaps.

Focus area (optional): {{focus_area}}
```

---

## Variables

| Variable | Description |
|---|---|
| `{{document_type}}` | Type of artifact being analyzed (e.g., "BRD", "feature description", "process flow") |
| `{{project_name}}` | Name of the project or product area |
| `{{current_state_description}}` | Description or text of what currently exists |
| `{{desired_state_description}}` | Description of what the business wants or needs |
| `{{focus_area}}` | Optional — specific area to prioritize (e.g., "security requirements", "user notifications") |

---

## Example Output

```markdown
## Gap Analysis Report — ERX Prior Authorization

### Summary
The current PA submission process is entirely manual (fax/phone). The desired state is a fully automated electronic PA workflow integrated with payer APIs. The primary gaps are in automation, real-time status tracking, and prescriber notification.

### Gaps

| Gap ID | Description | Impact | Recommended Action |
|---|---|---|---|
| GAP-001 | No electronic PA submission capability | High | Implement payer API integration for PA submission |
| GAP-002 | No real-time PA status tracking | High | Add status polling and webhook handling |
| GAP-003 | Prescribers not notified of PA decisions | Medium | Add notification workflow for PA approvals/denials |
| GAP-004 | No audit trail for PA submissions | Medium | Implement PA submission logging |

### Assumptions
- Payer API connectivity is technically feasible within the project timeline.
- Regulatory requirements (CMS PA mandates) are in scope.

### Next Steps
1. Validate payer API integration scope with the technical team (GAP-001).
2. Define SLAs for PA status updates (GAP-002).
3. Confirm notification channels with stakeholders (GAP-003).
```
