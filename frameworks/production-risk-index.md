# Production Risk Index (PRI)

Score your workload **1–5** (higher = stricter requirements) on each axis:

| Axis | 1 (low) | 5 (high) |
|------|---------|----------|
| **Data sensitivity** | Public marketing | Health/financial PII, credentials |
| **Downtime $ impact** | Annoyance | Revenue loss or SLA penalties |
| **Compliance exposure** | Light / none | HIPAA, PCI, SOC2 customer demands |
| **Integrity / fraud risk** | Read-only content | Money movement, ledger, auth abuse |

**Composite PRI (rough):** average of the four scores.

## Interpretation

- **PRI ≤ 2** — broader stack choices; **Starter** may fit if backups and deploy are disciplined.  
- **PRI ~ 3** — **Lean** or **Growth** patterns; managed DB and audit logging become defaults.  
- **PRI ≥ 4** — **Critical** patterns; segmentation, strong IAM, formal DR; budget may jump **regardless of traffic**.

## Pair with sectors

Industry-specific floors live in **[stackcraft-sectors](../../stackcraft-sectors/)**.
