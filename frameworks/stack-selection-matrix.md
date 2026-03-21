# Stack selection matrix

Use this **after** PRI ([production-risk-index.md](production-risk-index.md)) and team size ([../docs/03-team-size-models.md](../docs/03-team-size-models.md)).

## Axes

| Axis | Questions |
|------|-----------|
| **Traffic pattern** | Steady vs spiky? Global vs single region? |
| **Data** | One DB vs many? Strong consistency needs? |
| **Team ops hours** | Who is paged? 24/7 or business hours? |
| **Change frequency** | Many deploys/day vs weekly? |

## Tier quick map

| Signal | Lean toward |
|--------|-------------|
| 1 engineer, low PRI | [Starter](../tiers/starter/) |
| 2–5 engineers, staging needed | [Lean](../../stackcraft-lean-production/README.md) |
| Spikes, queues, multi-service | [Growth](../tiers/growth/) |
| High PRI or contractual DR | [Critical](../tiers/critical/) |

## Sector override

Always cross-check **[stackcraft-sectors](../../stackcraft-sectors/matrices/sector-vs-budget.md)**.
