# Core Contribution Files

## Core Method
- `aeri_agent/agent.py`: AERI scoring agent — sends structured prompt to Claude Code CLI with repo evidence
- `aeri_agent/cli.py`: CLI entry point (`aeri-score` command)

## Evidence Gathering (rule-based)
- `aeri_agent/analyzers/structure.py`: File structure analysis
- `aeri_agent/analyzers/dependencies.py`: Dependency and environment feasibility analysis
- `aeri_agent/repo_fetcher.py`: Repository cloning

## Report Generation
- `aeri_agent/report.py`: Score report (JSON + Markdown) with recommendations

## Examples
- `examples/`: AERI scoring outputs for real repositories

