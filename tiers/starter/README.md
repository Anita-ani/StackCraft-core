# Starter Production

**Budget:** $75–$300 (indicative; verify current pricing).

## Purpose

A **minimal** production system for early-stage products with **real users**: one primary environment, disciplined backups and deploys, and basic observability. Not highly available; acceptable when risk owners understand single-point-of-failure tradeoffs.

## Key characteristics

- Single compute node
- Limited redundancy
- Manual or scripted recovery procedures
- Basic observability (logs, uptime, host metrics)

## Sections

| Document | Description |
|----------|-------------|
| [architecture.md](architecture.md) | Component topology and data flow |
| [budget.md](budget.md) | Cost line items and assumptions |
| [team-fit.md](team-fit.md) | Operating model and headcount |
| [operations.md](operations.md) | Deploy and change workflow |
| [observability.md](observability.md) | Logs, metrics, alerts |
| [security.md](security.md) | Baseline access and hardening |
| [backups.md](backups.md) | Backup and restore expectations |
| [tradeoffs.md](tradeoffs.md) | Accepted limits and failure modes |
| [upgrade-triggers.md](upgrade-triggers.md) | When to adopt Lean tier |

## When to use

- MVP or early product with active users
- Solo or very small engineering teams
- Cost-constrained environments with **low to moderate** production risk index (PRI)

## When to move on

See [upgrade-triggers.md](upgrade-triggers.md).

## Industry context

High-risk sectors (e.g. regulated financial or health data) often require a **higher tier** regardless of budget. Cross-check [stackcraft-sectors](../../../stackcraft-sectors/).
