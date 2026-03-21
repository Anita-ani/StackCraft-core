# Growth Production Operations

## Deployment practices

- **CI/CD pipeline** is required for production changes; direct manual deploys are the exception, not the norm.
- Prefer **zero- or near-zero-downtime** strategies: **rolling**, **blue/green**, or **canary** with health checks.
- **Rollback** must be **tested and documented** (previous image, release, or task definition; feature-flag off).
- **Database migrations**: prefer strategies that **decouple** risky schema changes from single-step app deploys (expand/contract, backward-compatible phases) when the data model is large or hot.

## Release and capacity

- **Feature flags** for high-risk user paths.
- **Load tests** before major marketing or partner events when traffic shape is uncertain.
- **Capacity reviews** when autoscale policies, queue depth, or DB connection pools trend upward.

## Incident handling

- Alerts reach **on-call or owning engineers** with clear escalation.
- **Incident process** is lightweight but real: roles, communication channel, post-incident review for material events.
- **Logs and metrics** (and **traces** where enabled) are the default debugging path.

## Reliability practices

- **Redundancy** for critical components (multiple app instances; managed DB resilience options where affordable).
- **Automated restart** and **replacement** of unhealthy instances via orchestrator or autoscaler.
- **Staging** (and pre-prod if used) should reflect production **topology**, not only a single tiny box.

## Related

- [architecture.md](architecture.md)
- [upgrade-triggers.md](upgrade-triggers.md)
