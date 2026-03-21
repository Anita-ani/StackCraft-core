# Production readiness checklist

Use for **self-audits** and **scorecards**. Every tier in [`../tiers/`](../tiers/) should map back to these questions.

## Twelve canonical questions

1. **Where is it hosted?** Regions, accounts, environment separation.  
2. **How is it deployed?** Pipeline, approvals, immutable artifacts.  
3. **How is traffic routed?** DNS, TLS, load balancing, edge/WAF conceptually.  
4. **Where is the database?** Managed vs self-managed; failover story.  
5. **Where are secrets stored?** Rotation, access, audit.  
6. **How is health monitored?** Synthetics, metrics, logs, traces as needed.  
7. **How are alerts routed?** Severity, ownership, paging.  
8. **How are backups taken and tested?** RPO/RTO; restore drills.  
9. **How is access controlled?** IAM, SSO, break-glass, admin audit.  
10. **How is rollback done?** Deploy revert, migrations, feature flags.  
11. **How is DR exercised?** Game days, documented failover.  
12. **How are costs bounded?** Budget alerts, tags, teardown discipline.

## Scorecard

Rate **1–5** per question for your org. Compare to your **PRI** ([frameworks/production-risk-index.md](../frameworks/production-risk-index.md)):

- Low score + **high PRI** → underbuilt.  
- High score + low traffic → acceptable if cost is intentional.

## Checklist pack

Deep dives: [`../checklists/`](../checklists/).

## Next

[06-upgrade-paths.md](06-upgrade-paths.md)
