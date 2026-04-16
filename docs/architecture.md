# Architecture

## Problem framing

- User: Pricing science and ML platform teams
- Problem: Pricing models degrade when online features become stale or drift away from the offline training view.
- Decision: Keep pricing features fresh enough for ranking and price optimization models to act safely.

## System flow

1. A user submits case context, business signals, or a search question.
2. The API exposes scoring, analysis, and recommendation endpoints.
3. The web application turns those outputs into an operator-facing workflow.
4. Observability, docs, and runbooks make the project easier to evaluate and extend.

## Production posture

- Separate app, docs, demo, and data folders
- Container-ready packaging
- API endpoints for health and workflow actions
- Screenshot-ready demo surface
- Research and upstream audit artifacts included in-repo
