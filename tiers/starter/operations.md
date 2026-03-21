# Starter — operations

## Deploy flow

1. Merge to main → CI tests.  
2. Build immutable artifact.  
3. Deploy via scripted SSH, API, or platform hook.  
4. Smoke test health + one critical read path.

## Change discipline

- Document exact deploy commands.  
- Keep **previous artifact** for instant rollback.

## Not required yet (but common next steps)

- Full staging environment → [Lean (module)](../../../stackcraft-lean-production/operations.md).  
- IaC for every resource → start with **network + DB + buckets**.
