
# Reinforcement Learning Playground

A hands-on collection of reinforcement learning experiments covering fundamental concepts, classical algorithms, model-free learning, deep reinforcement learning, and exploration strategies.

The repository progresses from simple state-action-reward simulations and Markov Decision Processes (MDPs) to Bellman equations, Value Iteration, Monte Carlo methods, Temporal Difference learning, Q-Learning, SARSA, DQN, PPO, and Multi-Armed Bandits.

The experiments apply these concepts to practical decision-making scenarios including robot navigation, traffic management, recycling robots, games, customer service, finance, dynamic pricing, smart farming, recommendation systems, and exploration problems.

---

## Overview

Reinforcement Learning (RL) is a machine learning paradigm in which an agent learns how to make decisions by interacting with an environment.

At each step, the agent:

```text
State
  ↓
Action
  ↓
Environment
  ↓
Reward + Next State
  ↓
Learning / Policy Update
````

This repository explores how this learning process evolves from simple rule-based simulations to value-based, policy-based, and deep reinforcement learning approaches.

---

## Learning Progression

The experiments are organized to follow the progression of reinforcement learning concepts:

```text
RL Fundamentals
       ↓
Markov Decision Processes
       ↓
Bellman Equations
       ↓
Dynamic Programming
       ↓
Monte Carlo Learning
       ↓
Temporal Difference Learning
       ↓
Q-Learning & SARSA
       ↓
Deep Reinforcement Learning
       ↓
Multi-Armed Bandits
```

---

# Experiments

## 01. Reinforcement Learning Fundamentals

The introductory experiments demonstrate the basic building blocks of reinforcement learning using simple environments.

### Maze Navigation

A robot navigates a grid-based maze containing safe paths and obstacles.

The experiment introduces:

* States
* Actions
* Rewards
* Obstacles
* Goal states
* Cumulative rewards
* Random agent behaviour
* Environment visualization

The robot receives penalties for movement and collisions and a positive reward for reaching the goal.

### Traffic Junction

A grid-based traffic junction is used to introduce decision-making under traffic signals.

The agent must navigate toward a destination while responding to traffic signal states.

The experiment demonstrates how rewards and penalties can influence an agent's interaction with an environment.

---

# 02. Environment Simulation & Policies

These experiments extend the basic RL concepts into more structured decision-making environments.

### Car Journey under Traffic Conditions

A simulated 15 km car journey is modeled using states representing:

* Traffic signal
* Traffic intensity

Possible actions include:

* Go
* Slow down
* Stop

The experiment records:

* State transitions
* Actions
* Rewards
* Travel time
* Traffic-dependent speed

A state transition diagram is also used to represent the decision process.

### Robot Path Simulation

A robot moves along a one-dimensional path toward a goal.

The available actions are:

* Move forward by 1 unit
* Move forward by 2 units
* Stay in place

Deterministic and random policies are compared using:

* Steps taken
* Reward
* Cumulative score
* Policy efficiency

---

# 03. Markov Decision Processes & Dynamic Programming

This section introduces formal MDP modelling and value-based decision-making.

## Recycling Robot MDP

The classic recycling robot problem is modeled as an MDP.

The robot makes decisions based on its battery state and chooses whether to:

* Search for cans
* Wait
* Return to the charging station

The experiment uses **Value Iteration** to determine the optimal policy.

It explores:

* State definitions
* Actions
* Rewards
* Transition probabilities
* Value functions
* Policy optimization
* Convergence

## Tic-Tac-Toe as an MDP

Tic-Tac-Toe is modeled from the perspective of one player attempting to learn an optimal strategy.

The experiment explores:

* State representation
* Action space
* Rewards
* State transitions
* Q-values
* Optimal actions

It also examines how changing the reward for a draw affects the learned strategy.

---

# 04. Bellman Equations

The Bellman equation provides the mathematical foundation for many reinforcement learning algorithms.

This section applies Bellman methods to different environments.

## GridWorld

A 4×4 GridWorld is used to calculate the value function under a uniform random policy.

The environment contains:

* 16 states
* Four movement actions
* Terminal states
* Step penalties

The experiment includes:

* Bellman updates
* Iterative value estimation
* Convergence analysis
* Value-function visualization
* Transition tables
* Transition diagrams

## Customer Service Call Center

A customer service call center is modeled as an MDP with states representing:

* Idle
* Handling a call
* Break

The available actions include accepting a call and waiting.

The Bellman Expectation Equation is implemented to iteratively estimate state values under a uniform policy.

---

# 05. Monte Carlo Reinforcement Learning

Monte Carlo methods estimate value functions using complete episodes and observed returns.

## Monte Carlo Maze Navigation

A robot learns to navigate a grid-based maze using Monte Carlo methods.

The environment contains:

* Open spaces
* Obstacles
* Start state
* Goal state

Rewards encourage the robot to reach the goal while avoiding obstacles and minimizing unnecessary movement.

The experiment demonstrates how complete episode returns can be used to learn an effective policy.

## Monte Carlo Portfolio Optimization

Monte Carlo simulation is applied to investment portfolio decision-making.

The environment considers factors such as:

* Asset prices
* Volatility
* Portfolio allocation
* Economic conditions

Actions represent different portfolio allocations.

The objective is to maximize long-term return while accounting for risk.

---

# 06. Temporal Difference Learning

Temporal Difference learning updates value estimates using information from the current transition rather than waiting for an entire episode to finish.

## TD(0) — Student Study Habits

Student behaviour is modeled using states such as:

* Focused
* Distracted
* No Study

Each state has an associated learning reward and probabilistic transitions.

TD(0) is used to estimate the long-term value of different study habits.

The experiment includes:

* State transitions
* TD updates
* Value estimation
* Learning curves

## TD(0) — Stock Market Trends

A simplified stock market is represented using three market states:

* Bullish
* Stable
* Bearish

Different rewards represent market returns.

TD(0) is used to estimate the long-term value of each market state over simulated trading days.

---

# 07. Q-Learning & SARSA

This section explores model-free control methods.

## SARSA — Customer Service Routing

A customer service system is modeled as a sequence of departments:

```text
Reception
    ↓
