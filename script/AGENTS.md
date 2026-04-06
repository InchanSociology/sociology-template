# Script Agent Rules (Strict Execution Version)

## 0. Enforcement Rule
The agent MUST follow all rules below.
If any rule is violated, the agent MUST stop execution and report the issue.

## 1. Core Principle
All code MUST be:

- Reproducible (same input → same output)
- Modular (separable, single-responsibility scripts)
- Non-destructive (raw data NEVER modified)

## 2. 🚫 Forbidden Actions (Hard Constraints)
The agent MUST NOT:

- Overwrite any file in data/raw/
- Hardcode absolute or user-specific file paths
- Execute randomness without setting a seed
- Create variables without documentation
- Modify existing variables silently (must log changes)

If any of the above occurs → STOP and raise an error

## 3. ✅ Required Execution Rules

### 3.1 Reproducibility
The agent MUST:

- Set a random seed at the beginning of every script
- Use project-relative paths ONLY
- Ensure scripts run end-to-end without manual intervention

### 3.2 Script Pipeline (Strict Order)
The agent MUST organize scripts EXACTLY as follows:

script/
  00_import.py
  01_clean.py
  02_construct_variables.py
  03_analysis.py
  04_visualization.py

Rules:

- Each script MUST be independently executable
- Each script MUST save outputs for the next stage
- No script may skip steps or merge responsibilities

## 4. Output Management
The agent MUST save outputs ONLY to:

- Tables → output/tables/
- Figures → output/figures/
- Models → output/models/

Rules:

- DO NOT overwrite outputs without versioning or logging
- Outputs MUST be reproducible from scripts
- Intermediate data MUST go to data/intermediate/

## 5. Variable Construction Protocol
For EVERY constructed variable, the agent MUST:

- Add inline code comments explaining:
  - definition
  - transformation logic
  - units (if applicable)

- Log the variable in:
  memory/decisions.md

Including:

- variable name
- description
- reason for creation

If not documented → DO NOT create the variable

## 6. Model Transparency Protocol
For EVERY model, the agent MUST explicitly document:

- Dependent variable
- Independent variables
- Control variables
- Sample restrictions
- Estimation method (e.g., OLS, logit, fixed effects)

This MUST be:

- Written in code comments
- Saved alongside model outputs

## 7. Statistical Integrity Rules
The agent MUST:

- Report effect sizes (NOT only p-values)
- Report uncertainty:
  - standard errors OR confidence intervals
- Avoid binary “significant / not significant” interpretation
- Conduct at least ONE robustness check

If these are missing → analysis is invalid

## 8. Pipeline Integrity (Critical Rule)
Running the full pipeline:

00_import → 01_clean → 02_construct_variables → 03_analysis → 04_visualization

MUST:

- Reproduce ALL outputs
- Require ZERO manual fixes
- Produce identical results across runs

If not → pipeline is broken

## 9. Logging Requirement
The agent MUST log:

- All variable construction → memory/decisions.md
- All major analysis decisions → memory/decisions.md
- Any deviations from plan → memory/decisions.md

## 10. Failure Handling
If any rule is violated, the agent MUST:

- STOP execution immediately
- Explain:
  - which rule was violated
  - where it occurred
  - how to fix it

## 11. Project Initialization (Critical)
If the required project structure does NOT exist, the agent MUST create it.

Required directory structure:

script/
data/raw/
data/intermediate/
data/processed/
output/tables/
output/figures/
output/models/
memory/
notebooks/

Required files:

script/00_import.py
script/01_clean.py
script/02_construct_variables.py
script/03_analysis.py
script/04_visualization.py
memory/decisions.md

Rules:

- The agent MUST create missing directories and files automatically
- The agent MUST initialize each script with a minimal runnable template
- The agent MUST NOT wait for user instruction to create these

If structure is missing → CREATE before any analysis

## 12. Notebook Rules (Jupyter Integration)
Jupyter notebooks are for explanation, exploration, and presentation ONLY.

The agent MUST follow:

- All final data processing and analysis MUST be reproducible via script/*.py
- Notebooks MUST read from saved outputs (NOT hidden memory state)
- Each notebook MUST run top-to-bottom without errors
- Notebooks MUST NOT be the sole analysis pipeline

Each notebook SHOULD include markdown explaining:

- research question
- data source
- variable construction
- model interpretation
- limitations

## Final Principle

Scripts (.py) are the source of truth
Notebooks (.ipynb) are for interpretation and communication
