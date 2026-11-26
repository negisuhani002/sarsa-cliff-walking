# SARSA Cliff Walking using Reinforcement Learning

## Overview
This project implements the **SARSA (State-Action-Reward-State-Action)** algorithm using Gymnasium's `CliffWalking-v1` environment.

The project covers environment setup, Q-table initialization, ε-greedy action selection, SARSA learning, training, and evaluation of the learned policy.

## Environment
- Environment: `CliffWalking-v1`
- States: 48
- Actions: 4 (Up, Right, Down, Left)
- Q-table: 48 × 4
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

### 3. ε-greedy Policy
Implemented an ε-greedy policy to balance exploration and exploitation.

- Exploration: Select a random action.
- Exploitation: Select the action with the highest Q-value.

### 4. SARSA Training
Implemented the SARSA update rule:

\[
Q(s,a) \leftarrow Q(s,a)+\alpha
[r+\gamma Q(s',a')-Q(s,a)]
\]

The agent learns by interacting with the environment and updating its Q-values after each step.

### 5. Agent Evaluation
- Used the learned Q-table to select the highest-valued action at each state.
- Evaluated the agent's learned behavior in the CliffWalking environment.
- Tracked the total reward and episode length.

## Results

**Total Reward: -17**

**Episode Length: 17 steps**

The trained agent successfully reached the goal in the CliffWalking environment.

## Key Learnings
- Understanding on-policy Temporal Difference learning
- Implementing SARSA from scratch
- Working with Q-tables
- Understanding exploration and exploitation
- Learning the ε-greedy policy
- Training and evaluating an agent using Gymnasium

## Conclusion
This project provided practical experience in Reinforcement Learning by implementing the SARSA algorithm and training an agent to navigate the CliffWalking environment using Q-value updates and an ε-greedy policy.
