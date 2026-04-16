# Real-Time Pricing Feature Platform

![Demo Screenshot](demo/screenshot.png)

## Overview

Serve low-latency pricing and demand features to ranking and pricing models while tracking freshness and training-serving consistency.

## Real-world problem

- User: Pricing science and ML platform teams
- Problem: Pricing models degrade when online features become stale or drift away from the offline training view.
- Decision improved: Keep pricing features fresh enough for ranking and price optimization models to act safely.
- KPI target: Improve feature freshness and pricing decision quality.

## Why this matters

This repo is positioned as a real product for a real team, not a framework-only demo. The goal is to show how research-backed AI, analytics, or graph systems become deployable workflows with docs, UI, screenshots, and business-facing outputs.

## Project profile

- Domain: Commerce ML Platform
- Project type: `ml`
- Tags: pricing, feature-store, mlops, commerce

## Workflow

1. Ingest the operational context for the user and case.
2. Score risk, quality, or opportunity using the project API.
3. Compare current signals against a business baseline.
4. Generate a recommendation or operator brief for the next step.

## Quick start

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python scripts/bootstrap_data.py
uvicorn src.app.main:app --host 0.0.0.0 --port 8000 --reload
```

Open `http://localhost:8000/` to use the interactive application.

## Key endpoints

- `GET /`
- `GET /health`
- `GET /bootstrap`
- `GET /project`
- `POST /score`
- `POST /analyze`
- `POST /query`
- `POST /recommend`

## Documentation

- [Architecture](docs/architecture.md)
- [Evaluation](docs/evaluation.md)
- [Runbook](docs/runbook.md)
- [Innovation memo](research/innovation_memo.md)
- [Upstream audit](research/upstream_audit.md)
