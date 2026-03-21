# Repository structure

This document defines the purpose of each top-level directory in StackCraft Core.

## docs/

Concepts, reading order, and cross-cutting explanations. Start at [00-overview.md](00-overview.md).

## tiers/

Production stack definitions by **budget and maturity tier**.

- **Starter**, **Growth**, and **Critical** live here as linked documents (architecture, operations, observability, and so on).
- **Lean** ($400–$700) is a **standalone sibling repository** [stackcraft-lean-production](../../stackcraft-lean-production/README.md). Only [tiers/lean/README.md](../tiers/lean/README.md) remains in Core as a pointer.

## blueprints/

Named **reference architecture patterns** (e.g. single-server production, managed-first). Blueprints illustrate how common constraints map to components; they are not vendor-specific runbooks.

## frameworks/

**Decision-making models** and evaluation tools: risk scoring (PRI), cost vs resilience, stack selection, RTO/RPO framing. See [../frameworks/README.md](../frameworks/README.md).

## checklists/

Operational readiness validation. Use before launch or after material changes.

## templates/

Reusable documentation and process templates (architecture one-pagers, budgets, runbooks, postmortems, scorecards).

## assets/

Supporting material for documentation:

- `diagrams/` — figures referenced from markdown (prefer Mermaid in-repo where possible).
- `references/` — static reference material that is not prose docs (e.g. exported diagrams, companion PDFs). Keep this directory small and intentional.
