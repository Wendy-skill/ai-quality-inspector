# v3 — Interface with the 17 Research Skills

Load this reference **only** when handing a task or evidence to another Skill. Standalone use is unaffected.

## Ownership

- **Member:** ai-literature-member.
- **Own:** Literature search, full-text reading and citation identity.
- **Optional specialist support:** research-reading-mentor only for connected reading-note workflows; return source-based evidence to reviewer/editor without overstating full-text access.
- **Chinese triggers:** 文献检索、文献深读、引用核验.
- **English triggers:** literature search, citation verification.
- **Do not trigger:** Scientific validity and editing decisions are outside the literature member.

## Handoff and evidence

For the full contract, load `coordination-protocol.md` and `specialist-routing.md` in this folder. Provide `ID | owner | document/version/location | claim or issue | located evidence | source status | assessment | local Severity / Impact or urgency | action | author approval | workflow state`.

Source status: `Reported / Documented / Independently checked / Not available`. Assessment: `Confirmed / Reasoned inference / Unverified` (state precisely what is confirmed). State: `Open / Waiting for evidence / Awaiting author / Resolved / Recheck needed`. Scientific Severity and QA Impact must not be conflated.

Reuse only valid, version-matched Claim/Data Ledger records when available; the ledger is not auto-synchronised. Optional external Skills must be actually installed and invoked before claiming they ran. Return to the responsible member and selectively recheck after substantive changes. Do not call all specialists by default.
