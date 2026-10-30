# AI Research Group v3 — 17 Skill Routing Index

This index describes **optional** coordination across 17 public Skills. Each remains independently usable. A route is a recommendation, not a claim that another Skill was invoked.

## Five member / orchestrator Skills

| Member | Owns | Specialist support (only if useful and available) |
| --- | --- | --- |
| ai-literature-member | Search, source reading, citation identity, evidence maps | research-reading-mentor for Zotero/Obsidian deep-reading workflows |
| ai-research-execution | Approved computations, analysis, figures and reproducibility logs | fluent-setting-checker for configuration traceability; physics-sanity-check for a separate plausibility question |
| ai-paper-editor | Structure, terminology, language and meaning-preserving editing | claim-graph-paper-writer for proposition-level restructure; paper-format-guardian for Word formatting; journal-gap-analyzer for evidence-based editorial comparison |
| ai-strict-reviewer | Overall scientific adequacy, methods, evidence, interpretation and **Severity** | engineering-experiment-reviewer, engineering-review-paper-reviewer, simulation-paper-auditor, claim-evidence-checker, physics-sanity-check, journal-gap-analyzer |
| ai-quality-inspector | Numbers, captions, cross-references, manuscript requirements and **Impact** | paper-format-guardian for authorised fixes; fluent-setting-checker with actual solver evidence |

## Twelve specialist/support Skills

| Skill | Owns; should NOT replace |
| --- | --- |
| research-monday-start | Weekly planning and 25-minute first action; not execution or manuscript review |
| research-reading-mentor | Source-based reading and Zotero/Obsidian evidence notes; not source invention or scientific acceptance |
| engineering-experiment-reviewer | Experimental design, measurement, replication, uncertainty; not whole-manuscript editorial polish |
| engineering-review-paper-reviewer | Review-study scope, search, synthesis, contribution; not universal paper review |
| simulation-paper-auditor | Numerical-method credibility and simulation V&V; not all writing or figure formatting |
| fluent-setting-checker | Manuscript settings versus **actual** Fluent evidence; not solver-run proof without records |
| physics-sanity-check | Physical plausibility and alternatives; plausibility is not mechanism proof |
| claim-evidence-checker | Located claim-to-evidence mapping; strict-reviewer synthesises scientific Severity |
| journal-gap-analyzer | Comparative fit to **identified** journal papers; not acceptance prediction |
| paper-format-guardian | Audited Word formatting with backup/content invariance; not scientific rewriting |
| claim-graph-paper-writer | Claim graph/argument structure and authorised reconstruction; not scientific fact invention |
| skill-optimizer | Skill token/workflow efficiency; retain safety, constraints and specialist capabilities |

## Flow

Literature → approved Execution → Scientific Review → Editing → Quality Inspection.

This is a flexible default; a purely editorial task need not run earlier stages. Scientific review may return issues to Literature/Execution; Quality Inspection may return numeric issues to the author or Execution; substantive changes trigger targeted rechecking, not an automatic full rerun.

## Shared issue envelope

`ID | current owner | file/version/location | exact issue/claim | located evidence | source status | assessment | local scientific Severity or QA Impact (never force conversion) | action | author decision | workflow state`

Source status: `Reported`, `Documented`, `Independently checked`, `Not available`. Assessment: `Confirmed`, `Reasoned inference`, `Unverified`, always specifying **what** was verified. State: `Open`, `Waiting for evidence`, `Awaiting author`, `Resolved`, `Recheck needed`. Do not claim a successful tool call, file edit or persistent ledger without the tool evidence.

## Ledger

Record Claim ID, Data ID, source document/version, condition/baseline, figure/table, calculation/script/version, verification method and linked issue IDs. Reuse only when those match the current task. The ledger is **not** automatically shared or saved across apps.

## Loading

Read each Skill's own `SKILL.md` first; read its local `references/research-group-interop-v3.md` only for cross-Skill tasks. Member Skills also retain role-specific `references/coordination-protocol.md`, `references/specialist-routing.md` and `references/claim-data-ledger.md`. Do not load every Skill on each request.

## Testing status

These are documented contracts and synthetic acceptance cases, **not proof of live multi-agent integration or scientific performance**. Real end-to-end tests should assess routing, evidence fidelity, version tracking, non-duplication and consent boundaries.
