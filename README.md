# Reinforcement Learning GridWorld Agent

This project demonstrates how a **Reinforcement Learning agent learns to navigate an environment and reach a goal using Q-Learning**.

Instead of only training the model, the project focuses on **visualizing the learning behavior of the agent**. You can see how the agent explores the environment, learns from rewards, and finally follows the optimal path to the goal.

This makes it a **good beginner project for understanding Reinforcement Learning concepts in practice**.

---

# Project Overview

The environment used in this project is called **GridWorld**.

It is a simple grid-based environment where:

- An **agent** starts at a starting position.
- The environment contains **obstacles**.
- There is a **goal** the agent must reach.
- The agent can move **Up, Down, Left, or Right**.

During training, the agent receives **rewards and penalties**, which help it learn the best path.

After enough training episodes, the agent learns the **optimal policy** and reaches the goal efficiently.

---

# Environment Representation

Example GridWorld:

A . . . .

. O . . .

. . . O .

O . . . .

. . . . G


Symbols used in the grid:

| Symbol | Meaning |
|------|------|
| A | Agent |
| O | Obstacle |
| G | Goal |
| . | Empty space |

---

# Reinforcement Learning Concept Used

This project uses the **Q-Learning algorithm**, a popular model-free reinforcement learning technique.

The agent learns by interacting with the environment and updating a **Q-table**.

The Q-table stores the **expected reward for taking a specific action in a specific state**.

Over time, the Q-values improve and the agent learns the best action for each state.

---

# Reward System

The agent receives rewards based on its actions:

| Action Result | Reward |
|------|------|
| Reach Goal | +10 |
| Hit Obstacle | -10 |
| Normal Move | -1 |
| Move Outside Grid | -1 |

The small negative reward encourages the agent to **find the shortest path to the goal**.

---

# Learning Strategy

The agent follows an **Epsilon-Greedy strategy**:

### Exploration
The agent sometimes chooses a **random action** to explore new paths.

### Exploitation
Other times it chooses the **best known action from the Q-table**.

This balance allows the agent to **discover better solutions while still using learned knowledge**.

---

# Q-Learning Update Rule

The Q-table is updated using the Q-learning formula:

Q(s,a) = Q(s,a) + α [ r + γ max(Q(s',a')) − Q(s,a) ]



---


Where:

| Symbol | Meaning |
|------|------|
| s | current state |
| a | action |
| r | reward |
| s' | next state |
| α | learning rate |
| γ | discount factor |

This update gradually improves the agent's policy.

---

# Training Parameters

The agent is trained using the following settings:

| Parameter | Value | Purpose |
|------|------|------|
| Episodes | 5000 | Number of training iterations |
| Alpha | 0.1 | Learning rate |
| Gamma | 0.9 | Importance of future rewards |
| Epsilon | 0.1 | Exploration probability |

---

# Features of This Project

- Custom **GridWorld environment**
- Implementation of **Q-learning from scratch**
- **Policy visualization** using directional arrows
- **Step-by-step agent simulation**
- Interactive **play and step controls**
- Clear **grid rendering for visualization**

---

# Policy Visualization

After training, the learned policy can be visualized using arrows:

→ → ↓ ↓ ↓

↓ X ↓ → ↓

→ → ↓ X ↓

X → → → ↓

↓ → → → G


Each arrow shows the **best action the agent learned for that position**.

---

# Watching the Agent

The project includes a simulation mode where you can **watch the trained agent move through the environment**.

Controls:

| Key | Action |
|------|------|
| p | Play automatically |
| s | Move one step |
| q | Quit simulation |

This helps visualize **how the learned policy guides the agent to the goal**.

---

# Try It Yourself

You can run the project directly in Google Colab:

https://colab.research.google.com/drive/1ZhX4LCXe_6e-N8IsWiDWmdkpxF7pYc-e?usp=sharing

No installation required — just open the notebook and run the cells.

---


# What This Project Demonstrates

This project helps understand several important reinforcement learning concepts:

- Environment design
- State representation
- Reward engineering
- Exploration vs exploitation
- Q-table learning
- Policy visualization

It shows how even a **simple environment can demonstrate the core idea behind reinforcement learning**.

---



# Learning Outcome

By building this project, you will understand:

- How reinforcement learning agents interact with environments
- How rewards shape agent behavior
- How Q-learning updates knowledge over time
- How policies emerge from repeated training

---

