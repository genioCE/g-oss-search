# g-oss-search · Search & log analytics (OpenSearch)

**Audience:** O&G CIOs/CTOs and platform/search owners  
**Goal:** Provide search/log analytics without Elastic’s licensing constraints.

---

## Executive summary
- **What it is:** **OpenSearch** + **Dashboards** for log and document search.  
- **What it replaces:** Elastic Stack (non‑OSS licensing), or Splunk for certain log/search workloads.
- **Outcomes:** Lower TCO for search, with dashboards and alerts.

## Where it fits
```
[Apps/Agents/Promtail] ──> OpenSearch ──> Dashboards
```
Use alongside Loki/Grafana (`g-oss-observability`) or as the primary log search.

## O&G use cases
- Search SCADA gateway logs for dropouts.  
- Vendor file‑drop monitoring and anomaly triage.  
- Document search across well PDFs (with ingestion pipeline add‑ons).

## Security & compliance
- Native users/roles; integrate SSO behind a proxy.  
- Index lifecycle policies to control storage cost and retention.

## KPIs for leadership
- Query latency p95, indexed GB/day vs. budget, alert coverage.

## Quick start
```bash
docker compose up -d
# OpenSearch: http://localhost:9200  • Dashboards: http://localhost:5601
```
