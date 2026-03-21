# StackCraft Core

Crafting production systems by budget, scale, and risk.

StackCraft Core is a cloud-neutral guide to designing and operating real production systems.

This repository defines expectations for systems that:

- remain available under load
- recover from failure
- provide visibility into system behavior
- enforce basic security practices
- evolve as usage and team size grow

---

## What this repository covers

- Production architecture by budget tiers
- Team-size-based system design
- Risk-based infrastructure decisions
- Production readiness checklists
- Observability, security, and recovery principles
- Upgrade paths between system maturity levels

---

## Production tiers

| Tier     | Budget    | Description              |
|----------|-----------|--------------------------|
| Starter  | $75–$300  | Bootstrap production     |
| Lean     | $400–$700 | Small team systems       |
| Growth   | $800+     | Scaling systems          |
| Critical | Variable  | High-reliability systems |

Paths:

- [tiers/starter/](tiers/starter/)
- **Lean** — standalone module: [stackcraft-lean-production](../stackcraft-lean-production/README.md) (entry stub: [tiers/lean/](tiers/lean/))
- [tiers/growth/](tiers/growth/)
- [tiers/critical/](tiers/critical/)

---

## Each stack defines

- Application runtime model
- Traffic routing and ingress
- Data storage and persistence
- Secret and configuration management
- Monitoring and alerting
- Backup and recovery strategy
- Failure handling and rollback approach

See [docs/05-production-readiness-checklist.md](docs/05-production-readiness-checklist.md).

---

## Repository structure

```text
stackcraft-core/
├── docs/
├── tiers/
├── blueprints/
├── frameworks/
├── checklists/
├── templates/
└── assets/
```

Directory definitions: [docs/09-repo-structure.md](docs/09-repo-structure.md).

---

## How to use this repository

1. Start with [docs/00-overview.md](docs/00-overview.md).
2. Understand production expectations: [docs/01-what-is-production.md](docs/01-what-is-production.md).
3. Select a budget tier: [docs/02-budget-tiers.md](docs/02-budget-tiers.md).
4. Apply decision frameworks: [frameworks/](frameworks/).
5. Use checklists before deployment: [checklists/](checklists/).

---

## Related repositories

- **stackcraft-lean-production** — Standalone Lean tier ($400–$700) module ([../stackcraft-lean-production/README.md](../stackcraft-lean-production/README.md)).
- **stackcraft-sectors** — Industry-specific production guidance (sibling repository).
- **stackcraft-setups** — Step-by-step implementation guides (sibling repository).

---

## Goal

Provide a structured approach to designing production systems that align with:

- budget constraints
- team capacity
- business risk
- operational maturity

---

## Scope

This repository documents **engineering practices** and architecture patterns.

It does **not** provide legal advice, regulatory interpretation, or compliance certification. Organizations in regulated industries must engage qualified counsel and auditors.

---

## Disclaimer

Educational technical content. See [CONTRIBUTING.md](CONTRIBUTING.md) for contribution expectations.
