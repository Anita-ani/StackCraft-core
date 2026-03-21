# Blueprint: growth production

**Intent:** Horizontal or autoscale app tier, **queues** for async, tracing, stronger isolation.

## When it fits

- Traffic spikes, multiple services, or noisy multi-tenant SaaS.  
- Debugging requires more than logs on one box.

## Characteristics

- Load balancers, worker tiers, cache discipline.  
- WAF-class thinking at the edge.

**Tier:** [Growth](../tiers/growth/README.md).
