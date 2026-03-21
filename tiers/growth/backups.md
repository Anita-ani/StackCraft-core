# Growth Production Backups

## Requirements

- **Automated backups** for databases and other durable state (object stores, configuration where applicable).
- **Defined retention** aligned to **RPO** and compliance needs.
- **Restore testing** on a schedule — at least **monthly** for top-tier datasets into a non-production environment.

## Strategy

- **Managed database**: PITR or frequent snapshots per provider capabilities.
- **Immutable or cross-region copies** for datasets where a single-region loss is unacceptable (cost tradeoff).
- **Application assets** and **artifacts** (build outputs, infra state) backed up or reproducible from source control.
- **Configuration** (IaC, env definitions) versioned and recoverable.

## Async and queues

Backups **do not** restore **in-flight queue messages** by default. Document **replay**, **idempotency**, or **dead-letter** handling so recovery drills match reality.

## Goal

**Minimal data loss** and **predictable recovery time** under documented scenarios — not “we have snapshots somewhere.”

## Related

- [architecture.md](architecture.md)
- [tradeoffs.md](tradeoffs.md)
