# Onboarding Agent – UX Redesign & Outcomes

## 1. Context
Early users were **dropping off after sign-up**:  
- “Connect database” lived deep in **Settings** → required prior knowledge and three clicks to get there  
- No progress feedback → users assumed the app was hung.  
- No “interrupt / back” option if the wrong tables were selected.  

## 2. Research inputs
| Source | Purpose |
|--------|---------|
| **User interview scripts** | 12 structured calls with senior / staff data engineers (Snowflake, Redshift, BigQuery) – captured workflow pain and heuristic shortcuts. |
| **User stories for testing** | Prioritised tasks around ERD generation, semantic-layer review, and fast POC cycles. |
| **UX reflections** | Post-mortem on first-run drop-offs; listed quick-win UI and functionality changes, e.g. return data profile already generated, download options, etc. |

## 3. Design decisions
| Pain point | Change shipped |
|------------|----------------|
| DB connect buried somewhere | **Middle panel (from three panels) “Onboarding agent”** guides user through connection + schema scan. |
| No progress feedback | Live status + step counter |
| No safe exit | “Stop → Restart” button at every step. |
| Intimidating review process | Three-panel layout: high-level feature list • chat-style agent • editable output. |

## 4. Metrics & results
| Metric (beta testers + 4 design partners) | Before | After |
|---------------------------------------------|--------|-------|
| Independent onboarding completion | ~0% (required 1-hr call) | **> 90 %** in early beta testing|
| Setup call time (founder/eng) | ~60 min | < 10 min |

**Reflection**: Most of the remaining friction emerged from connection problems, especially with BigQuery. Also, Snowflake cluster provisioning needed to be at least Small for workloads.

## 5. Lessons & next steps
- **Agent paradigm works if it is one of n options available** – conversational + inline actions (both autopilot + "take the wheel" option).  
- **Progress indicators** are non-negotiable for long-running tasks.  
- Next step: Develop guide for provisioning resouces (incl. Terraform, BigQuery docs, Snowflake connection strings) while ensuring cluster size is adequate for workload
