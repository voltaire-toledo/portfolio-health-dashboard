# Portfolio Health Dashboard

A zero-compute, centralized telemetry and health vital signs flowsheet for repository portfolios, hosted on **GitHub Pages** with an **Azure Function + Cosmos DB** telemetry ingestion backend.

## Architecture

- **Frontend**: Lightweight static dashboard hosted on GitHub Pages (`index.html`).
- **Telemetry Ingestion**: Azure Function (`/api/telemetry`) accepting JSON vitals from nodes (workstations, dev containers, laptops).
- **Central Ledger**: Azure Cosmos DB (Free Tier: 1,000 RU/s & 25 GB storage).
- **Public API**: Azure Function (`/api/fleet`) serving cached portfolio telemetry to the GitHub Pages frontend.

## Local Development

```bash
# Serve locally
python -m http.server 8000
```
