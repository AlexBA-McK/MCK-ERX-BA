# Skill: Prioritize Backlog

## Purpose
Apply a structured prioritization framework (MoSCoW or WSJF) to a backlog of epics, features, or user stories.

## Inputs
- A list of backlog items (titles and brief descriptions are sufficient)
- Prioritization framework: MoSCoW (default) or WSJF
- Optional: business context, constraints, or goals to inform prioritization

## Outputs
- A prioritized backlog table with rationale for each item's priority
- A summary of the prioritization logic applied

## Usage

### Standalone
Prefix your prompt with the instruction block below, then provide the backlog items.

### Within an Agent
Include the instruction block in the `roadmap-creator` agent or any planning-focused agent.

---

## Instruction Block (MoSCoW)

```
Prioritize the provided backlog items using the MoSCoW framework:
- **Must Have** — critical for the current delivery; failure to include means the solution fails
- **Should Have** — important but not vital; significant value, painful to leave out
- **Could Have** — desirable but not necessary; included if time and resources allow
- **Won't Have (this time)** — agreed to be out of scope for the current delivery cycle

For each item:
1. Assign a MoSCoW priority.
2. Provide a 1-2 sentence rationale referencing business value, risk, or dependency.
3. Flag any items where you need more information to prioritize confidently — mark these as *(Needs Clarification)*.

Output as a Markdown table: Item | Priority | Rationale.
Sort the table: Must Have first, then Should Have, Could Have, Won't Have.

After the table, provide a summary paragraph explaining the overall prioritization logic and any key trade-offs.
```

---

## Instruction Block (WSJF)

```
Prioritize the provided backlog items using Weighted Shortest Job First (WSJF).
WSJF Score = Cost of Delay / Job Size
Cost of Delay = User/Business Value + Time Criticality + Risk Reduction/Opportunity Enablement

For each item, estimate on a Fibonacci scale (1, 2, 3, 5, 8, 13):
1. User/Business Value — how much value does this deliver to users or the business?
2. Time Criticality — how much does delaying this cost over time?
3. Risk Reduction / Opportunity Enablement — does this reduce risk or unlock other value?
4. Job Size — relative effort required (higher = more effort)

Calculate: WSJF = (Value + Time Criticality + Risk/Opportunity) / Job Size

Output as a Markdown table: Item | Value | Time Criticality | Risk/OE | Job Size | WSJF Score.
Sort by WSJF Score descending (highest priority first).

After the table, provide a summary of the top 5 priorities and the key factors that drove their ranking.
```
