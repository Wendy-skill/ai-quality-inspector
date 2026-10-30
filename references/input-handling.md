## 4. Input Handling

Choose the inspection method based on the material supplied.

### 4.1 LaTeX source

When `.tex`, `.bib`, or project files are available:

- inspect `\label`, `\ref`, `\autoref`, and `\eqref`
- inspect `\cite`, `\citep`, `\citet`, and related citation commands
- detect undefined labels
- detect duplicated labels
- detect cited-but-missing bibliography entries
- detect unused bibliography entries where feasible
- inspect figure/table file references
- inspect numbering logic
- inspect compilation logs when available

Prefer programmatic checks over manual inspection when source files make this possible.

Do not infer rendered output from source alone when compilation-dependent behaviour matters.

### 4.2 Word / DOCX

When a `.docx` file is available:

- inspect heading hierarchy
- inspect captions
- inspect figure/table/equation numbering
- inspect visible cross-references
- inspect citations and bibliography
- inspect recurring numerical values
- inspect recurring terminology
- compare Abstract, Results, Discussion, and Conclusions
- check RQs, Objectives, Contributions, and final answers for consistency

Do not assume Word fields are correct merely because the rendered text appears correct.

If field-level information is inaccessible, mark that check as unavailable rather than pretending it was verified.

### 4.3 PDF

Treat PDF primarily as a rendered document.

Check:

- visible numbering
- captions
- text–figure agreement
- text–table agreement
- equation references
- citations
- terminology
- cross-page consistency
- Abstract ↔ Results ↔ Conclusions

Hidden Word/LaTeX fields cannot be verified from PDF alone.

Mark those checks as unavailable when necessary.

### 4.4 Images / screenshots

Inspect only information visibly present in the image.

Do not infer:

- missing axes
- hidden legends
- unseen captions
- invisible units
- unreadable numerical values

If a required detail is not visible, mark it as `Needs verification`.
