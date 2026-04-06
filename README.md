# Sociology Research Template

An AI-assisted sociology research template for reproducible, modular, and well-documented projects.

## Purpose

This repository is designed to support sociology research workflows from project planning to data processing, analysis, and writing.

It is especially useful for projects that combine:

- clear project organization
- reproducible data workflows
- AI-assisted coding and writing
- modular research documentation

## Directory Overview

- `data/`  
  Data storage, organized into raw, intermediate, and processed layers

- `kb/`  
  Project knowledge base, including concepts, methods, data documentation, codebooks, and promptbooks

- `memory/`  
  Project memory, including decisions, progress, open questions, and change logs

- `script/`  
  Reproducible code for data pipelines, analysis, and visualization

- `output/`  
  Generated tables, figures, models, and other outputs

- `writing/`  
  Manuscript materials, including outlines and section drafts

## Project Philosophy

This template separates three functions:

- Rules  
  Stable instructions about how the project should be organized and maintained

- Memory  
  Evolving records of project decisions, progress, and open questions

- Knowledge  
  Accumulated concepts, literature, methods, and data documentation

## Suggested Workflow

1. Define the research question in `writing/outline.md`
2. Record decisions and open questions in `memory/`
3. Document concepts, literature, and data in `kb/`
4. Build datasets through `script/data_pipeline/`
5. Store analysis-ready data in `data/processed/`
6. Run analysis scripts from `script/`
7. Draft the manuscript in `writing/sections/`

## Notes

- Treat `data/raw/` as read-only
- Keep all transformations reproducible through scripts
- Use the most specific `AGENTS.md` file that applies to the file you are editing