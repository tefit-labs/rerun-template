# <Idea name>: rerun

Rerun of **<idea>** (<originators, year, paper link>). Catalogue entry: `https://github.com/tefit-labs/tefit/blob/main/catalogue/ideas/<slug>.md`

> **Status: in progress / unreviewed / reviewed by <name> on <date>.**

## Question

One sentence: what this rerun tests, and what number would count as a signal.

## Run it

    ./get_data.sh          # if the rerun needs data; downloads into ./data (not committed)
    python3 run_all.py     # every run, resumable, one JSON-lines log per run in logs/
    python3 summarise.py   # prints every table in RESULTS.md from the logs

## Files

- `train.py`: the model and one training run.
- `run_all.py`: the full grid: tuning runs, selection on validation, then seeds on test.
- `summarise.py`: reads `logs/` and prints the tables. `RESULTS.md` holds nothing else.
- `logs/`: raw logs, committed, including failed runs.

## Requirements

Python version, packages, hardware used, and wall-clock time for the full grid.

## AI assistance

What was written or run by a model, and what a person has checked.

## Rules

This repo follows the [tefit rerun rules](https://github.com/tefit-labs/.github/blob/main/CONTRIBUTING.md#rerun-rules).
