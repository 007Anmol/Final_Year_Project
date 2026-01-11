# 🚚 Multi-Objective Route Optimization using Multiparametric Graph Attention Networks (MP-GAT)

## 📌 Overview

This project implements a **learning-based framework for multi-objective logistics route optimization** using a **Multiparametric Graph Attention Network (MP-GAT)**.  
The system models a realistic **multi-modal transportation network** and learns to balance **cost, delivery time, and reliability** simultaneously—overcoming the limitations of classical routing algorithms such as Dijkstra, which optimize only a single objective at a time.

The framework combines:
- Multi-modal transport network modeling (road, rail, air, sea)
- Shipment-specific constraints (urgency, budget, weight)
- Graph Attention Networks (GATs) for adaptive routing intelligence
- Classical Dijkstra baselines for supervision and benchmarking

---

## 🎯 Problem Statement

Real-world logistics routing is inherently **multi-objective**, requiring trade-offs between:

- Transportation cost
- Delivery time
- Reliability / on-time performance
- (Optional) Carbon footprint

Classical routing algorithms (e.g., Dijkstra, A*) require **fixed edge weights** and can only optimize a **single objective at a time**. They are unable to adapt dynamically to shipment-specific constraints such as urgency or budget.

### Key Question
> How can we learn **adaptive routing strategies** that balance multiple objectives while accounting for shipment context and network structure?

---

## 💡 Proposed Solution: MP-GAT

We propose a **Multiparametric Graph Attention Network (MP-GAT)** that learns routing behavior directly from data.

### Key ideas:
- Represent the logistics network as a **multi-modal multigraph**
- Encode **edge parameters** (cost, time, reliability) into node representations
- Condition predictions on **shipment context**
- Learn **multi-objective trade-offs** using multi-task learning
- Supervise training using **exact Dijkstra solutions**

Instead of predicting explicit paths, MP-GAT predicts **route-level performance metrics**, enabling fast inference and flexible integration with classical solvers.

---

## 🧱 System Architecture

