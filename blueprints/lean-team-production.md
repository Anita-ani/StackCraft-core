# Blueprint: lean-team production

**Intent:** Move from **survival** (Starter) to **control**—collaborative, operationally intentional production: **staging**, managed data plane, centralized visibility, deployments that can be **rolled back**, and runbooks the team shares.

## When it fits

- Two to five engineers shipping multiple times per week
- Downtime or bad deploys have measurable cost
- Team must stop validating changes only in production

## Characteristics

- Separate **staging** and **production** environments
- **Secrets manager** (or equivalent) and least-privilege access
- **IaC** with remote state for core infrastructure
- **Alert routing** with named ownership
- **Runbooks** for rollback and restore

**Tier:** [Lean](../../stackcraft-lean-production/README.md) (standalone module).

**Setups:** [DigitalOcean recipe](../../stackcraft-setups/recipes/lean-saas-on-digitalocean.md) and [AWS recipe](../../stackcraft-setups/recipes/lean-saas-on-aws.md) in stackcraft-setups.
