# Knowledge Base Agent Rules (kb/)

## Purpose

The `kb/` directory stores structured knowledge used for research.

This includes:

- theoretical concepts
- methodological tools
- data documentation
- codebooks
- prompt templates

The goal is to build a reusable and cumulative knowledge base.

---

## Structure

The agent MUST organize knowledge into the following subdirectories:

kb/
  concepts/
  methods/
  data-docs/
  codebooks/
  promptbooks/

---

## File Creation Rules

The agent MUST:

- Create a new file for each distinct concept, method, or dataset
- Use descriptive, lowercase, hyphen-separated filenames
- Avoid mixing multiple topics in one file

Example:

- social-capital.md
- fixed-effects-model.md
- acs-data.md

---

## Content Requirements

Each knowledge file MUST include:

1. Definition or description  
2. Key components or structure  
3. When to use  
4. Limitations  
5. References (if applicable)  

---

## Knowledge Types

### 1. concepts/
- Sociological or theoretical ideas
- Example: inequality, social capital, neighborhood effects

### 2. methods/
- Statistical or computational methods
- Example: regression, matching, fixed effects

### 3. data-docs/
- Dataset-level documentation
- Example: ACS, ECLS-K, CPS

### 4. codebooks/
- Variable-level documentation
- Must include variable definitions and coding schemes

### 5. promptbooks/
- Reusable AI prompts for analysis or writing

---

## Writing Style

The agent MUST:

- Be concise and structured
- Avoid unnecessary narrative
- Use bullet points when possible
- Separate facts from interpretation

---

## Cross-Domain Usage

The agent MUST:

- Use knowledge from `kb/` when interpreting results
- Reference relevant knowledge in analysis and writing
- Update knowledge files when new insights are gained

---

## Update Rules

The agent MUST:

- Update existing files rather than duplicating similar content
- Add new files when encountering new concepts or methods
- Log major additions or changes in memory/decisions.md

---

## Forbidden

The agent MUST NOT:

- Store raw data here
- Store analysis outputs here
- Mix knowledge with memory or scripts

---

## Final Principle

The `kb/` directory is a **living knowledge system**, not a dump.

Knowledge should be:

- reusable
- structured
- cumulative
