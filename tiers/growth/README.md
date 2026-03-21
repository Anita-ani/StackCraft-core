# Growth Production

**Budget:** $800+ (indicative; often **$800–$2,000+** before large HA spend — verify live pricing).

## Purpose

A production system for **growing teams** that need systems to behave more like a **platform** than a single application: availability under load, safer deploys, structured observability, and reduced blast radius. This is not enterprise multi-region by default; it is **resilient, single-region (or primary-focused) production** with room to scale.

## Who this is for

- Roughly **5–15 engineers** (or equivalent operational load)
- Growing startup or scale-up with **revenue- or trust-sensitive** uptime
- **Frequent deployments** and increasing operational complexity
- Products where traffic spikes, multi-service boundaries, or tenant noise push past Lean patterns

## Core characteristics

- **Multiple application instances** (containers or VMs) behind a load balancer
- **Managed data tier** preferred; **failover or HA** where the business justifies cost
- **Staging** and often **pre-production** (or prod-like preview) for risky changes
- **CI/CD** with a **safe deployment strategy** (rolling, blue/green, or canary) and mandatory rollback
- **Structured observability**: centralized logs, metrics, alerting; **distributed tracing** where it pays off
- **Automated backups** and clearer recovery expectations than Lean
- **Basic redundancy** for critical paths (not vanity HA)

## Lean → Growth (main shift)

| Lean | Growth |
|------|--------|
| Single app instance may suffice | Multiple instances behind load balancing |
| Basic monitoring | Structured observability (logs + metrics; tracing common) |
| Recovery often manual | More **automated** restart, scaling, and recovery patterns |
| Simple deploys | **Zero- or near-zero-downtime** deploy patterns expected |
| Limited redundancy | **Redundancy** introduced for app and often data tier |

## What matters most

- **Availability** and graceful handling of load
- **Deployment safety** and fast rollback
- **Operational clarity** (ownership, runbooks, observable failure modes)
- **Reduced blast radius** (isolation, staged rollouts)

## What is acceptable

- **Single-region** architecture (with strong backups and runbooks)
- **Partial** redundancy (e.g. multi-instance app, single primary DB with failover option)
- **Managed** failover rather than self-built active/active everywhere

## What is not acceptable

- **Single point of failure** in core user-facing paths when the tier budget allows mitigation
- No meaningful **monitoring and alerting**
- **Production deploys** without a **rollback** path and traceability

## Sections

| Document | Description |
|----------|-------------|
| [architecture.md](architecture.md) | Topology: LB, app cluster, data, async paths |
| [budget.md](budget.md) | Line items, autoscale and egress watchouts |
| [team-fit.md](team-fit.md) | Service ownership and platform touchpoints |
| [operations.md](operations.md) | Deploy patterns, capacity, incidents |
| [observability.md](observability.md) | Logs, metrics, tracing, SLO-oriented alerts |
| [security.md](security.md) | WAF, private connectivity, access lifecycle |
| [backups.md](backups.md) | PITR, restore testing, async replay awareness |
| [tradeoffs.md](tradeoffs.md) | Gains vs remaining limits |
| [upgrade-triggers.md](upgrade-triggers.md) | When to adopt Critical tier |

## When to move on

See [upgrade-triggers.md](upgrade-triggers.md).

**Blueprint:** [growth-production](../../blueprints/growth-production.md)

**Industry context:** [stackcraft-sectors](../../../stackcraft-sectors/)

**Prior tier:** [stackcraft-lean-production](../../../stackcraft-lean-production/README.md)
