# GTM Experimentation & Funnel Tracking (Early PMF)

**ICP:** Heads of Data Engineering, Principal Data Engineers, Data Architects, Heads of Data  
**Problem we address:** “Simple”  or "quick and dirty" dashboards/analytics/data prototypes that are anything but, due to incomplete data models, stale docs, and costly requirements gathering.

## Channels Tested (small-N, sprint style)
- **Personal network** — strongest signal; yielded user interviews and design partners; not scalable.
- **LinkedIn outbound using agentic tool** — very limited traction; **<1%** reply; ICP not actively sourcing there.
- **Hosting in-person events (data-engineer community)** — good traction; largest event **~50** attendees → **~10** demos; not all attendees were ICP.
- **System integrators / channel partners** — genuine interest; **2** design partners; blocked by **client data-privacy** constraints.

## Channels Deferred (why)
- **Reddit / other social** — no “power user” on team; no open-source asset to anchor content.
- **Content creation** — bandwidth constraints; CEO did not have technical background to ship credible content fast.

## Funnel Snapshot (what the numbers said)
- Strong **demo → POC** conversion: **>90%**
- Upper-funnel weak: cold reply/meeting rates low; **pain was “important but not urgent.”**
- ICP often lacked immediate budget / clear justification path.

## Metrics Tracked (lightweight)
- **Reply rate** (emails/DMs)  
- **Meeting booked %** and **time-to-first-reply**  
- **Demo → POC %**  
- **CAC proxy** = (hours × blended rate + spend) / meetings  
- Notes from calls (the “why” behind each outcome)

## Recommended Decisions (Kill / Keep / Iterate)
- **Kill:** generic LinkedIn outbound after three monthly sprints below reply-rate bar.  
- **Keep:** in-person events + partner conversations (highest intent + warm intros).  
- **Iterate:** message toward *“reduce requirements-gathering pain & compliance risk”*; lower-friction CTAs (15-min technical check), tighten ICP list.

## Strategic Decision: Distribution (OSS vs. Multi-tenant SaaS)

**Proposal (mine):** Open-source the core (permissive license) and offer a managed service; use OSS to accelerate adoption within our ICP (Heads of Data Eng / Data Platform), reduce procurement friction, and drive bottom-up distribution.

**Decision:** Team disagreed with OSS on IP grounds. We proceeded with a **closed, multi-tenant web app**.

**Impact:** Building the multi-tenant app consumed **material time and engineering bandwidth**.

**Rationale for OSS:**
- Infra-buyer ICP prefers **source-visible** tools for evaluation and PoCs.
- Creates opportunity to get into Reddit/Discord channels to get product/tech feedback.
- OSS lowers **trust and integration barriers**; enables **community validation** and contributions.
- Improves **top-of-funnel** (stars, issues, examples) and shortens **time-to-first-value**.

**Counterfactual playbook (what I’d do next time):**
- **OSS core + managed cloud** (guard rails, hosted connectors, auth).
- **Fast PoC path:** docker compose + example datasets and notebooks.
- **Governance:** clear contribution guide and roadmap; commercial features in the hosted tier.

## What I Did (condensed)
- Designed small-N experiments per channel with clear **success bars** and **stopping rules**.  
- Built a **funnel tracker** (reply → meeting → demo → POC) with a **CAC proxy** and call-note fields.  
- Ran founder-led events to generate **warm demos**; captured objections (budget, urgency, data privacy).  
- Converted learning into a **prioritized GTM plan** and **message/ICP refinement**.

## Takeaways
- Events + partner routes produced the **warmest** conversations; LinkedIn cold outreach underperformed.  
- Message clarity and **proof assets** (demo + client-hosted PoCs) mattered more than channel volume.  
