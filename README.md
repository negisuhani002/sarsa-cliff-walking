# SARSA and Q-Learning using Reinforcement Learning

## Overview
This project implements two Temporal Difference (TD) reinforcement learning algorithms, **SARSA** and **Q-Learning**, using Gymnasium's `CliffWalking-v1` environment.

The project covers Q-table initialization, ε-greedy action selection, algorithm implementation, training, and evaluation of the learned policies.

## Environment
- Environment: `CliffWalking-v1`
- States: 48
- Actions: 4 (Up, Right, Down, Left)
- Q-table shape: 48 × 4
- Goal: Reach the destination while avoiding the cliff

## Technologies Used
- Python
- NumPy
- Random
- Gymnasium

## Project Workflow

### 1. Environment Setup
- Created the CliffWalking environment using Gymnasium.
- Initialized a Q-table with zeros.
- Defined the state and action spaces.

### 2. Hyperparameter Configuration
- Episodes: 500
- Learning rate (α): 0.5
- Discount factor (γ): 0.99
- Exploration rate (ε): 0.1

### 3. SARSA Implementation
- Implemented the SARSA on-policy learning algorithm.
- Used an ε-greedy policy for action selection.
- Updated Q-values using the next action selected by the current policy.

### 4. Q-Learning Implementation
- Implemented the Q-Learning off-policy algorithm.
- Used an ε-greedy policy during training.
- Updated Q-values using the maximum Q-value of the next state.

### 5. Model Evaluation
- Evaluated the trained agents using their learned Q-tables.
- Selected the highest-valued action at each state during evaluation.
- Recorded the total reward and episode length.

## Results

| Algorithm | Total Reward | Episode Length |
|---|---:|---:|
| SARSA | -17 | 17 steps |
| Q-Learning | -13 | 13 steps |

The results represent the recorded evaluation runs. Rewards may vary across runs because of randomness during training.

## Key Learnings
- Understanding Temporal Difference learning
- Implementing SARSA and Q-Learning
- Understanding on-policy and off-policy learning
- Working with Q-tables
- Balancing exploration and exploitation using ε-greedy policy
- Training and evaluating agents in Gymnasium

## Conclusion
This project provided practical experience in Reinforcement Learning by implementing and evaluating SARSA and Q-Learning in the CliffWalking environment. It helped demonstrate the difference between on-policy and off-policy learning through their Q-value update strategies.

## Notebooks
- `sarsa.ipynb` – SARSA implementation and evaluation
- `q_learning.ipynb` – Q-Learning implementation and evaluation
