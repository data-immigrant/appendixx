# Appendix B – Roadmap & User Stories (Replicability)

**Phase 1 (0–6 mo):** Consumer MVP – scan & decode labels; micro‑courses; pilot users.  
**Phase 2 (6–18 mo):** Community reporting; token incentives; moderation council.  
**Phase 3 (18–36 mo):** Compliance‑as‑a‑Service; regulator & financier dashboards; APIs; quantum upgrade.

## Representative user stories (Epic 1 – Consumer)
- **US1.1 Scan a label:** camera recognizes EU logos; fallback manual search; P95 latency < 5s.  
- **US1.2 Resolve logo → data:** LabelResolver + IPFS via Cloudflare Worker; offline cache.  
- **US1.3 View dossier:** render name, definition, rules; CTA to learning.  
- **US1.4 Take micro‑course:** pay (Stripe/crypto); watch; receive completion badge.  
- **US1.5 Telemetry & anchoring:** anonymised scan events → Besu; nightly anchor to L2.

## Representative user stories (Epic 3 – Community)
- **US2.1 Submit report:** geo‑tagged report; optional photos; stored on IPFS; on‑chain reference; requires staked rep.  
- **US2.2 Vote on claims:** stake to up/down‑vote; on‑chain vote record; abuse detection.  
- **US2.3 Earn rewards:** verified reports → token reward + discount code.  
- **US2.4 Review reports:** moderation dashboard; approve/reject; decisions logged & anchored.

## Representative user stories (Epic 5 – Compliance)
- **US3.1 Regulator login:** SSO with MFA; RBAC; GDPR‑compliant logging.  
- **US3.2 Company dashboard:** view claims, sources, verification status; filter/export.  
- **US3.3 Generate reports:** compile audit logs + cryptographic proofs; digitally sign (PQ key).  
- **US3.4 API for financiers:** REST/GraphQL with rate‑limits and analytics.

**Replicability:** features are modular, templated and deployable to new sectors/regions with configuration (schemas, label libraries), not code rewrites.
