# Upgrade paths

Tiers are **not isolated**. Migrate in **order**; the first things to break are usually people and change velocity, not CPU.

## Starter → Lean

Lean tier documentation lives in the standalone **[stackcraft-lean-production](../../stackcraft-lean-production/README.md)** module (not under `tiers/lean/` beyond a stub).

**Do first:** staging; secrets manager; IaC baseline; alert routing with owners; rollback + backup runbooks (see checklists).

**Often stays:** same provider/region; same CI vendor.

**Breaks first:** one server / one env for a growing team; untracked manual changes.

## Lean → Growth

**Tier reference:** [Growth](../tiers/growth/README.md).

**Do first:** horizontal or autoscale app tier; load balancing; queues for async; stronger isolation (data + network); structured observability and (optional) tracing; zero- or near-zero-downtime deploy patterns; safer DB migrations (expand/contract).

**Breaks first:** shared DB contention; multi-tenant noise without isolation strategy; single-instance app under real traffic.

**Implementation sketches:** [Growth SaaS on AWS](../../stackcraft-setups/recipes/growth-saas-on-aws.md) · [Growth SaaS on DigitalOcean](../../stackcraft-setups/recipes/growth-saas-on-digitalocean.md).

## Growth → Critical

**Do first:** HA/DR with defined RTO/RPO; formal access lifecycle; edge security posture; incident program; automated restore tests where possible.

**Breaks first:** informal on-call at scale; single-region assumptions vs contract/regulator demands.

## Changing provider or hosting model

Conceptual difficulty:

| Move | Pain |
|------|------|
| PaaS → IaaS | Stateful data, networking, TLS |
| Single VPS → managed platform | DNS cutover, migration window |
| Cloud A → Cloud B | IAM rewrite, egress, state |

Always plan **DNS**, **data migration**, **rollback** (keep old stack read-only until stable).

Provider-specific playbooks belong in future **`stackcraft-<provider>`** repos—not Core.

## Tier docs

- Starter, Growth, Critical: `upgrade-triggers.md` under each [tier folder](../tiers/).
- **Lean:** [upgrade-triggers.md](../../stackcraft-lean-production/upgrade-triggers.md) in **stackcraft-lean-production**.

## Next

[07-managed-vs-self-managed.md](07-managed-vs-self-managed.md)
