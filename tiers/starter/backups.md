# Starter — backups

## Minimum requirement

Backups must **exist** and be **restorable**.

If you cannot restore, you do not have backups.

## Strategy

- **Daily** (or more frequent) logical database dump for PostgreSQL.  
- Store dumps in **object storage** with lifecycle rules (retention you can afford).  
- If you use a **managed database**, enable vendor automated backups **and** keep logical dumps for portability.

## Example

```bash
# Illustrative — set DATABASE_URL from your secret manager in real use
pg_dump "$DATABASE_URL" | gzip > "pgdump-$(date -u +%Y%m%d).sql.gz"
# Upload pgdump-*.sql.gz to object storage (aws s3 cp, s3cmd, doctl spaces, etc.)
```

## Critical rule

Schedule a **restore drill** (quarterly minimum) to a throwaway instance or empty database — measure time to a healthy app.

See [../../checklists/backup-restore-checklist.md](../../checklists/backup-restore-checklist.md).
