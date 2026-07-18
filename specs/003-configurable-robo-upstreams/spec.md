# Configurable local Robo upstreams

## Goal

Allow the local Workspace launcher to select reservation-safe Analyzer and
Catalog ports without changing Docker service ports.

## Contract

- Local Analyzer routes use `ROBO_ANALYZER_URL`, defaulting to the legacy
  `http://127.0.0.1:5502` endpoint.
- Local Catalog routes use `ROBO_CATALOG_URL`, defaulting to the legacy
  `http://127.0.0.1:5503` endpoint.
- Both gateway-prefixed and direct routes use the same variables.
- Architect web on port 15173 is accepted by the explicit CORS filter.
- Docker profile routing remains unchanged.
