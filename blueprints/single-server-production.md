# Blueprint: single-server production

**Intent:** One primary compute node (VM or equivalent) running app + **externally** managed DB preferred.

## When it fits

- Low PRI, small traffic, 1–2 engineers.  
- Strong backups and deploy discipline.

## Must not skip

- Managed database **or** rigorously operated DB with tested restore  
- TLS, firewall, automated backups to object storage  
- Monitoring and on-call path (even if informal)

## Weaknesses

Single AZ/server failure domain; limited horizontal scale without redesign.

**Tier:** aligns with [../tiers/starter/README.md](../tiers/starter/README.md).
