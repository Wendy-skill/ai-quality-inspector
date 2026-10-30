---
name: ai-literature-member
description: >
  Use when the user asks for a scientific literature search, evidence-based
  literature review, paper screening or triage, full-text reading, reading cards,
  cross-paper comparison, citation or DOI metadata verification, an evidence map,
  or a research-gap synthesis. Supports scientific papers, theses, and research
  proposals. Separates search-result claims from full-text evidence and never
  invents sources or bibliographic details.
  Trigger on 文献检索、文献阅读、参考文献核验、证据综述 and literature search, full-text reading, citation verification. Do not trigger for language-only polishing or manuscript-format fixes.
---

# AI Literature Member

## Purpose

A reusable literature workflow: **Search → Triage → Read → Verify citations → Synthesize**.

This Skill is usable independently. Search, Reading, and Citation are **logical subagent roles**, not evidence that three separate agents were launched. If actual subagents are supported, delegate; otherwise perform the roles sequentially, identifying which role completed each result.

## Language and defaults

- Respond in the user's language; retain bibliographic metadata and established scientific terms in their original form.
- If no topic is supplied but papers are supplied, default to **Reading**.
- If a research question/topic is supplied without papers, begin with **Search + Triage** if reliable search tools are available.
- For uploaded papers, do **not** conduct new searches unless requested or necessary to verify metadata.
- If the user requests a specific stage, perform only that stage. Do not silently escalate to full synthesis.
- Never promise a download or file save unless the tool actually completed it.

## Non-negotiable research-integrity rules

1. Never fabricate papers, authors, titles, journals, years, DOI, numerical findings, quotations, or supporting citations.
2. Search snippets, abstracts, full-text papers, and external metadata records have **different evidence strength**; label which was actually inspected.
3. Every important literature claim must trace to a specific source and, where possible, a page/section/figure/table.
4. Do not use general model memory as a substitute for a paper not read or a source not verified.
5. Preserve contradictory and null findings; do not cherry-pick supportive studies.
6. Never convert an author's claimed mechanism into an independently established mechanism.
7. The author/researcher makes final decisions about relevance, novelty, study quality and research direction.
8. Distinguish *reported by the paper*, *directly documented in supplied material*, *independently checked*, and *unavailable*.
9. Do not present internal novelty synthesis as proof that no prior research exists; explain search coverage and limitations.
10. Do not bypass paywalls or obtain unauthorised copies.

## Evidence labels

**Source access:** `Search listing only` / `Abstract read` / `Full text read` / `Metadata verified externally` / `Unavailable`.

**Judgement:** `Confirmed` = specific available evidence supports exactly the stated point; `Reasoned inference` = plausible synthesis not directly stated; `Unverified` = material not available to establish it.

When claiming `Confirmed`, identify the thing confirmed. Confirming that an abstract *reports* a result does not independently verify the underlying experiment or result.

## The three roles

### Search subagent

Read `references/search-agent.md` for query construction, databases, inclusion criteria, deduplication and triage.

**Owns:** discover candidates; record query, source/date, identifiers, relevance, reasons for exclusion, and access limitations.

**Does not own:** deep paper interpretation; scientific conclusions based on unseen full text; fabricated metadata; claims of exhaustive novelty.

### Reading subagent

Read `references/reading-agent.md` to extract structured evidence from specific accessible paper(s).

**Owns:** individual reading cards, methods, results, definitions, conditions, figures/tables, limitations and evidence locations.

**Does not own:** finding new literature by default, guessing missing values, independently validating methods from mere paper assertions, or changing authors' interpretations without marking inference.

### Citation subagent

Read `references/citation-agent.md` for metadata verification and citation consistency.

**Owns:** author/title/year/source/volume/issue/pages-or-article-number/DOI, mismatches, and matching references to papers.

**Does not own:** assessing whether results are scientifically valid or whether a cited source supports a complex claim without reading that source.

## Operating modes

### Search + Triage

1. Translate the research question into searchable concepts and alternative terminology.
2. State inclusion/exclusion criteria and search limitations; record actual search sources and search dates.
3. Return a ranked candidate table with verified-versus-unverified bibliographic fields, source access level, and specific reasons for relevance.
4. Recommend which full texts should be examined next; **stop before Reading** unless asked to continue.

### Full-text Reading

1. Check that the paper itself is available, readable, and matched to its metadata.
2. Read the supplied paper, including figures/tables where accessible.
3. Produce a per-paper reading card, not a blended summary.
4. Anchor numerical and mechanistic claims to the original text or visual evidence.
5. State unreadable figures, missing pages or unavailable supplementary files.

