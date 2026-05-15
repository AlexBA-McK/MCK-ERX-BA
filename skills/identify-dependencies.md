# Identify Dependencies

## Purpose
Identify and classify dependencies between epics, user stories, or system components from a set of project artifacts.

## When to Use
- Inside the `epics-analyzer` agent to surface sequencing constraints
- Inside the `roadmap-creator` agent to inform placement of epics
- Standalone when reviewing a backlog for hidden dependencies before sprint planning

---

## Skill Definition

```
For the provided list of epics, stories, or system components, identify all dependencies using the following approach:

1. **Internal dependencies**: Identify cases where one item cannot start or complete without another item from the provided list being done first. State the relationship clearly: "[Item A] depends on [Item B] because [reason]."

2. **External dependencies**: Identify cases where an item depends on something outside the provided list (e.g., a third-party API, a vendor, another team, a regulatory approval, or a platform capability not yet built). Classify as:
   - External/Technical: dependency on an API, integration, or infrastructure component
   - External/Organizational: dependency on another team or vendor
   - External/Regulatory: dependency on a compliance decision or regulatory approval

3. **Circular dependencies**: Flag any cases where Item A depends on Item B and Item B depends on Item A. These represent a planning conflict that must be resolved.

4. **Output format**: Produce a dependency table and a sequencing recommendation.

Dependency Table:
| Item | Depends On | Dependency Type | Impact if Unresolved |
|---|---|---|---|

Sequencing Recommendation:
List the items in a recommended delivery order based on their dependencies, with any parallel tracks clearly noted.
```

---

## Example

**Input:**
```
1. PA Automation — automate prior authorization submission
2. Prescriber Notification — notify prescribers of PA decisions
3. Payer API Integration — connect to payer systems
4. Pharmacy Onboarding Portal — self-service pharmacy registration
```

**Output:**
```markdown
### Dependency Table
| Item | Depends On | Type | Impact if Unresolved |
|---|---|---|---|
| PA Automation | Payer API Integration | Internal | Cannot submit PA without payer connectivity |
| Prescriber Notification | PA Automation | Internal | No PA decision data to notify on |
| Pharmacy Onboarding Portal | None | — | Independent; can be built in parallel |

### Sequencing Recommendation
**Track A (sequential):**
1. Payer API Integration
2. PA Automation
3. Prescriber Notification

**Track B (parallel):**
1. Pharmacy Onboarding Portal (can start anytime)
```
