# v3 — Interface with the 17 Research Skills

Load this reference **only** when handing a task or evidence to another Skill. Standalone use is unaffected.

## Ownership

- **Member:** ai-paper-editor.
- **Own:** Author-approved structure, terminology and language revisions.
- **Optional specialist support:** claim-graph-paper-writer for argument graph, paper-format-guardian for DOCX style, journal-gap-analyzer for benchmark-based editorial comparison.
- **Chinese triggers:** 论文编辑、学术润色、结构调整.
- **English triggers:** paper editing, academic polishing.
- **Do not trigger:** Do not silently strengthen findings or alter scientific meaning.

## Handoff and evidence

For the full contract, load `coordination-protocol.md` and `specialist-routing.md` in this folder. Provide `ID | owner | document/version/location | claim or issue | located evidence | source status | assessment | local Severity / Impact or urgency | action | author approval | workflow state`.

Source status: `Reported / Documented / Independently checked / Not available`. Assessment: `Confirmed / Reasoned inference / Unverified` (state precisely what is confirmed). State: `Open / Waiting for evidence / Awaiting author / Resolved / Recheck needed`. Scientific Severity and QA Impact must not be conflated.

Reuse only valid, version-matched Claim/Data Ledger records when available; the ledger is not auto-synchronised. Optional external Skills must be actually installed and invoked before claiming they ran. Return to the responsible member and selectively recheck after substantive changes. Do not call all specialists by default.
