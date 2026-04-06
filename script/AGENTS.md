# Script Directory Rules

This directory contains all project scripts for data processing, analysis, and visualization.

## Purpose

- Store reproducible research code
- Separate data transformation from analysis
- Keep workflows modular and transparent

## Structure

Common subdirectories may include:

- `data_pipeline/` for raw-to-processed data construction
- `analysis/` for statistical models and estimation
- `visualization/` for figures and plots
- `utils/` for helper functions

Not every project must use the same file names or the same subdirectory structure.
Choose a structure that fits the project, but keep it clear and reproducible.

## Core Principles

### 1. Reproducibility First

- All results must be reproducible through code
- No manual editing of analytic outputs
- No undocumented transformations

### 2. Separate pipeline from analysis

- Data transformation belongs in `script/data_pipeline/`
- Statistical modeling belongs in analysis scripts
- Visualization should be separate from raw data construction when possible

### 3. Prefer modular scripts

- Each script should have a clear purpose
- Avoid large monolithic files
- Use descriptive file names

Examples:
- `build_panel.py`
- `run_main_models.R`
- `make_figure_1.py`

### 4. Flexible workflow, clear logic

A project may follow a sequence such as:

1. import raw data
2. clean and harmonize
3. construct variables
4. run analysis
5. generate tables and figures

This logic is recommended, but exact filenames do not need to follow a fixed `00-04` pattern.

## Agent Instructions

- Read the most specific `AGENTS.md` in the relevant subdirectory
- Do not mix data construction and substantive analysis in one script unless the project is very small
- Prefer updating scripts rather than manually editing outputs

## Principle

The script directory should make it easy to see:
- where data are built
- where models are run
- where outputs are generated

- All analysis must use datasets from `data/processed/`, not directly from raw data