Technical Support
    ↓
Billing
    ↓
Manager
    ↓
Resolution
```

The agent learns how to route calls efficiently while avoiding incorrect transfers.

Rewards reflect:

* Correct routing
* Incorrect routing
* Time costs
* Successful resolution

SARSA is used to learn the routing policy.

## SARSA — Course Recommendation

An online learning platform is modeled as a recommendation environment.

Learner states include:

* Browsing
* Watching lectures
* Attempting quizzes
* Inactive

Possible recommendation actions include:

* Sending reminders
* Suggesting similar courses
* Offering discounts
* Showing success stories

The objective is to learn actions that encourage engagement and course completion.

---

# 08. Deep Reinforcement Learning

Deep RL combines reinforcement learning with neural networks to handle more complex state representations and decision problems.

## DQN & PPO — Dynamic Pricing

A custom dynamic pricing environment is developed for an online retail setting.

The environment considers factors such as:

* Inventory
* Competitor pricing
* Day of the week
* Previous price
* Customer sentiment

The agent selects different price levels with the objective of maximizing cumulative profit.

Two deep RL algorithms are explored:

* Deep Q-Network (DQN)
* Proximal Policy Optimization (PPO)

The experiments examine pricing behaviour and cumulative rewards.

## DQN & PPO — Smart Farming

A smart farming environment models decisions involving:

* Soil moisture
* Rainfall
* Nutrient levels
* Temperature
* Crop growth stage

The agent learns irrigation and fertilizer strategies.

The reward function considers:

* Crop growth
* Profit
* Resource usage
* Over-irrigation
* Under-irrigation
* Nutrient imbalance

PPO and DQN are used to explore automated farm-management decisions.

---

# 09. Multi-Armed Bandits

The final experiment explores the exploration-exploitation problem.

A 10-armed bandit environment is created where each arm has an unknown reward probability.

The agent must identify profitable arms while balancing:

```text
Exploration
     vs.
Exploitation
```

The following strategies are compared:

### ε-Greedy

Two exploration rates are investigated:

* ε = 0.1
* ε = 0.01

### Upper Confidence Bound (UCB)

UCB dynamically balances estimated reward and uncertainty when selecting an arm.

Performance is analyzed using cumulative reward and reward progression over time.

---

# Algorithms Covered

| Category            | Algorithms / Concepts              |
| ------------------- | ---------------------------------- |
| Fundamentals        | States, Actions, Rewards, Policies |
| MDP                 | Markov Decision Processes          |
| Dynamic Programming | Bellman Equation, Value Iteration  |
| Monte Carlo         | Monte Carlo Value / Control        |
| Temporal Difference | TD(0)                              |
| Value-Based RL      | Q-Learning                         |
| On-Policy RL        | SARSA                              |
| Deep RL             | DQN                                |
| Policy Optimization | PPO                                |
| Bandits             | ε-Greedy, UCB                      |

---

# Applications Explored

The experiments demonstrate reinforcement learning across multiple decision-making domains:

* 🤖 Robot navigation
* 🚗 Traffic management
* ♻️ Recycling automation
* 🎮 Game strategy
* 💼 Customer service routing
* 📈 Portfolio optimization
* 📊 Stock market modelling
* 🎓 Course recommendation
* 🛒 Dynamic pricing
* 🌱 Smart farming
* 🎰 Multi-armed bandits

---

# Repository Structure

```text
reinforcement-learning-playground/
│
├── README.md
├── requirements.txt
├── LICENSE
├── .gitignore
│
├── 01_fundamentals/
│   ├── README.md
│   ├── maze_navigation.ipynb
│   ├── traffic_junction.ipynb
│   ├── traffic_conditions.ipynb
│   └── robot_path_policies.ipynb
│
├── 02_mdp_and_dynamic_programming/
│   ├── README.md
│   ├── recycling_robot_value_iteration.ipynb
│   ├── tic_tac_toe_mdp.ipynb
│   ├── bellman_gridworld.ipynb
│   └── bellman_call_center.ipynb
│
├── 03_model_free_rl/
│   ├── README.md
│   ├── monte_carlo_maze.ipynb
│   ├── monte_carlo_portfolio.ipynb
│   ├── td0_study_habits.ipynb
│   ├── td0_stock_market.ipynb
│   ├── sarsa_customer_service.ipynb
│   └── sarsa_course_recommendation.ipynb
│
├── 04_deep_reinforcement_learning/
│   ├── README.md
│   ├── dqn_ppo_dynamic_pricing.ipynb
│   └── dqn_ppo_smart_farming.ipynb
│
└── 05_multi_armed_bandits/
    ├── README.md
    └── multi_armed_bandit.ipynb
