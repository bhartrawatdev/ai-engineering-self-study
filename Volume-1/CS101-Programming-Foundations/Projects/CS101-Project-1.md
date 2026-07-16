# CS101 — Main Project: Command-Line Log Analyzer

This is the standalone spec for CS101's Main Project (also summarized in `CS101.md`). Use this file as your working reference while building.

## Description

A CLI tool that reads a synthetic log file (`timestamp | level | message` format, e.g. `2026-01-15 08:32:11 | ERROR | Connection timeout`) and produces a summary report. This project exists to force integration of everything from the course — functions, classes, file I/O, error handling, the standard library, and a real CLI interface — into one coherent program instead of isolated exercises.

## Requirements

- [ ] Accept the log file path as a command-line argument via `argparse`.
- [ ] Parse each line of the log file into a structured record.
- [ ] Handle malformed lines gracefully — log/skip them, never crash on bad input.
- [ ] Report:
  - [ ] Total line count
  - [ ] Count by log level (`INFO` / `WARNING` / `ERROR` / etc.)
  - [ ] The 5 most common error messages
  - [ ] The busiest hour of the day (most log entries)
- [ ] Support an `--output` flag to write the report as JSON instead of printing to the console.
- [ ] Represent each parsed log entry as a small class — not a raw dictionary or tuple.
- [ ] Include at least one custom exception (e.g. `MalformedLogEntryError`) that you raise and catch deliberately, rather than relying only on built-in exceptions.

## Stretch Goals

- [ ] Add a `--level` filter flag to only report on a specific log level.
- [ ] Support a second, differently-formatted log file (e.g. a real-world format like nginx access logs) using regex, parsed by the same tool.
- [ ] Use NumPy to compute basic statistics (e.g. average log entries per hour) instead of hand-rolled loops.

## Suggested File Layout

```
log-analyzer/
├── log_analyzer.py     ← CLI entry point, argparse, orchestration
├── models.py           ← LogEntry class, custom exceptions
├── sample.log           ← synthetic test data you generate yourself
├── requirements.txt
└── README.md            ← how to run it
```

## What "Done" Looks Like

- Running `python log_analyzer.py sample.log` produces a readable console report with no crashes on malformed input.
- The code is split across at least two files, imported properly as a module — not one giant script.
- You can explain every line of your own code without hesitation if asked.
- A short `README.md` inside this project's folder describes how to run it.

## Generating Test Data

Don't hand-write hundreds of log lines. Use a short throwaway Python script with `random` and `datetime` to generate a `sample.log` with a mix of valid entries across all log levels, plus a deliberate handful of malformed lines (missing fields, bad timestamps, extra pipes) to actually exercise your error handling.
