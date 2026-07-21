# CS105 — Main Project: ML Experiment Tracker (Database-Backed)

This is the standalone spec for CS105's Main Project (also summarized in `CS105.md`). Use this file as your working checklist while building.

## Description

A small database-backed CLI tool for logging and querying machine learning experiment runs — hyperparameters, metrics, and metadata — designed as a properly normalized relational schema with both raw SQL and ORM access paths. Unlike most course projects, this one is meant to actually get used: you'll have real, hands-on need for exactly this kind of tracking starting with ML101.

## Requirements

- [ ] Design a normalized schema (at least 3 tables) representing:
  - Experiments/runs
  - Hyperparameters (allowing an arbitrary, varying set of names/values per run — avoid repeating-group columns)
  - Metrics (allowing multiple metrics per run, potentially at different steps/epochs)
- [ ] Implement a Python CLI tool (`argparse`) supporting at minimum:
  - [ ] Logging a new run with its hyperparameters
  - [ ] Logging a metric value for an existing run
  - [ ] Querying/listing runs with filtering (e.g. "runs with validation accuracy above X")
- [ ] Implement the core CRUD operations using raw parameterized `sqlite3` SQL.
- [ ] Implement the same core operations a second way, using SQLAlchemy's ORM, as a separate module.
- [ ] Include at least one deliberately indexed column and confirm via `EXPLAIN QUERY PLAN` that it's used.
- [ ] Wrap any multi-step write operation (e.g. logging a run plus all its hyperparameters) in a transaction.

## Suggested File Layout

```
ml-experiment-tracker/
├── schema.sql              ← CREATE TABLE statements, normalized schema
├── db_raw.py                 ← raw sqlite3 CRUD operations (parameterized queries)
├── db_orm.py                   ← SQLAlchemy ORM models + equivalent operations
├── cli.py                        ← argparse CLI tying it together
├── experiments.db                 ← the SQLite database file (gitignored if it contains only test data, or committed with sample data — your call)
├── requirements.txt
└── README.md                        ← schema explanation + how to use the CLI
```

## Stretch Goals

- [ ] A "compare runs" command showing two or more runs' hyperparameters and metrics side by side.
- [ ] Export query results (e.g. runs sorted by best validation metric) to CSV.
- [ ] Store a fake "run embedding" (random vector) per run and implement a "find similar runs" command using brute-force nearest-neighbor search.

## What "Done" Looks Like

- The schema is properly normalized — no repeating hyperparameter/metric columns — and you can explain which normal form violations your design specifically avoids.
- Both the raw-SQL and SQLAlchemy-ORM code paths work correctly and produce identical results for the same operations.
- You can log a handful of realistic-looking experiment runs and successfully query/filter/compare them through the CLI.
- Pushed to this repo's `Projects/` folder with a README explaining the schema design and how to use the CLI.

## Notes on Schema Design

Think carefully about the hyperparameters table before writing any SQL — since different experiment types will have completely different hyperparameter names (e.g. `learning_rate` for one run, `n_estimators` for another), a single `run_hyperparameters` table with `run_id`, `param_name`, `param_value` columns (an entity-attribute-value pattern) handles this far better than trying to anticipate every possible hyperparameter as a fixed column. This is a deliberate, realistic design decision worth reasoning through rather than rushing.
