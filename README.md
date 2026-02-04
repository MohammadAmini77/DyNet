# DyNet


# Dynamic Bandwidth Allocation in Collaborative Reinforcement Learning

This repository is based on my MSc thesis and its paper titled **“Dynamic Bandwidth Allocation in Collaborative Reinforcement Learning Under Total Bandwidth Constraints”**, completed as part of the Master of Science in Electrical Engineering in Iran University of Science and Technology.

## Abstract

Collaborative (cooperative) multi-agent reinforcement learning (MARL) enables multiple agents to coordinate and achieve shared goals. However, many existing MARL methods assume ideal or unlimited communication between agents, which is unrealistic in practical wireless systems where bandwidth is scarce.

This thesis proposes two novel communication-aware MARL algorithms, **DyNet 1** and **DyNet 2**, which dynamically allocate bandwidth among agents based on the importance of their observations. The goal is to improve coordination performance while minimizing unnecessary communication overhead under strict bandwidth constraints.

## Key Contributions

- Proposes **dynamic, learning-based bandwidth allocation** for collaborative reinforcement learning.
- Introduces two novel algorithms:
  - **DyNet 1**: Dynamic bandwidth allocation under a fixed total bandwidth constraint.
  - **DyNet 2**: Dynamic bandwidth usage with explicit penalization of communication cost.
- Employs a **centralized scheduler** that learns how to distribute bandwidth efficiently among agents.
- Encourages **sparse and efficient communication**, reducing wasted spectrum and power.
- Demonstrates effectiveness in bandwidth-constrained environments such as IoT and vehicular networks.

## Methodology

- Each agent uses a deep neural network to estimate the importance of its local observation.
- These importance values are sent to a learned **bandwidth allocator (scheduler)**.
- The scheduler dynamically assigns portions of the available bandwidth to different agents.
- DyNet 2 extends this framework by adding a communication penalty to the reward function, allowing agents to transmit messages only when the expected performance gain outweighs the communication cost.
- The learning framework is based on **actor–critic reinforcement learning** with centralized training and decentralized execution.

## Experimental Evaluation

The proposed methods are evaluated in two representative environments:

### Predator–Prey Game
- Tests cooperative behavior under strict bandwidth limitations.
- Demonstrates improved coordination and higher task success rates compared to baseline methods.

### Vehicular Ad-Hoc Networks (VANETs)
- Models spectrum sharing and communication among vehicles.
- Shows that DyNet algorithms achieve better performance with fewer transmitted messages.

## Results Summary

Simulation results show that both **DyNet 1** and **DyNet 2**:
- Achieve higher task performance under limited bandwidth
- Significantly reduce unnecessary communication
- Are suitable for real-world, bandwidth-constrained multi-agent systems


## Code Availability

The implementation used in this thesis is **not publicly available at the moment**.


## Thesis Information

- **Author:** Mohammad Amini  
- **Supervisor:** Dr. Shahrokh Farahmand  
- **Degree:** Master of Science in Electrical Engineering  
- **Institution:** Iran University of Science and Technology  

## Keywords

Collaborative Reinforcement Learning, Multi-Agent Reinforcement Learning, Communication Constraints, Dynamic Bandwidth Allocation, Actor-Critic, Vehicular Networks, IoT
