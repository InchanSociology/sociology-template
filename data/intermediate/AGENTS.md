# Intermediate Data Rules

This folder stores temporary data generated during data processing.

## Purpose

- Store partially cleaned data
- Store merged or reshaped datasets
- Store step-by-step pipeline outputs

## Rules

- Files here are not final
- Files may be deleted or regenerated at any time
- Do NOT use these datasets for final analysis

## Reproducibility

All files in this folder must be reproducible from:
- `data/raw/`
- scripts in `script/data_pipeline/`

## Examples

- merged datasets
- reshaped panel data
- filtered subsets
- partially cleaned files

## Agent Instructions

- You may read from this folder ONLY if:
  - explicitly part of a pipeline step
- Do NOT treat this as analysis-ready data
- Prefer `data/processed/` whenever possible