# Appendix H – Deployment & Ops SOP (Replicable)

**New org onboarding (standard, 1–2 hours):**
1) Create org in admin; assign plan.  
2) Upload label templates & dossiers (CSV/JSON or portal forms).  
3) Auto‑pin to IPFS; update LabelResolver mapping via admin TX.  
4) QA checklist; go‑live toggle.

**Monitoring & SRE:**
- Datadog dashboards: latency, error rate, L2 gas, IPFS pinning, queue depth.  
- Autoscaling via Cloudflare; alarms route to on‑call.  
- Backups: IPFS pinning redundancy; DB snapshots; key rotation policy.

**Change management:**
- Feature flags; staged rollouts; blue‑green deploys.
