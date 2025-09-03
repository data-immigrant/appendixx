# Appendix A – System Architecture & Scalability Rationale

## Overview
Our platform uses a **Client–Edge–On‑Chain–Off‑Chain** pattern to achieve global performance with low marginal cost.

**Client:** React‑Native mobile app & Next.js web.
**Edge:** Cloudflare Worker resolves label slugs, performs caching and API orchestration.
**On‑Chain:** zkEVM smart contracts (LabelResolver; ERC‑20 token & staking). Optional post‑quantum signature support.
**Off‑Chain:** IPFS for JSON‑LD dossiers & media; private ledger (Hyperledger Besu/Fabric) for high‑throughput event logs; nightly anchors to L2.

## Why this scales efficiently
- **Edge caching & serverless autoscale** → low latency for millions of users without managing servers.
- **zkEVM rollup economics** → batched transactions keep fees very low even at high TPS.
- **Hybrid storage (IPFS + hash on‑chain)** → sub‑linear cost growth as data volume increases.
- **Multi‑tenant, API‑first design** → a single deployment serves many orgs; partners integrate via REST/GraphQL.
- **Configurable crypto** → post‑quantum signatures are optional; do not burden end‑users or integrators.

## Data Flow (typical scan)
1) User scans a label → app calls Edge endpoint.  
2) Edge queries **LabelResolver** on zkEVM for IPFS CID → fetches dossier from IPFS (cached).  
3) App renders verified info + links; scan event logged on private ledger → nightly anchor hash to L2.

