# Repo Agent Instructions

Follow the most specific AGENTS.md that applies to any file you edit.

## Project framework: Rules, Memory, Knowledge

This project is organized around three dimensions. **Do not mix them.**

- **Rules** (‘AGENTS.md’ files) = how the agent works. Procedural constraints, file conventions, verification expectations. Relatively stable.
- **Memory** (memory/) = where the project currently stands. Evolving direction, decisions made, open questions, prompt revision history. Changes frequently.
- **Knowledge** (‘kb/‘) = what the project knows. Literature, concept definitions, codebooks, promptbooks, data documentation. Grows as new materials are added.

## Directory scope

| Directory | Purpose | Agent rules |
| --------- | ------- | ----------- |
| `script/` | Research code and pipelines | See `script/AGENTS.md` |
| `writing/` | Manuscripts and Latex | See `writing/AGENTS.md` |
| `memory/` | Evolving project context | See below |
| `kb/` | Substantive knowledge base | See below |
| `data/` | Source data (**read-only**) | Prefer `data/raw/`, `data/intermediate/`, `data/processed/` for stages |
| `output/` | Generated artifacts | Prefer subfolders: `output/tables/`, `output/figures/`, `output/models/` |

** Directory convertions

- Treat `data/` as read-only. Never overwrite source data silently
- Write generated artifacts (table, figures, model) under `output/`.
- Write manuscripts and report under `writing/`.
- Keep inputs and outputs separated; never silently overwrite.

## Verification expectations

- Save interim outputs befor finalizing any analysis. 
- Compare new results against prior versions when they exist.
- Flag ambiguity rather than forcing a conclusion. State the uncertainty explicitly, propose options with brief rationale, and do not proceed with a default assumption siletly.

## Execution Priority

The agent MUST follow rules in the following order of priority:

1. Directory-specific AGENTS.md (e.g., script/, writing/)
2. Root AGENTS.md
3. User instructions

If conflicts occur, the more specific rule overrides the general one.


## Task Decomposition

The agent MUST:

- Break down complex tasks into sequential steps
- Explicitly state the plan before execution when tasks are non-trivial
- Execute tasks step-by-step rather than all at once
- Verify outputs before proceeding to the next step

## File Management Rules

The agent MUST:

- Create new files rather than overwrite existing ones unless explicitly instructed
- Never delete files without explicit instruction
- Maintain versioning or logging when modifying outputs
- Respect directory roles (no cross-directory misuse)

## Research Integrity

The agent MUST:

- Distinguish clearly between empirical results and interpretation
- Avoid causal claims unless supported by appropriate methods
- State assumptions explicitly
- Highlight limitations of data and methods
- Avoid overgeneralization beyond the sample

## Reproducibility Scope

All outputs in this project MUST be reproducible from:

- script/ code
- data/ inputs

The agent MUST NOT rely on hidden state, manual steps, or undocumented transformations.

## Cross-Domain Interaction

The agent MUST:

- Use knowledge from kb/ when interpreting results
- Record decisions in memory/ when new assumptions or changes occur
- Ensure writing/ reflects outputs generated from script/


## Sociological Reasoning & Workflow

The agent MUST:
- **Theory-Data Dialogue**: When creating models in `script/`, justify the inclusion of control variables based on the sociological literature found in `kb/`.
- **Contextual Interpretation**: In `writing/`, do not just report p-values. Explain what the coefficients mean for the actual social actors or institutions (e.g., Texas high schools).
- **Inclusion/Exclusion Logic**: Every data filtering decision must be recorded in `memory/` to ensure the research's transparency and to address potential selection bias.



