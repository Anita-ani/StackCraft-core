# Growth Production Observability

## Requirements

- **Centralized logging** for application and platform (searchable, retained per policy).
- **Metrics** for infrastructure and application golden signals.
- **Alerting** on **actionable** thresholds — not noise.
- **Distributed tracing** (usually **sampled**) is optional but strongly valuable once you have multiple services or async paths.

## What to track

### Infrastructure

- CPU, memory, disk, network
- Instance count, autoscale events
- Load balancer health and target health

### Application

- Request rate, error rate, latency (by route or service where practical)
- Dependency health (DB, cache, queues, third parties)
- Background job success, duration, and backlog depth

### Database

- Connections, CPU, storage, replication lag (if replicas)
- Slow queries or lock contention (tooling varies by provider)

## Service clarity

- **Service scorecards** (or equivalent): owner, dependencies, SLO targets, on-call.
- **Business metrics** dashboards with **access control** when metrics are sensitive.

## Alerts (baseline examples)

Tune to your baselines; alert on **symptoms that need human action**:

- Service or region **unavailable** from the user’s perspective
- **Sustained high error rate** or **5xx** spike correlated with deploys
- **Latency** SLO burn or sudden regression
- **Resource exhaustion** (disk, memory, connection pools)
- **Database** failover, replication failure, or critical health signals
- **Queue** backlog growth beyond defined thresholds
- **Backup or replication job** failures

## Related

- [operations.md](operations.md)
- [security.md](security.md) (access to observability tooling)
