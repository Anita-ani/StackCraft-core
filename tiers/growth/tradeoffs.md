# Growth Production Tradeoffs

## What you gain

- **Improved availability** for the application tier (multi-instance, LB health checks).
- **Safer deployments** (rolling / blue-green / canary, rollback discipline).
- **Better observability** and faster **incident response** when tracing and SLO-style metrics exist.
- **Ability to handle traffic growth** via horizontal scale and async offload.
- **Stronger edge posture** (CDN, WAF) when implemented.

## What you still lack (vs Critical / enterprise)

- **Multi-region** or **active/active** patterns are not assumed at this tier.
- **Advanced compliance** programs (formal control frameworks, dedicated GRC tooling) may still be missing.
- **Full platform engineering** layers (golden paths for every service, large internal developer platforms) may not exist yet.

## Cost impact

**Higher baseline spend** than Lean: redundancy, load balancers, observability volume, and managed HA options add fixed and variable cost. The return is **predictability** and **lower surprise downtime** when the team operates the stack well.

## Key message

**Growth Production** is where systems become **resilient under growth**, not merely functional.

## Related

- [upgrade-triggers.md](upgrade-triggers.md)
- [budget.md](budget.md)
