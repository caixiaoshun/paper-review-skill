---
name: paper-review-skill
description: Review ML/AI papers and draft human-sounding reviewer comments for conference or journal forms. Use when working with `.tex`, `.pdf`, `.docx`, or `.doc` manuscripts, or when the user asks for strengths and weaknesses, rebuttal guidance, recommendation justification, or venue-style review text.
---

# Paper Review Skill

Review the manuscript rigorously. Draft the review like a real reviewer.

## Workflow

### 1. Obtain the manuscript content

- Read `.tex` projects from the main file plus required `\input` or `\include` files.
- Extract `.pdf` text with a reliable tool. Prefer, in order:
  1. a local PDF extraction utility if available;
  2. `pdftotext -layout`;
  3. Python-based extraction such as PyMuPDF, `pdfplumber`, or `pypdf`.
- Extract `.docx` or `.doc` text with a suitable parser such as `python-docx` or `mammoth`.
- Ask for the manuscript path when the user did not provide one.

### 2. Match the output language

- Write in the language requested by the user.
- Default to the manuscript language when the user does not specify one.

### 3. Read the paper in passes

Use at least three internal passes before drafting the review.

1. First pass:
   - Identify the problem statement, motivation, and claimed contributions.
   - Map the proposed method and its main components.
   - Locate the core experiments, tables, figures, and equations.

2. Second pass:
   - Check whether the paper's claims match the evidence.
   - Check whether baselines, controls, and ablations are adequate.
   - Check whether equations, notation, and derivations are clear enough for the paper's claims.
   - Check whether the setup is reproducible from the manuscript.

3. Third pass:
   - Identify the strongest positive points that are actually supported.
   - Identify the main blockers: unfair comparison, inconsistent numbers, unsupported claims, weak ablations, missing controls, unclear math, or missing discussion.
   - Separate major issues from presentation issues.

### 4. Use online search when it helps

Use search during analysis when it helps answer questions such as:

- whether a baseline is current or outdated;
- whether a novelty claim is plausible relative to recent work;
- whether a benchmark, dataset, metric, or protocol has an official setup;
- whether a library, framework, model family, or API behaves as the paper implies.

Prioritize:

1. official documentation, official benchmark pages, official repositories, and original papers;
2. other primary sources such as arXiv pages or project pages;
3. secondary summaries only when primary sources are unavailable.

Use external search to improve understanding, not to replace close reading.

- Judge the paper primarily on what it contains.
- Keep external-comparison remarks fair and specific.
- Do not overstate criticism when the external evidence is mixed.

### 5. Match the review form

- Follow the venue form or the user's template exactly when one is provided.
- If the form asks for `Paper Summary`, keep it short and neutral.
- If the form asks for `Major Weaknesses`, put the main technical blockers there.
- If the form asks for `Suggestions For Rebuttal` and the user wants brevity, `Refer to weaknesses.` is acceptable.

If no form is provided, default to:

1. Paper Summary
2. Strengths
3. Major Weaknesses
4. Minor Weaknesses
5. Suggestions for Improvement or Suggestions for Rebuttal
6. Ethics note if relevant

Do not include scores or accept/reject decisions unless the user explicitly asks for them or the form requires them.

### 6. Draft the review in reviewer style

Read [references/review-writing-style.md](references/review-writing-style.md) before drafting the final prose.

Apply these rules:

- Keep the summary short and neutral.
- State major problems directly.
- Use evidence naturally instead of mechanically.
- Prefer objective phrasing over promotional or emotional phrasing.
- Keep the main body centered on concrete strengths and weaknesses.

### 7. Run the final check

Before finalizing, verify:

- the review matches the requested language;
- the structure matches the venue form or user template;
- the summary stays short and neutral;
- the main technical concerns are explicit and easy to identify;
- the claims are supported by the manuscript or by clearly framed external comparison;
- the prose sounds like a reviewer comment rather than an AI-generated report.
