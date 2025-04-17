# Evolutionary Adaptation in Seahorses and Pipefishes  
**A Dual Approach Using Genetic Algorithms and Reinforcement Learning**

## 📘 Overview

This project investigates how seahorses and pipefishes evolve or can be analyzed using intelligent computational methods. It consists of two distinct approaches:

- **Genetic Algorithms (GA)**: Simulates evolutionary exploration across 10 generations to analyze how traits like brain weight and body length evolve.
- **Reinforcement Learning (RL)**: Predicts key biological attributes (**Sex**, **Preservation**, and **Location**) based on observed traits (**Brain Weight** and **Body Length**).

---

## 🔍 Problem Statement

Understanding evolutionary traits and how they define species survival or classification is a central theme in biology. This project combines evolutionary computing and learning-based prediction to:

- Explore the impact of traits across generations.
- Predict categorical biological attributes from numerical traits.
- Compare generative vs. predictive modeling in biological contexts.

---

## 🎯 Objectives

- Use **Genetic Algorithms** to simulate the evolution of traits across generations.
- Use **Reinforcement Learning (Q-Learning)** to build a trait-based classifier.
- Visualize and compare both approaches from a performance and biological relevance standpoint.

---

## 📂 Project Structure

```
evolutionary-adaptation/
│
├── EC_Project.ipynb           # GA: Evolution over 10 generations
├── RL_Project.ipynb           # RL: Trait-based prediction using Q-Learning
├── data/                      # Dataset
└── README.md                  # This file
```

---

## ⚙️ Methodology

### 🧬 Genetic Algorithm (GA)

- **Goal**: Explore trait evolution (Brain Weight, Body Length) across 10 generations.
- **Key Components**:
  - *Selection*: Roulette Wheel, Tournament
  - *Crossover*: Arithmetic / SBX
  - *Mutation*: Gaussian / Non-Uniform
  - *Fitness Function*: Survival likelihood based on target trait bounds
  - *Diversity Maintenance*: Elitism + random injects

- **Outcome**: Visual trends showing how traits evolve in the population over time.

---

### 🤖 Reinforcement Learning (RL)

- **Goal**: Predict **Sex**, **Preservation**, and **Location** from **Brain Weight** and **Body Length**.
- **Environment**: `EvolutionEnv` with encoded states and actions
- **Q-Learning Setup**:
  - States: Binned or normalized combinations of input traits
  - Actions: Predicted classes for each attribute
  - Rewards: +1 for correct prediction, 0 otherwise
  - Policy: ε-greedy with decay
  - Output: Separate Q-Tables or a multi-task Q-Learning framework

- **Outcome**: Trained agent that can infer the biological classification based on physical measurements.

---

## 📊 Results

| Feature                     | Genetic Algorithm                 | Reinforcement Learning             |
|----------------------------|-----------------------------------|------------------------------------|
| Objective                  | Evolution simulation              | Attribute prediction               |
| Input Traits               | Brain Weight, Body Length         | Brain Weight, Body Length          |
| Output                     | Trait trends across generations   | Sex, Preservation, Location        |
| Core Mechanism             | Evolution over time               | State-action reward optimization   |
| Result Type                | Graphs, Trait convergence         | Accuracy scores, Confusion matrix  |

---

## 📈 Visualizations

- GA: Trait convergence over generations, fitness trends
- RL: Episode-wise reward plots, prediction accuracy, confusion matrices

