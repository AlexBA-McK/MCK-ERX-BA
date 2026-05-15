# Roadmap Creator

Generates structured product roadmaps from epics, business priorities, and release goals.

---

## Description

This agent takes a list of epics, features, or initiatives along with business priorities and produces a formatted product roadmap. It organizes work into time horizons (quarters, sprints, or named releases), highlights dependencies, and surfaces items that need prioritization decisions.

---

## Inputs

| Input | Description |
|---|---|
| **Epics / initiatives list** | Titles and brief descriptions of the work items to place on the roadmap |
| **Business priorities** *(optional)* | Strategic goals or OKRs that drive prioritization |
| **Time horizon** *(optional)* | Planning period (e.g., "Q3–Q4 2026", "Next 3 sprints", "6-month roadmap") |
| **Constraints** *(optional)* | Team capacity, dependencies, or fixed dates/deadlines |

---

## Outputs

A structured roadmap containing:
- **Roadmap Overview** — summary of the planning period and key themes
- **Roadmap Table** — epics/features organized by time period with priority, status, and dependencies
- **Key Themes** — strategic themes grouping related initiatives
- **Dependencies & Risks** — sequencing dependencies and flagged risks
- **Open Prioritization Decisions** — items needing stakeholder input before they can be placed

---

## Usage Example

**Input:**
```
Time Horizon: Q3–Q4 2026
Business Priorities: Improve PA turnaround time, expand pharmacy network, reduce manual interventions

Epics:
1. Prior Authorization Automation — automate PA submission and tracking
2. Pharmacy Onboarding Portal — self-service portal for new pharmacies
3. Real-Time Eligibility Check — integrate real-time insurance eligibility API
4. Prescriber Dashboard — unified view for prescribers to track Rx status
5. Audit & Compliance Reporting — automated compliance reports for regulators

Constraints:
- Team capacity: 2 squads (6 devs each)
- Real-Time Eligibility depends on insurance carrier API availability (external dependency)
```

**Output:**
```markdown
## Product Roadmap — ERX Platform
**Period:** Q3–Q4 2026

### Roadmap Overview
Two squads focused on reducing manual interventions and expanding platform reach. PA Automation and Real-Time Eligibility are highest priority; Prescriber Dashboard deferred to Q4 pending PA Automation completion.

### Roadmap

| Initiative | Priority | Q3 2026 | Q4 2026 | Squad | Dependencies | Status |
|---|---|---|---|---|---|---|
| PA Automation | 🔴 High | ✅ In Progress | — | Squad A | None | Active |
| Real-Time Eligibility | 🔴 High | 🔲 Planned | — | Squad B | External: Carrier API | Blocked |
| Pharmacy Onboarding Portal | 🟡 Medium | — | 🔲 Planned | Squad A | PA Automation | Queued |
| Audit & Compliance Reporting | 🟡 Medium | — | 🔲 Planned | Squad B | None | Queued |
| Prescriber Dashboard | 🟢 Low | — | 🔲 Planned | TBD | PA Automation | Queued |

### Key Themes
- **Automation & Efficiency**: PA Automation, Real-Time Eligibility
- **Platform Growth**: Pharmacy Onboarding Portal
- **Compliance**: Audit & Compliance Reporting

### Dependencies & Risks
- Real-Time Eligibility is blocked by external carrier API readiness. Risk: may slip to Q4.
- Pharmacy Onboarding Portal and Prescriber Dashboard both depend on PA Automation completing in Q3.

### Open Prioritization Decisions
1. If Real-Time Eligibility is delayed past Q3, should Squad B pick up Prescriber Dashboard instead?
2. Prescriber Dashboard squad assignment is TBD — confirm resource allocation.
```

---

## Limitations

- The agent does not have access to your project management tools (Jira, Azure DevOps, etc.) and cannot pull live backlog data.
- Capacity estimates are illustrative and should be validated against actual team velocity.
- Sequencing recommendations are based on the dependencies and priorities provided; final decisions remain with the PO and stakeholders.
