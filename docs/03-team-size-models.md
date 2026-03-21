# Team size models

Choose stacks that match **who can operate them** nights and weekends.

## Solo (1 engineer)

- Prefer **managed-first** data and deploy surfaces.  
- Automate deploy, backup, and restore documentation.  
- One on-call path (often you).

## Small team (2–5)

- **Staging** environment.  
- **IaC** for core resources; shared dashboards.  
- Secrets in a manager; no per-server mystery `.env`.

## Growth team (5–15)

- Clear **service ownership** and env separation.  
- Tracing and SLO-shaped thinking.  
- SSO for admin tools; least privilege.

## Larger / critical

- Platform/SRE function, error budgets, **DR drills**.  
- Access reviews and formal incident process.

## People trap

If only one person knows production and they leave, you have **operational debt**, not a cheap stack. Runbooks and checklists exist to reduce that risk—see [`../checklists/`](../checklists/).

## Next

[04-risk-based-thinking.md](04-risk-based-thinking.md)
