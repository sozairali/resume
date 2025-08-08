# Robotics Data Infrastructure Exploration

**Objective:** Investigate opportunities to build a scalable “RoboLake” platform for robotics companies, addressing pain points in storing, retrieving, and processing large-scale ROS bag data.

**Method:** Structured interviews with 11 senior robotics engineers, including at Amazon Robotics, Pickle Robot, Six River, and others.

---

## Key Findings
1. **Open Source Dominance**  
   - Most robotics data engineering pipelines are built with open source tools. 
   
2. **ROSbag as Industry Standard**  
   - ROS1 dominates older setups; ROS2 is emerging in newer companies.
   - Transition between ROS1 and ROS2 is non-trivial.
   - ROSbag is a communication protocol (pub-sub model), not a queryable data format.
   - **MCAP** is a newer, queryable format associated with ROS2 gaining adoption.

3. **Engineering Resource Constraints**  
   - Roboticists frequently write custom tooling themselves.
   - Startups rarely have budget for dedicated DEs or tooling.
   - Priority is to “make the robot work” before investing in data infra.
   - Processing and querying data takes very long due to the size of data involved

4. **Long Development Cycles**  
   - Prototyping and testing require field experiments, slowing iteration.

5. **Existing Tooling Gaps**  
   - **Foxglove** is gaining traction for real-time visualization. It has the potential to expand into a full data engineering platform, but it will have to reveal its "guts" in order to do so. Users love the visualization capabilities it provides. 
   
---

## Central Thesis
- Data engineering is **not** core to robotics companies, yet every robotics company will need:
  1. **Data versioning** for algorithm tracking and security.
  2. **Quick querying** -- maybe even in natural language or a declarative format -- to diagnose failures.
  3. **Anomaly detection** in operational data.
  4. Cost-efficient infrastructure.
  
- Currently, Foxglove is the only well-known tool in the space — focused on visualization, not full-stack data pipelines.
- Another tool called ARES is making its way too

---

## Opportunity
A “Robo Lake” could:
- Enable **natural-language-to-query** workflows.
- Pull only the required bytes from cloud storage (e.g., S3, GCS).
- Integrate version control and cost-efficient retrieval.
