# Budget tiers

Plan cloud spend like any budget: **line items**, **assumptions**, and a **buffer**.

## Line items (every estimate)

1. Compute / runtime  
2. Database  
3. Storage and backups  
4. Networking (egress, LB)  
5. Observability (metrics, logs, traces)  
6. Alerting and on-call tooling  
7. DNS / CDN / edge security  
8. CI/CD  
9. Contingency (often 10–25%)  

## Three numbers

For each environment:

- **Minimum viable** — keeps the lights on.  
- **Comfortable** — staging (where applicable), monitoring, room for spikes.  
- **Cost of underinvesting** — downtime, recovery time, reputation (qualitative is fine).

## Indicative monthly bands (USD, verify live pricing)

| Tier | Typical range | Notes |
|------|----------------|-------|
| Starter | ~$75–$300 | Single region, small footprint |
| Lean | ~$400–$700 | Prod + staging, better observability |
| Growth | ~$800–$2k+ | Scale events, queues, WAF-class controls |
| Critical | $2k–$10k+ common | HA/DR, long retention, enterprise patterns |

**Industry overrides raw budget.** See [08-sector-decision-framework.md](08-sector-decision-framework.md) and [stackcraft-sectors](../../stackcraft-sectors/).

## Date your numbers

Cloud prices change. Each tier’s [budget.md](../tiers/starter/budget.md) (and your spreadsheets) should note **last reviewed**.

## Next

[03-team-size-models.md](03-team-size-models.md)
