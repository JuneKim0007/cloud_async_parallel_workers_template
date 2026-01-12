# Cloud-Naive, Async, Parallel Workers Template
This project uses **FastAPI** in **Python** to provide a simple, cloud-native backend for async and parallel workers—designed especially for those who can’t afford dedicated machines running 24/7.
Cloud-native backend worker template supporting async I/O and parallel (core pinned) computation.

This project provides a **cloud-naive execution model** such that:
- **Async I/O** for network-bound and orchestration tasks.  
- **Parallel worker pools** for CPU-intensive computation. 

The system is designed to run **entirely in the cloud** to avoid needing a machine being on 24/7.

While I am aware that combining a lightweight, dedicated local machine with cloud resources responsible for certain management aspects--such as orchestrating tasks-- can improve cost efficiency, the main goal of this project is to provide a basic async and parallel runtime in Python with FastAPI for those (sadly like me) who cannot afford such machines running 24/7. However, I also am considering to develop optional code snipchets in the future that enable such orchestration tasks.

The main design goals stem from my personal need to create a game backend server template while generalizing the code to be applicable in other areas.
  
**The design rationale mainly focuses on:**

- Maintaining low latency
- Reducing operational costs

---

## Design Sketches and Limits

This project assumes that **all components run in cloud environments**.

In real-world deployments, it is often more cost-efficient to introduce a **lightweight, always-on orchestrator** (local, edge, or minimal cloud instance) to aggregate results and coordinate large workloads.  
However, many developers and small teams cannot afford or manage such infrastructure.

**The primary goal of this template is to:**  
- Enable fully cloud-native execution  
- Attempt to balance cost and latency without requiring dedicated orchestration hardware  
- Serve as a practical reference for async + parallel backend worker systems

Optional optimizations (such as external orchestration or edge aggregation) are documented but **not required**.

---

## Architecture Overview

At a high level, the system separates execution responsibilities:

- **Async I/O Workers**  
  Handle frequent, light workloads
  Designed for high concurrency and low latency  

- **Parallel Compute Workers**  
  Handle heavy-computation workloads  
  Executed in worker pools suitable for cloud-based parallelism  

---

## Designing Sketches

### Basic Workflow

---

### Worker Models


---

### Queue Models


---

## Notes
---
