# Cost vs resilience

## The curve

- **Low cost** usually means fewer redundancy layers and more manual procedures.  
- **High resilience** means replication, DR, observability depth, and people time.

## Where teams overspend

- Multi-AZ everything before product–market fit.  
- Heavy Kubernetes for a single small service.  
- Long log retention without a retention policy tied to risk.

## Where teams underspend

- Backups without **tested** restore.  
- No staging.  
- No budget alerts—then surprise egress bills.

## Sweet spot

Match **PRI** and **revenue at risk** to tier; use [../docs/02-budget-tiers.md](../docs/02-budget-tiers.md) line items so finance can reason about tradeoffs.
