# Lean Production ($400–$700)

**StackCraft: Lean Production** is a **standalone module**. It is not folded into StackCraft Core; Core links here for navigation and upgrade paths.

**Budget:** $400–$700 per month (indicative; verify current pricing).

This is the tier where you stop treating production as “just hosting an app” and start running a **more disciplined** environment.

## Good fit

- Small startup teams
- Products with active users
- Systems where downtime is painful
- Teams that need staging, better monitoring, and safer deployments

**Key message:** Starter Production is about **survival**. Lean Production is about **control**. Production becomes **collaborative** and **operationally intentional**.

## Positioning: what changes from Starter to Lean

- From **single-box thinking** to **separated responsibilities**
- From **basic uptime** to **actual observability**
- From **manual deploy and pray** to a **safer deployment flow**
- From **backup exists** to **deliberate recovery planning**

## What a Lean stack should usually include

- Separate app and database layers
- Staging environment
- Managed database (preferred)
- Central logging
- Metrics and alerting
- CI/CD pipeline
- Better secret handling
- Backup policy with retention
- Basic runbooks

## Who this is for

- Small engineering teams
- Startups with active users
- Products where downtime impacts trust or revenue

## Core characteristics

- Separate application and database layers
- Staging environment
- Managed services preferred
- Better observability
- Safer deployments

## What matters most

- Deployment safety
- Visibility into failures
- Backup reliability
- Team-friendly operations

## What is acceptable

- Single production app node in some cases
- Managed database without HA
- Moderate manual operations

## What is NOT acceptable

- Deploying directly without a rollback plan
- No staging environment
- No centralized logs
- No alerts for critical failures

## Documentation

| Document | Description |
|----------|-------------|
| [architecture.md](architecture.md) | Topology and components |
| [budget.md](budget.md) | Typical range and allocation |
| [operations.md](operations.md) | Practices and deploy expectations |
| [observability.md](observability.md) | Logs, metrics, alerts |
| [security.md](security.md) | Baseline and recommended controls |
| [backups.md](backups.md) | Policy, retention, validation |
| [tradeoffs.md](tradeoffs.md) | Gains and limits |
| [upgrade-triggers.md](upgrade-triggers.md) | When to adopt Growth |

## Implementation

- [stackcraft-setups — Lean SaaS on DigitalOcean](../stackcraft-setups/recipes/lean-saas-on-digitalocean.md)
- [stackcraft-setups — Lean SaaS on AWS](../stackcraft-setups/recipes/lean-saas-on-aws.md)

## Related repositories

- [stackcraft-core](../stackcraft-core/) — tiers (Starter, Growth, Critical), frameworks, checklists
- [stackcraft-sectors](../stackcraft-sectors/) — industry-specific baselines
- [stackcraft-setups](../stackcraft-setups/) — tools and recipes

## Scope

Engineering guidance only. Not legal or compliance certification.

## Social draft

[drafts/linkedin-lean-production.md](drafts/linkedin-lean-production.md)
