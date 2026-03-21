# Backup & restore checklist

- [ ] Automated DB backups (PITR or snapshots)  
- [ ] Logical dumps to object storage where policy requires  
- [ ] Immutable or access-controlled backup storage  
- [ ] Restore drill **quarterly** minimum; record RTO  
- [ ] Secrets to access backups are not the same as app-only creds  
- [ ] DR region/copy documented if required  

See [../frameworks/rto-rpo-guide.md](../frameworks/rto-rpo-guide.md).
