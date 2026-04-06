# Memory Agent Rules

## Purpose

The `memory/` directory stores the evolving state of the project.

This includes:

- decisions made
- assumptions
- open questions
- project progress

This is NOT a place for final results or knowledge storage.

---

## Core Principle

Memory is for **reasoning and traceability**, not outputs.

---

## Required Files

The agent MUST use:

- decisions.md → major decisions and reasoning
- (optional) open_questions.md → unresolved issues
- (optional) progress.md → project status

---

## Logging Rules

The agent MUST:

- Record all major decisions in `decisions.md`
- Explicitly state reasoning behind choices
- Log assumptions when they are made
- Update memory continuously during the project

---

## Open Questions

The agent SHOULD:

- Record ambiguities or uncertainties
- Avoid silently resolving unclear issues
- Propose possible interpretations when relevant

---

## What NOT to store

The agent MUST NOT:

- Store raw data
- Store analysis outputs
- Store general knowledge (use kb/ instead)

---

## Relationship to Other Folders

- script/ → produces outputs
- kb/ → stores general knowledge
- writing/ → produces manuscripts
- memory/ → tracks decisions and reasoning

---

## Final Principle

If a decision is not recorded in memory, it did not happen.

## Required Files Usage

The agent MUST use:

- decisions.md → record decisions and reasoning
- open_questions.md → record ambiguities and unresolved issues
- progress.md → track project status and next steps
- change_log.md → track major changes

---

## Update Triggers

The agent MUST update memory when:

- a new variable is created
- a model is specified or changed
- a sample is restricted
- an ambiguity is encountered
- a major change is made