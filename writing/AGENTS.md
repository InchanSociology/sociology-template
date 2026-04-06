
# Writing Principles for Academic Journal Articles

Theory-driven empirical research targeting top journals in sociology.

Scope: ‘writing/‘ directory tree. The root ‘AGENTS.md’ also applies.

---

## Quality Standards (always apply)

- **Academic, human voice**: Write in a professional academic tone with natural, readable prose. Avoid "AI-sounding" filler, stock transitions, and overly polished generic phrasing.
- **Accuracy, conciseness, coherence.** Stay engaging; avoid unnecessary dryness. Prefer plain language over jargon; define technical terms at first use.
- **Clarity first.** Use short-to-medium sentences, active voice, and concrete examples to explain abstract ideas.
- **Specificity over generalities.** Avoid broad, empty statements. Make claims concrete by naming mechanisms, scope conditions, data, comparisons, and implications.
- **Consistency.** Keep terminology, notation, and framing consistent across sections; avoid sudden shifts in formality or voice.
- **Substantive titles.** Section and subsection titles should name the central concept, argument, or phenomenon, not describe what the section does. Avoid meta-descriptive titles like "Why X Matters." Prefer titles that a reader can learn from: "Communication as Constitutive of Objectivity" over "Why These Three Properties Matter."
- **Fewer em dashes (---/--):** Prefer commas, parentheses, or shorter sentences; use an em dash only when it improves clarity or emphasis.

## Structure and Citations (apply when appropriate)

- **Paragraph structure.** Each paragraph should open with a clear topic sentence, state a claim, provide supporting evidence or mechanism, and close with a takeaway (implication, boundary condition, or transition).
- **Math and notation.** State the intuition and purpose _before_ any equation. Define variables at first use, introduce notation gradually, and explain what the equation does immediately after it appears.
- **Idea-first citations.** Lead with the idea or claim, then cite parenthetically with `\autocite`. Reserve `\textcite` (narrative citation) for cases where the author is genuinely the topic of the sentence (e.g., introducing a scholar for the first time, or when the author’s identity is relevant to the argument). Vary citation integration to avoid repetitive syntax.
- **Pinpoint citations.** For specific arguments, definitions, method details, figures/tables, or key evidence, include pinpoint locations (page, section, figure/table number, or chapter) where possible, even when paraphrasing. Always use **journal page numbers** (not article-relative page numbers) for pinpoint references to journal articles.
- **Reference authenticity.** Do not invent citations. Only cite references that exist in the project's `*.bib` files.

## Latex build rules

- Keep the final PDF in `/writing/latex_aux/` (e.g. `.aux`, `.bbl`, `.bcf`, `.blg`, `.fdb_latexmk`, `.fls`, `.log`, `.out`, `.run.xml`, `.thm`, `.toc`)