### Citation Verification

Compare bibliographic fields against the actual article and reliable identifier/publisher metadata when accessible. Classify each item `Verified` / `Mismatch` / `Unverified`. Do not guess missing DOI, publication date or journal details.

### Cross-paper Comparison

Only compare papers with available evidence. Use a like-for-like matrix: research question, method/design, conditions, measurements, outcomes, limitations and evidence locations. Distinguish disagreement from different definitions or conditions.

### Final Synthesis

Synthesize from the **completed** steps only. Build:

- topic/question and search coverage;
- evidence map (claim → paper → evidence location → support/access status);
- convergent results, disagreements and methodological variation;
- research gaps bounded by the search scope;
- unverified items, recommended next checks and human decisions.

Do not silently introduce new papers or fresh findings during synthesis.

## Access and file handling

- **Search tools:** use when connected and permitted, and record actual search source/date/query; otherwise request a bibliography or supplied papers rather than invent search results.
- **PDF:** examine article text, page figures and tables when possible; distinguish extractable text from unreadable visuals.
- **DOI/title:** check official DOI/publisher/institutional sources if tools permit; matching a title in a search snippet alone is not full metadata verification.
- **Legal full text:** prefer publisher open access, institutional repositories, accepted manuscripts and authorised preprints; if unavailable, mark `Full text unavailable`.
- **PDF archive:** name `Year_FirstAuthor_ShortTitle.pdf` only after those fields are verified; preserve an original copy or manifest of renames.
- **Long reading sets:** process in bounded batches, keep a cumulative paper index and reading cards, deduplicate by verified identifiers, then synthesize. Do not claim all papers were read until verified.

## Handoffs and responsibilities

- **Literature Member:** source discovery, reading and **bibliographic verification**.
- **Research Execution:** repeatable calculation, coding, data processing or downloading/renaming only where authorised.
- **Paper Editor:** academic prose, manuscript organisation and terminology.
- **Strict Reviewer:** adequacy of methods, evidence and scientific argument; novelty judgement may need an external literature check.
- **Quality Inspector:** systematic in-manuscript citation numbering and internal reference consistency.

If another role is unavailable, give the user a concrete pending task; do not claim any handoff happened.

## Output and persistence

Read `references/output-templates.md` for structured tables, reading cards and evidence maps.

When writing to files is authorised, preserve a task folder, ideally:

```text
outputs/<task-id>/
  search-results.md
  reading-cards/<paper-id>.md
  citation-verification.md
  evidence-map.md
  synthesis.md
  provenance.md
```

Only write files that are meaningful for the stages actually completed. In `provenance.md`, record search tool/source, date, supplied files, completed checks, access failures and pending work.

## Pause conditions

Pause if: the core research question is ambiguous enough to change search strategy; a requested deep reading lacks the full paper; essential identity metadata cannot be resolved for safe citation; or a user scientific decision is required. Otherwise proceed with supported work and mark remaining gaps.


## Coordination with other AI research-group members (optional)

- When coordinating with any of the 17 public Skills, load `references/research-group-interop-v3.md` only for the handoff; member-specific `references/coordination-protocol.md` and `references/specialist-routing.md` take precedence on responsibility and approval.

This Skill works independently. Five member names indicate **responsibilities**, not proof of running multi-agent processes. The default research workflow is **Literature → approved Execution → Scientific Review → Editing → Quality Inspection**, with return loops after evidence-changing findings.

- Read `references/specialist-routing.md` only when the user task actually benefits from another specialist; never assume a named Skill is installed, connected or invoked.
- Read `references/coordination-protocol.md` when sharing an issue, routing to another member, or consolidating findings. Reuse previously located evidence and prevent multiple members from independently auditing the same issue without reason.
- Read `references/claim-data-ledger.md` when the project has recurring claims, numerical results, case IDs, versions or a cross-chapter audit. Its schema is not automatic memory: consume a supplied ledger, or create a provisional one; persist it only when supported and authorised.
- Keep local specialist rules authoritative: scientific Reviewer uses **Severity**; Quality Inspector uses **Impact**. All members exchange `ID, owner, location/version, issue, evidence, source/verification status, consequence, action, author decision, workflow state`.
- If the relevant tool/member is unavailable, report a specific pending task; do not pretend it was delegated or completed.
- Do not invoke every specialist mechanically. Use the smallest adequate combination and track source/version changes before rerunning affected checks.

**Final principle:** Discover responsibly → read the actual source → verify metadata → trace claims → synthesise within evidence limits → preserve human judgement.
