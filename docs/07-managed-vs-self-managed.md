# Managed vs self-managed

StackCraft is neutral: both models are valid. Choose based on **team bandwidth**, **PRI**, and **blast radius**.

## Managed-first (default for small teams)

**Pros:** less misconfiguration surface, faster path to backups and patching, clearer SLAs from vendors.  
**Cons:** higher $ at scale; less control over internals; vendor lock-in tradeoffs.

**Good when:** few ops people, high PRI data, or you must ship product—not build a database company.

## Self-managed (control-first)

**Pros:** cost control at scale, deep tuning, exotic requirements.  
**Cons:** you own patching, backups, failover drills, and on-call depth.

**Good when:** strong platform team, cost at volume, or regulatory/architectural needs vendors cannot meet.

## Hybrid

Very common: **managed database** + **self-managed** app on VMs or Kubernetes.

## Decision prompts

- Can you **restore** in under your RTO without heroics?  
- Who is **paged** when the data layer misbehaves?  
- Have you **tested** failover this quarter?

## Next

[08-sector-decision-framework.md](08-sector-decision-framework.md)
