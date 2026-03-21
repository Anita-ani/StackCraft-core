# Security checklist

- [ ] TLS for user-facing traffic  
- [ ] Firewall / security groups: least open ports  
- [ ] No password SSH; keys or SSM-style access  
- [ ] IAM least privilege for deploy and runtime  
- [ ] Dependency scanning in CI (policy for critical CVEs)  
- [ ] Admin actions auditable where sensitive  
- [ ] Break-glass access documented (rare, logged)  
- [ ] Third-party keys rotated on schedule  

High PRI: pair with sector baselines in [stackcraft-sectors](../../stackcraft-sectors/).
