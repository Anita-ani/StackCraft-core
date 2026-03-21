# Critical Production

**Budget:** Highly variable; often **$2,000–$10,000+** monthly infrastructure before dedicated staffing.

## Purpose

Workloads with **high blast radius**, strict contractual recovery expectations, or **regulatory pressure**: HA data paths, tested disaster recovery, formal access lifecycle, and incident programs that match organizational scale.

## Key characteristics

- Redundancy and DR aligned to explicit RTO/RPO
- Strong identity, audit, and third-party risk discipline
- Error budgets and leadership-level review of reliability
- Evidence-oriented operations (tested restores, drills)

## Sections

| Document | Description |
|----------|-------------|
| [architecture.md](architecture.md) | HA topology and DR posture |
| [budget.md](budget.md) | Replication, retention, support tiers |
| [team-fit.md](team-fit.md) | 24/7 or follow-the-sun coverage |
| [operations.md](operations.md) | Change control and audit trail |
| [observability.md](observability.md) | SLO programs and security monitoring |
| [security.md](security.md) | Zero-trust patterns, data classification |
| [backups.md](backups.md) | Immutable backups and automated restore verification |
| [tradeoffs.md](tradeoffs.md) | Cost, process, and velocity |
| [upgrade-triggers.md](upgrade-triggers.md) | Beyond this reference (cell architecture, multi-region active/active, formal compliance programs) |

## When to use

- Explicit customer or regulatory recovery requirements
- Large revenue or safety impact from extended outage
- Organizational maturity to operate the controls, not only deploy the tools

## When to move on

See [upgrade-triggers.md](upgrade-triggers.md). Further evolution is **organization- and policy-specific**; this repository does not replace enterprise architecture or compliance programs.

**Blueprint:** [high-reliability-production](../../blueprints/high-reliability-production.md)

**Industry context:** [stackcraft-sectors](../../../stackcraft-sectors/)
