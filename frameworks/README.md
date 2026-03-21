# Frameworks

This directory contains **decision-making models** used to evaluate and compare production systems.

Use these frameworks to reason about:

- what level of infrastructure is appropriate for a workload
- how **risk** should influence architecture and operations
- how **cost** trades off against resilience and recovery time
- when to **upgrade** tier or split responsibilities across a larger team

## Start here

| Document | Use |
|----------|-----|
| [production-risk-index.md](production-risk-index.md) | Score data sensitivity, downtime impact, compliance exposure, and integrity risk (PRI). |
| [cost-vs-resilience.md](cost-vs-resilience.md) | Frame spend against failure modes and recovery expectations. |
| [stack-selection-matrix.md](stack-selection-matrix.md) | Map traffic, team, and data signals to a tier. |

## Supporting guides

| Document | Use |
|----------|-----|
| [rto-rpo-guide.md](rto-rpo-guide.md) | Define recovery point and recovery time objectives in operational terms. |

Frameworks are **cloud-neutral**. Industry-specific floors live in **stackcraft-sectors**. Implementation procedures live in **stackcraft-setups**.
