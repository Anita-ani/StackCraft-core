# Growth Production Budget

**Last reviewed:** 2026-03-21

## Typical range

Roughly **$800–$2,000+ / month** (USD, indicative). Upper bound rises quickly with HA databases, heavy egress, premium observability, or large autoscale ceilings.

## Budget areas

- Compute (app instances, workers, autoscale minimums)
- Load balancer and fixed networking fees
- Managed database (instance size, storage, optional replicas / failover)
- Cache and queues (if used)
- Observability (logs volume, metrics cardinality, tracing)
- DNS, CDN, WAF
- CI/CD runners and artifact storage
- Backups and archive storage

## Example allocation (illustrative)

| Area | Indicative monthly band |
|------|-------------------------|
| App compute (multi-instance / autoscale floor) | $200–$600 |
| Load balancer + egress buffer | $50–$200 |
| Managed DB (+ optional replica / HA) | $200–$800 |
| Cache / queue | $50–$300 |
| Monitoring, logs, tracing | $50–$250 |
| CDN / DNS / WAF | $50–$200 |
| CI/CD + artifacts | $30–$150 |
| Backups / object storage | $40–$150 |

Adjust for region, reserved capacity, and traffic shape.

## Watchouts

- **Metrics label cardinality** — unbounded dimensions inflate cost and degrade performance.
- **Egress** during spikes or misconfigured logging.
- **Autoscale max** without a cap — bill shock during attacks or bugs.
- **Fixed LB + WAF** fees that do not scale down with traffic.

## Template

[../../templates/budget-template.md](../../templates/budget-template.md)
