# Growth Production Security

## Baseline

- **Least-privilege** access for humans and automation (IAM, RBAC, scoped API keys).
- **Secrets management** — no long-lived secrets in repo; rotation where feasible.
- **Network posture** — private subnets for data tier where supported; security groups or firewalls **deny by default**.
- **TLS everywhere** for user-facing and internal control-plane traffic as appropriate.
- **Patching** cadence for OS, images, and dependencies (team-defined SLA).

## Recommended

- **WAF** with managed rule sets plus **custom rules** for abuse patterns.
- **Private connectivity** to data stores (VPC endpoints, private link, or equivalent).
- **SSO** and **RBAC** for cloud and observability consoles.
- **Short-lived credentials** for CI/CD (e.g. OIDC to cloud), not static keys where avoidable.
- **Audit logs** for sensitive access and production changes.
- **Block or gate deploy** on **critical CVE** policy (define what “critical” means for your org).

High **production risk index (PRI)** or regulated sectors may still require **Critical** tier controls. Cross-check [stackcraft-sectors](../../../stackcraft-sectors/).

## Related

- [architecture.md](architecture.md)
- [operations.md](operations.md)
