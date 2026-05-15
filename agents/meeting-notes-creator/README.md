# Meeting Notes Creator

## Purpose

Converts raw meeting transcripts or rough meeting notes into clean, structured, and shareable meeting notes. Ensures consistent formatting across all team meetings and reduces the manual effort of note-taking.

## Inputs

| Input | Required | Description |
|---|---|---|
| Meeting transcript or raw notes | ✅ Yes | The unstructured text captured during or after the meeting |
| Meeting date | ✅ Yes | Date of the meeting (used in the notes header) |
| Meeting title / topic | ✅ Yes | Short title or subject of the meeting |
| Attendees list | ⬜ Optional | Names and roles of participants |
| Action item owner(s) | ⬜ Optional | Names to attribute action items to |

## Outputs

A structured Markdown document containing:
- **Meeting header** — title, date, attendees, facilitator
- **Agenda** — topics discussed (inferred or explicit)
- **Summary** — concise overview of the meeting
- **Key Discussion Points** — organized by topic
- **Decisions Made** — numbered list of decisions
- **Action Items** — table with owner, description, and due date
- **Next Steps / Follow-ups**
- **Next Meeting** *(if mentioned)*

## Usage

1. Copy the contents of [`instructions.md`](instructions.md).
2. Paste into Copilot Chat (or your LLM tool) as the first message.
3. Follow up with the meeting transcript or notes.
4. Optionally add context: *"The meeting was on [date], topic was [topic], attendees were [names]."*
5. Review the output, adjust any inaccuracies, and share with attendees.

## Example

See [`example-input.md`](example-input.md) and [`example-output.md`](example-output.md) for a worked example.
