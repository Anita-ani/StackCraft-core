# RTO / RPO guide

## Definitions

- **RPO (Recovery Point Objective)** — maximum acceptable **data loss** (time or transactions).  
- **RTO (Recovery Time Objective)** — maximum acceptable **outage** to restore service.

## How tiers often map (indicative)

| Tier | Typical RPO (if honest) | Typical RTO (if rehearsed) |
|------|-------------------------|---------------------------|
| Starter | Minutes–hours (snapshots + dumps) | Tens of minutes–hours |
| Lean | Minutes | Under an hour common |
| Growth | Sub-minute to minutes (with replication) | Minutes to low hours |
| Critical | Seconds–minutes (architecture-dependent) | Minutes with tested failover |

## Practice beats slides

If you have never **restored** to a clean environment, your RTO/RPO are unknown—assume worst case.

See [../checklists/backup-restore-checklist.md](../checklists/backup-restore-checklist.md).
