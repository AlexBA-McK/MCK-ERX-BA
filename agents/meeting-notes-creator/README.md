# Meeting Notes Creator

Analyzes raw meeting transcripts and produces clean, structured, actionable meeting notes.

---

## Description

This agent takes an unedited meeting transcript (copy-paste from Teams, Zoom, or manual notes) and transforms it into organized meeting notes with clearly labeled sections: attendees, key discussion points, decisions, action items, and open questions.

---

## Inputs

| Input | Description |
|---|---|
| **Meeting transcript** | The full or partial text of the meeting recording/transcript |
| **Meeting context** *(optional)* | Meeting title, date, project name, or purpose to improve output quality |

---

## Outputs

A structured Markdown document containing:
- **Meeting Title & Date**
- **Attendees**
- **Agenda / Topics Discussed**
- **Key Discussion Points** (per topic)
- **Decisions Made**
- **Action Items** (owner + due date where mentioned)
- **Open Questions / Parking Lot**
- **Next Steps**

---

## Usage Example

**Input:**
```
Meeting: ERX Rx Fulfillment Review — May 14, 2026
Transcript:
Alex: Okay so the main thing today was the fulfillment SLA. We need to decide if 48 hours is acceptable.
Jamie: I think 24 hours is more aligned with patient expectations. Let's check with compliance.
Alex: Agreed. Jamie can you follow up with compliance by Friday?
Jamie: Sure. Also, the BRD for the new pharmacy API is still not finalized.
Alex: Yeah, Sarah is working on that. We need it by next sprint.
```

**Output:**
```markdown
## Meeting Notes — ERX Rx Fulfillment Review
**Date:** May 14, 2026

### Attendees
- Alex
- Jamie

### Key Discussion Points
- Rx fulfillment SLA target: 48-hour vs. 24-hour window debated.

### Decisions Made
- 24-hour SLA preferred; pending compliance sign-off.

### Action Items
| Owner | Action | Due Date |
|---|---|---|
| Jamie | Follow up with compliance on 24-hour SLA | Friday |
| Sarah | Finalize BRD for new pharmacy API | Next sprint |

### Open Questions
- Will compliance approve the 24-hour SLA?

### Next Steps
- Jamie to report back after compliance check.
- BRD review in next sprint planning.
```

---

## Limitations

- The agent relies on the quality of the transcript; unclear or overlapping speech may produce incomplete notes.
- Speaker attribution is preserved only if names are present in the transcript.
- Action item due dates are extracted only when explicitly mentioned.
