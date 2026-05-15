# Extract Acceptance Criteria

## Purpose
Extract and structure acceptance criteria from unstructured requirements text, user stories, or meeting notes.

## When to Use
- Inside the `user-story-creator` agent to ensure every story has criteria
- Inside the `document-analyzer` agent to assess criteria completeness
- Standalone when reviewing a feature description that lacks explicit criteria

---

## Skill Definition

```
For each requirement or user story provided, extract or derive acceptance criteria using the following rules:

1. Look for explicit acceptance criteria already stated in the text (e.g., "the system must...", "users should be able to...", "pass if..."). Extract and reformat them.
2. For requirements with no explicit criteria, derive testable criteria based on the stated goal. Each criterion must be:
   - Specific: refers to a concrete behavior or outcome
   - Measurable: has a clear pass/fail condition
   - Unambiguous: cannot be interpreted in multiple ways
3. Format each set of criteria as a checklist:
   - [ ] [Criterion]
   - [ ] [Criterion]
4. Flag any requirement where acceptance criteria cannot be derived due to insufficient information. Mark it: ⚠️ Insufficient detail — clarification needed.
5. Do not invent business logic or system behavior not implied by the requirement.
```

---

## Example

**Input:**
```
REQ-005: Users must be able to reset their password.
```

**Output:**
```markdown
**REQ-005 — Acceptance Criteria:**
- [ ] A "Forgot Password" link is accessible from the login page.
- [ ] Clicking the link prompts the user to enter their registered email address.
- [ ] A password reset email is sent to the user's registered email within 2 minutes.
- [ ] The reset link in the email expires after 24 hours.
- [ ] After a successful password reset, the user is redirected to the login page.
- [ ] If the email address is not found, an appropriate error message is displayed without revealing whether the account exists.
```
