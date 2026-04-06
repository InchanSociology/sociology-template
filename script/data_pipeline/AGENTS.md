# Data Pipeline Agent Rules

This directory contains scripts that transform raw data into analysis-ready datasets.

## Purpose

- Convert raw data into structured, clean, and reproducible datasets
- Standardize variables across sources and time
- Output datasets to `data/intermediate/` and `data/processed/`

---

## Core Principles

### 1. Reproducibility First

- Every dataset in `data/processed/` must be reproducible from:
  - `data/raw/`
  - scripts in this directory
- No manual steps allowed
- No undocumented transformations

---

### 2. Raw Data is Read-Only

- NEVER modify files in `data/raw/`
- ALWAYS load raw data and write outputs to:
  - `data/intermediate/`
  - `data/processed/`

---

### 3. Stepwise Processing

Pipelines should follow a clear sequence:

1. Load raw data
2. Clean missing values
3. Harmonize variable names and formats
4. Reshape data (wide → long if needed)
5. Construct derived variables
6. Save intermediate outputs (optional)
7. Save final dataset to `data/processed/`

---

### 4. Modular Scripts

- Each script should perform a clear task
- Avoid monolithic scripts
- Prefer:
  - `build_dataset_name.R`
  - `clean_dataset_name.py`

---

## File Naming Conventions

- Build scripts:
  - `build_psid_panel.R`
  - `build_nlsy_dataset.py`

- Intermediate outputs:
  - `psid_panel_intermediate.parquet`

- Final outputs:
  - `psid_panel_processed.parquet`

---

## Data Standards

All processed datasets should:

- Use consistent variable names (snake_case)
- Avoid encoded missing values (e.g., -9, -1)
- Use explicit NA/null values
- Be in tidy format when possible:
  - one row per unit per time
  - one column per variable

---

## Logging and Transparency

Each pipeline script should:

- Print or log key steps:
  - number of observations
  - number of variables
  - missing value summary
- Clearly indicate output file location

---

## Error Handling

- Fail loudly if:
  - required variables are missing
  - input files are not found
- Do NOT silently continue with incorrect data

---

## Agent Instructions

When building or updating a dataset:

1. Identify required variables from `kb/codebooks/`
2. Load raw data from `data/raw/`
3. Apply cleaning and transformations
4. Create derived variables if needed
5. Save output to `data/processed/`
6. Ensure reproducibility

If a processed dataset already exists:
- Prefer updating the pipeline rather than manually editing data

---

## What NOT to Do

- Do NOT analyze data in this directory
- Do NOT manually edit datasets
- Do NOT save outputs outside the data folder
- Do NOT overwrite raw data

---

## Principle

This directory is the only place where data transformation logic should exist.

All analysis must depend on outputs generated here.