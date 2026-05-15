# Roadmap Creator

## Purpose

Produces a structured product roadmap from a prioritized list of epics, themes, or features. Organizes work into time horizons (quarters, sprints, or phases), surfaces dependencies, and generates a shareable roadmap document suitable for stakeholder communication.

## Inputs

| Input | Required | Description |
|---|---|---|
| Epics / features list | ✅ Yes | List of epics or features with names and brief descriptions |
| Priorities | ✅ Yes | Priority ranking or MoSCoW classification for each item |
| Time horizon | ✅ Yes | Planning period (e.g. Q3 2025 – Q2 2026, or 3 sprints) |
| Capacity / team size | ⬜ Optional | Rough team capacity to inform what fits in each period |
| Dependencies | ⬜ Optional | Known dependencies between epics |
| Release milestones | ⬜ Optional | Fixed release dates or milestones to anchor the roadmap |

## Outputs

A structured Markdown roadmap document containing:
- **Roadmap Overview** — goals and planning horizon
- **Roadmap Table** — epics/features mapped to time periods with priority and status
- **Milestone Summary** — key releases or go-live dates
- **Dependency Map** — which items depend on others
- **Risks & Assumptions**
- **Out of Scope** — items deliberately deferred

## Usage

1. Copy the contents of [`instructions.md`](instructions.md).
2. Paste into Copilot Chat (or your LLM tool) as the first message.
3. Provide the epics list, priorities, and time horizon.
4. Optionally add capacity, dependencies, or milestone dates for a more detailed roadmap.
5. Use the output for PI planning, stakeholder reviews, or executive presentations.

## Example

See [`example-input.md`](example-input.md) and [`example-output.md`](example-output.md) for a worked example.
