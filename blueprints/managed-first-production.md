# Blueprint: managed-first production

**Intent:** Push operational burden to vendors—managed DB, managed TLS, platform deploys where possible.

## When it fits

- Small team, moderate PRI, need speed.  
- You are not building a database company.

## Characteristics

- Strong defaults for patching and backups (still **verify**).  
- Less networking control; faster time to safe baseline.

## Watchouts

- Cost at scale; egress.  
- Still need **your** runbooks for app logic, migrations, and access.

**Tier:** often [Starter](../tiers/starter/) → [Lean](../../stackcraft-lean-production/README.md).
