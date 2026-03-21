# Sector decision framework

StackCraft Core defines **cloud-neutral** tiers and checklists. **stackcraft-sectors** applies sector-specific minimum baselines; **stackcraft-setups** holds implementation procedures.

## When to use other repositories

| Repository | Use when |
|------------|----------|
| [stackcraft-sectors](../../stackcraft-sectors/) | Money movement, health or other sensitive personal data, regulated flows, or high external trust requirements |
| [stackcraft-setups](../../stackcraft-setups/) | You are selecting concrete tools (containers, reverse proxies, cloud accounts) and need step-by-step setup |

## Recommended flow

1. Select a **tier** under `tiers/`.
2. Score **PRI** using [frameworks/production-risk-index.md](../frameworks/production-risk-index.md).
3. Compare against **stackcraft-sectors**; if the sector baseline exceeds the tier, **raise the tier** or reduce scope (data collected, geographies, etc.).
4. Implement using **stackcraft-setups** once tools and environments are chosen.

## Scope

Sector content in **stackcraft-sectors** is still **engineering guidance**, not legal or compliance certification. Regulated workloads require organizational process and professional review.
