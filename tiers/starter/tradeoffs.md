# Starter — tradeoffs

## What you gain

- **Low cost**  
- **Simplicity** — one place to look, one deploy path to learn  
- **Fast setup** — days, not months, when you stay disciplined  

## What you lose

- **High availability** — no automatic failover across zones  
- **Redundancy** — single failure domain for compute  
- **Automatic failover** — recovery is **procedural** (restore, redeploy)  
- **Elastic scale** — vertical scale or manual second node later  

## Risk

**Single point of failure:** if the server dies → **downtime** until you recover on a new machine or snapshot.

That can be an **acceptable** business decision at this tier **if**:

- backups are real and **tested**  
- you can redeploy the app from CI in a known time  
- stakeholders understand RTO/RPO  

## What makes this “production” anyway

Even at **~$150/mo**, you still need:

- backups + tested restore  
- logs you can debug  
- monitoring + alerts  
- SSL  
- basic access control  

## Industry

This stack can safely run many **SaaS MVPs**, **internal tools**, and **early products**.

It is often **wrong** for:

- **FinTech** without audit-grade logging and controls → see [stackcraft-sectors — FinTech](../../../stackcraft-sectors/sectors/fintech/README.md)  
- **Healthcare** without access control and vendor/legal alignment → see [stackcraft-sectors](../../../stackcraft-sectors/README.md) (add `sectors/healthcare/` when you publish it)  

## Next tier

When staging, team size, or PRI forces it → [stackcraft-lean-production](../../../stackcraft-lean-production/README.md).
