# Lean Production Architecture

## Overview

A production setup for small teams that need safer deployments, clearer observability, and better separation of concerns.

## Architecture

```text
User → DNS/CDN → Reverse proxy / load balancer → Application service
                                              ↓
                                        Managed database
                                              ↓
                                         Backup storage

CI/CD → Staging → Production

Monitoring / logging → Metrics, logs, alerts
```

## Components

### Application layer

App service running on a VM, app platform, or container host.

### Database layer

Managed PostgreSQL or MySQL preferred.

### Reverse proxy / ingress

Nginx, cloud load balancer, or managed ingress.

### Staging

Separate environment for validation before production release.

### Observability

- Logs
- Metrics
- Uptime checks
- Alerts

### Backups

- Scheduled backups
- Retention policy
- Restore validation

## Module index

[README.md](README.md)
