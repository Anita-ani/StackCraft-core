# Growth Production Team Fit

## Size and shape

- Typically **5 to 15 engineers**, or a smaller team carrying equivalent on-call and release load.
- **Service or domain owners** for major components (API, workers, data, edge).
- **Shared ownership** of production with emerging **platform** or **SRE** practices (may be part-time hats).

## How the team works

- **CI/CD** is the default path to production; exceptions are rare and documented.
- **Incident response** uses logs, metrics, and often traces; roles (incident lead, comms) are understood.
- **Load or launch testing** happens before major campaigns when risk warrants it.

## Operational expectations

- Alerts route to **people who can act**, not a generic list.
- **Runbooks** exist for top failure modes (deploy rollback, DB failover, traffic shed).
- **Scorecards** or dashboards tie services to owners, dependencies, and SLOs where used.

## Related

- [operations.md](operations.md)
- [observability.md](observability.md)
