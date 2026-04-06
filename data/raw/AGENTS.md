# Raw Data Rules

This folder contains original, unmodified data.

## Strict Rules

- NEVER edit, rename, or overwrite any file in this directory.
- NEVER save new files into this directory unless they are original source data.
- NEVER perform analysis using data directly from this folder.

## What belongs here

- Original downloads (e.g., surveys, administrative data)
- Vendor-provided datasets
- Direct exports from external systems

## Integrity Principle

Files in this folder must remain identical to their original source.

If any transformation is needed:
- create a script in `script/data_pipeline/`
- output results to `data/intermediate/` or `data/processed/`

## Agent Instructions

- Treat this directory as read-only
- Do NOT load data from here for analysis
- Only reference for building pipelines