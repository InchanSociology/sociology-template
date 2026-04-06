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







