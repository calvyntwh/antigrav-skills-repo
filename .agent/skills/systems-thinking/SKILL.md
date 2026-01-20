---
name: systems-thinking
description: Architectural analysis using Feedback Loops and System Dynamics.
license: MIT
---

# Systems Thinking (The Loop Protocol)

> "You cannot just change one thing." - Garrett Hardin

## When to Use
*   **Architecture Changes:** Migrating DBs, splitting microservices, changing cache strategies.
*   **Scaling:** "We need to handle 10x traffic."
*   **Performance Tuning:** "The system is slow, let's add threads."
*   **Post-Mortems:** "Why did fixing X break Y?"

## The Protocol: The Loop Protocol
Stop thinking in Lines (Problem -> Solution).
Start thinking in Loops (Action -> Result -> Feedback -> Action).

### 1. Identify the Node
What variable are you changing?
*   *Example:* "I am increasing the Thread Pool size."

### 2. Trace the Edges
What is connected to this node?
*   *Downstream:* Threads consume -> DB Connections.
*   *Upstream:* Threads process -> Incoming Requests.

### 3. Find the Loops
*   **Reinforcing Loop (R):** Does A produce more B, which produces more A? (Explosion).
    *   *Example:* Retry Logic. Fails -> Retry -> More Load -> Fails.
*   **Balancing Loop (B):** Does A produce B, which reduces A? (Stability/Resistance).
    *   *Example:* Auto-scaling. Load High -> Add Servers -> Load per Server Low -> Remove Servers.

### 4. Simulation (The Delay)
What happens *later*?
*   "If I add cache, it works now. But in 5 minutes, data is stale. Do we have invalidation?"
