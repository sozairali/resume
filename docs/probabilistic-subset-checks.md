# Probabilistic Subset Checks for FK→PK

**Goal.** Fast, scalable way to check if set **A** is (probably) a subset of **B** in a PK–FK context (i.e., every FK appears in PK).

## Requirements
- Optimize for **time** and scale at least quasi-linearly in time/space  
- Allow sending a **Bloom “signature”** to the server while keeping raw data with the customer 

## What I built (Bloom baseline)
- Implemented a **Bloom filter** with target **1% FPR**  
- Tuned `k` (hashes) and `m` (bits) and estimated storage costs on AWS  
- Repo: https://github.com/sozairali/bloom-filter
  
## Why we chose HLL for this use-case
- Team adopted an **HLL representation** because it needs **fewer hashes** and **smaller memory** per sketch 
- The HLL “signature” was **good enough to flag likely subsets** (fast negative/positive filter); false positives were most common when IDs were **ordinal** (ordered) values—an area where Bloom also struggles for this task 
- We paired sketches with an **LLM + metadata** to power **FK–PK recommendations** end-to-end

## Takeaways
- Bloom provided a clear **baseline** (tunable FPR; compact).  
- For our constraints, **HLL-style signatures** offered a **faster/lighter** way to screen for probable subset relations and integrate with downstream recommendation logic. 
