# Risk-based thinking

The same monthly spend can be **responsible** for one product and **irresponsible** for another. Risk—not just traffic—should drive architecture.

## Production Risk Index (PRI)

Full rubric: [`../frameworks/production-risk-index.md`](../frameworks/production-risk-index.md).

In short, score **1–5** on:

- Data sensitivity  
- Downtime / revenue impact  
- Compliance exposure  
- Integrity / fraud risk  

**Higher average → stricter baselines**, often **before** you add headcount.

## Tier vs sector

- **Tier** (Starter → Critical) = operational **maturity** and **scale** of your platform.  
- **Sector** = business **context** (FinTech, health, etc.) in [stackcraft-sectors](../../stackcraft-sectors/).

You need **both**: a FinTech MVP might need **Lean** or higher even at low traffic.

## Honest tradeoffs

Document what you are **not** buying yet (e.g. multi-region, formal SOC2 program). Revisit when PRI or revenue changes.

## Next

[05-production-readiness-checklist.md](05-production-readiness-checklist.md)
