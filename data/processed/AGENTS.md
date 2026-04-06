# Processed Data Rules

This folder contains final, analysis-ready datasets.

## Purpose

- Cleaned and validated data
- Harmonized variables
- Reduced to relevant features
- Ready for modeling and analysis

## Requirements

Datasets in this folder must be:

- Clean (no raw missing codes like -9, -1)
- Structured (e.g., tidy/long format when appropriate)
- Documented (variable meaning should be clear)

## Reproducibility

Every dataset must be reproducible from:

- `data/raw/`
- via scripts in `script/data_pipeline/`

If not reproducible:
- it should not be trusted

## Restrictions

- Do NOT manually edit files
- Do NOT create datasets without scripts
- Do NOT store temporary files here

## Agent Instructions

- ALWAYS use data from this folder for analysis
- NEVER use `data/raw/` directly
- Only use `data/intermediate/` if explicitly required

## Principle

This is the single source of truth for all analysis.