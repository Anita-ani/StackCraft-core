# Blueprint: high-reliability production

**Intent:** HA data paths, **tested** DR, formal access and incident programs—aligned with high PRI or strict contracts.

## When it fits

- Regulatory pressure, large revenue at risk, or explicit customer DR clauses.

## Characteristics

- Multi-AZ / multi-region per requirements—not by default.  
- Automated restore verification; chaos or game days.  
- SSO, least privilege, audit logging for sensitive actions.

**Tier:** [Critical](../tiers/critical/README.md).
