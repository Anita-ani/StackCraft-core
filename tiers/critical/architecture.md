# Critical — architecture

HA app and data paths, **tested** DR, strong edge and identity posture—exact topology is policy-driven.

```mermaid
flowchart LR
  users[Users] --> edge[CDN_WAF]
  edge --> lb[Multi_AZ_LB]
  lb --> app[App_HA]
  app --> db[(HA_DB)]
  db --> dr[DR_replica]
```

Multi-region only when **required**—it is expensive and complex.