```

---

# Technologies

The experiments use Python and a range of libraries for simulation, numerical computation, visualization, and reinforcement learning.

### Core

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn

### Reinforcement Learning

* Gymnasium
* Stable-Baselines3
* PyTorch

### Visualization & Simulation

* NetworkX
* Jupyter Notebook

---

# Installation

Clone the repository:

```bash
git clone https://github.com/MansiiSapariya/reinforcement-learning-playground.git
```

Navigate into the repository:

```bash
cd reinforcement-learning-playground
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

Launch Jupyter:

```bash
jupyter notebook
```

Open any experiment from the corresponding folder.

---

# How to Use This Repository

The experiments are organized in a learning-oriented sequence.

If you are new to reinforcement learning, the recommended order is:

```text
01 Fundamentals
       ↓
02 MDP & Dynamic Programming
       ↓
03 Model-Free RL
       ↓
04 Deep RL
       ↓
05 Multi-Armed Bandits
```

Each notebook contains the environment definition, implementation, experiments, visualizations, and observations relevant to that problem.

---

# Key Learning Outcomes

This collection provides practical experience with:

* Formulating real-world problems as MDPs
* Defining states, actions and rewards
* Designing custom environments
* Computing value functions
* Applying Bellman equations
* Finding optimal policies using Value Iteration
* Learning from complete episodes using Monte Carlo methods
* Updating values using TD learning
* Implementing Q-Learning
* Implementing SARSA
* Understanding on-policy vs. off-policy learning
* Applying neural networks to reinforcement learning
* Using DQN for value-based deep RL
* Using PPO for policy optimization
* Understanding exploration vs. exploitation
* Comparing ε-Greedy and UCB strategies
* Visualizing learned policies and value functions
* Applying RL concepts to practical decision-making problems

---

# Classical RL vs Deep RL

One of the main themes of this repository is the progression from classical reinforcement learning to deep reinforcement learning.

### Classical RL

The earlier experiments rely on explicit representations of states and actions.

Examples include:

* Value Iteration
* Monte Carlo
* TD(0)
* Q-Learning
* SARSA

These approaches are useful for understanding the mathematical foundations of RL and work well for relatively small state spaces.

### Deep RL

The later experiments introduce neural-network-based approaches:

* DQN
* PPO

These methods allow RL to be applied to environments with richer state representations and more complex decision-making problems.

---

# Experiment Philosophy

The purpose of this repository is not simply to implement algorithms.

Each experiment attempts to connect an RL concept with a decision-making problem:

```text
RL Concept
     ↓
Environment
     ↓
State Representation
     ↓
Action Space
     ↓
Reward Design
     ↓
Learning Algorithm
     ↓
Policy / Value Function
     ↓
Evaluation
```

This makes it possible to study not only how an algorithm works, but also how the design of the environment and reward function influences the resulting behaviour.

---

# Future Extensions

Potential extensions to this repository include:

* Actor-Critic methods
* Advantage Actor-Critic (A2C)
* Double DQN
* Dueling DQN
* Prioritized Experience Replay
* Multi-Agent Reinforcement Learning
* Continuous-control environments
* Reward shaping experiments
* Hyperparameter optimization
* RL benchmarking
* Real-world datasets
* Offline reinforcement learning
* Model-based reinforcement learning
* More complex simulation environments

---

# Disclaimer

These experiments are primarily educational and experimental implementations.

Several environments use simulated states, transitions, rewards, market conditions, customer behaviour, or other assumptions. Therefore, the results should not be interpreted as production-ready systems or real-world financial, agricultural, pricing, or business recommendations.

---

# Author

**Mansi Sapariya**

MSc Data Science


**I would use this README with `reinforcement-learning-playground` rather than `reinforcement-learning-experiments`.** It feels more like a developer/research portfolio and less like an uploaded coursework archive.
```
