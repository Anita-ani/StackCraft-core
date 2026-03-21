# Starter — observability

## Minimum requirements

- **Logs** must be accessible (app + reverse proxy; `journalctl` / `docker logs` is enough to start).  
- **Basic metrics** — CPU, memory, disk on the host.  
- **Uptime monitoring** — synthetic check against your public URL or `/health`.  
- **Alerting** on failures — you must *notice* when things break.

## Tools (examples)

- **Grafana** (self-hosted or Grafana Cloud) — optional but useful for dashboards.  
- **Uptime** services (many have free tiers).  
- **System logs** — `journalctl`, Docker logging driver, or vendor metrics in the cloud console.

## What to track

- CPU usage  
- Memory usage  
- Disk usage  
- Application errors (rate or log-based)  
- HTTP response status / error rate  

## Alerts (start here)

- Server or health check **down**  
- **High CPU** sustained (tune threshold after a week of data)  
- **Disk near full** (before 90% if possible)  
- **5xx spike** or elevated error logs  

## Dashboards

One **RED-style** view is enough at Starter: rate, errors, duration (even if rough).

See [../../checklists/observability-checklist.md](../../checklists/observability-checklist.md).
