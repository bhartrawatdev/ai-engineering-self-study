# CS104 — Main Project: Modular ETL Pipeline Framework

This is the standalone spec for CS104's Main Project (also summarized in `CS104.md`). Use this file as your working checklist while building.

## Description

A small, extensible framework for building data pipelines (Extract → Transform → Load), designed specifically to demonstrate composition, the Strategy pattern, type hints, and real test coverage. This project exists to prove the course's design principles hold up under an actual build, not just in isolated exercises — and to directly preview the kind of data pipeline work coming in ML102.

## Requirements

- [ ] Define abstract base classes (or protocols) for `Extractor`, `Transformer`, and `Loader`, each with a clear, minimal required interface.
- [ ] Implement at least 2 concrete extractors (e.g. from CSV, from JSON).
- [ ] Implement at least 2 concrete transformers (e.g. filtering rows, normalizing a column).
- [ ] Implement at least 2 concrete loaders (e.g. write to CSV, print summary to console).
- [ ] Build a `Pipeline` class that composes one extractor, a list of transformers, and one loader — swappable without modifying `Pipeline` itself.
- [ ] Fully type-hint the framework and confirm it passes `mypy` with no errors.
- [ ] Write a `pytest` test suite covering each extractor, transformer, and loader independently, plus at least one full end-to-end pipeline test.
- [ ] Package the project properly: `pyproject.toml`, installable locally via `pip install -e .`, with a clear README.

## Suggested File Layout

```
etl-pipeline/
├── pyproject.toml
├── README.md
├── src/
│   └── etl_pipeline/
│       ├── __init__.py
│       ├── extractors.py     ← Extractor ABC + concrete implementations
│       ├── transformers.py   ← Transformer ABC + concrete implementations
│       ├── loaders.py        ← Loader ABC + concrete implementations
│       └── pipeline.py       ← the Pipeline class composing the above
└── tests/
    ├── test_extractors.py
    ├── test_transformers.py
    ├── test_loaders.py
    └── test_pipeline.py       ← end-to-end test(s)
```

## Stretch Goals

- [ ] Add a simple plugin-discovery mechanism (a registry dict mapping names to transformer classes) so new transformers can be added and selected by name without editing `Pipeline`.
- [ ] Add an Observer-pattern-based logging/progress system reporting on each pipeline stage as it runs, without `Pipeline` needing to know about logging directly.
- [ ] Add a `--config` CLI option (via `argparse`) that builds a pipeline from a JSON/YAML config specifying which extractor/transformers/loader to use.

## What "Done" Looks Like

- Any extractor, transformer, or loader can be swapped for a different implementation without modifying the `Pipeline` class — proving the Open/Closed principle is actually being honored, not just claimed.
- `mypy` and the full `pytest` suite both pass cleanly.
- The project installs locally via `pip install -e .` and can be imported/run from any directory.
- Pushed to this repo's `Projects/` folder with a README explaining the architecture and how to add a new extractor/transformer/loader.

## Notes on Test Data

Use small, synthetic CSV/JSON files you generate yourself (a handful of rows is plenty) — the point of the test suite is verifying the framework's behavior and edge-case handling, not processing large real datasets. Real-scale data pipeline concerns are ML102's job, not this course's.
