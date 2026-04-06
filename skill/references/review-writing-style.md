# Review Writing Style

Use these rules when turning analysis into final review text.

## Core rule

Write like a reviewer filling a conference or journal form:

- sound like someone who read the paper carefully;
- point out what works and what does not;
- avoid polished executive-summary prose.

## 1. Keep the opening short and neutral

- Use 1-3 neutral sentences for a summary field.
- Do not turn the summary into an evaluation paragraph.
- Do not front-load praise unless the venue style clearly calls for it.

Prefer:

- "This paper proposes X for Y and evaluates it on Z."
- "The method combines A and B and reports results on C."

Avoid:

- "This paper presents a promising and compelling framework..."
- "The work is well motivated and comprehensively validated..."

## 2. Go directly to the concrete issues

After the short summary, move quickly to strengths and weaknesses.

- Keep strengths brief and specific.
- Put the main technical blockers in major weaknesses.
- State the issue first, then point to the evidence, then explain why it matters.

Preferred patterns:

- "The main result tables are inconsistent."
- "The comparison is not fair because the proposed method uses a much stronger backbone."
- "The claim of consistent improvement is stronger than the evidence shown."
- "The current ablations do not isolate the contribution of the proposed module."

## 3. Avoid AI-sounding review language

Do not default to phrases such as:

- "promising"
- "compelling"
- "well motivated"
- "strengthens the paper's foundation"
- "practically significant finding"
- "interesting and timely direction"

Prefer plain reviewer language:

- "reasonable"
- "useful"
- "unclear"
- "not well supported"
- "needs clarification"
- "not isolated by the current ablation"

## 4. Prefer objective phrasing

Prefer:

- "The current empirical evidence is not strong enough to support this claim."
- "The manuscript does not provide a fair comparison against matched baselines."
- "This configuration is not sufficiently justified by the ablations."

Avoid unnecessary personal framing such as:

- "I like the idea, but..."
- "I am excited by this direction..."

Use first-person wording only when it sounds natural and adds clarity.

## 5. Do not force a grand summary plus a long exhaustive list

Avoid:

- one polished high-level summary paragraph;
- followed by a long list that restates the same points in more abstract language.

Instead:

- keep the overall summary short;
- let the concrete weaknesses carry the review.

## 6. Use evidence naturally

Support claims with table, figure, section, or equation references when helpful, but do not attach a reference to every sentence just because a template allows it.

Natural examples:

- "Table 3 is described as a 6-layer setting, but the reported WPT-AASIST numbers match the 24-layer baselines in Tables 2 and 4."
- "Figure 2 supports the claim that the residual signal separates real and fake samples across the four domains."

If a point depends on external search, include it only when the comparison is relevant, defensible, and expressed in normal reviewer language.

## 7. Separate major and minor issues correctly

Treat these as major issues:

- unfair or incomplete comparisons;
- inconsistent tables or metrics;
- unsupported claims;
- weak ablations or missing controls;
- unclear derivations that matter to the contribution;
- reproducibility gaps that block evaluation.

Treat these as minor issues:

- figure readability;
- table formatting;
- color choices;
- typos;
- local wording problems.

Do not bury a real methodological blocker inside minor comments.

## 8. Write recommendation justifications in a restrained way

If the form asks for a recommendation justification:

- keep it short;
- tie it to the main blockers;
- avoid emotional or promotional framing.

Prefer:

- "The current empirical evidence is not solid enough to support a stronger recommendation."
- "The main comparison is not reliable enough in its current form because the key tables are inconsistent."
- "The paper may become more convincing after stronger matched baselines and cleaner ablations."

Avoid:

- "I really like this idea, but..."
- "This excellent and exciting work would be much stronger if..."
