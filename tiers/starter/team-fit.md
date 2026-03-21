# Starter — team fit

## Ideal

- **1 engineer** (founder or senior IC) who owns features **and** production.  
- Low to medium **PRI** ([../../frameworks/production-risk-index.md](../../frameworks/production-risk-index.md)).

## What one person can sustain

- One production environment + disciplined deploy + quarterly restore drill.  
- On-call = same human; keep alerts **sparse** and actionable.

## When Starter is the wrong tier for team size

- **2+ engineers** shipping frequently without staging → consider [Lean (module)](../../../stackcraft-lean-production/README.md).  
- **High PRI sector** (many FinTech/PHI cases) → sector doc may mandate Lean or Critical—see [stackcraft-sectors](../../../stackcraft-sectors/).
