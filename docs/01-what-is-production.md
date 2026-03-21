# What is production?

**Production** is the environment where workloads are **customer- or business-critical**: outages and data loss have real cost, and change must be controlled.

Hosting is a subset of the problem. Production engineering is about **operating under failure and change**: detection, response, recovery, and learning.

## Minimum bar

A system in production should support:

- **Observation** — enough telemetry to detect regressions and incidents
- **Recovery** — backups and restore procedures that have been exercised
- **Access control** — least privilege for humans and automation
- **Predictability under load** — known capacity limits and a plan when they are hit

Detailed criteria: [05-production-readiness-checklist.md](05-production-readiness-checklist.md).

## Further reading

- Budget and tier selection: [02-budget-tiers.md](02-budget-tiers.md)
- Risk framing: [04-risk-based-thinking.md](04-risk-based-thinking.md)
