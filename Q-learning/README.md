# Q-Learning

## Introduction

Q-Learning is a model-free reinforcement learning algorithm used to learn the optimal action-selection policy for a given Markov decision process (MDP). It belongs to the class of value iteration algorithms, where an agent learns to make decisions by estimating the value of each possible action in each possible state.

## Q-Value Function

At the core of Q-Learning lies the Q-value function (also known as the action-value function), denoted as Q(s, a), which represents the expected cumulative reward of taking action "a" in state "s" and following the optimal policy thereafter. The Q-value for a given state-action pair is updated iteratively based on observed rewards and transitions.

The Q-value update equation, also known as the Bellman equation, is as follows:

$Q(s, a) = Q(s, a) + α * [reward + γ * max(Q(s', a')) - Q(s, a)]$
$\text{Q}(s, a) = \text{Q}(s, a) + \alpha \left[ \text{reward} + \gamma \max(\text{Q}(s', a')) - \text{Q}(s, a) \right]$


## Q-Table

The Q-table is a data structure used to store the Q-values for all possible state-action pairs. It is typically represented as a two-dimensional array or dictionary, where the rows correspond to states and the columns correspond to actions.

Where:
- $Q(s, a)$ is the Q-value for state-action pair (s, a).
- α (alpha) is the learning rate, controlling the weight given to new information.
- γ (gamma) is the discount factor, determining the importance of future rewards.
- reward is the immediate reward received after taking action "a" in state "s".
- $max(Q(s', a'))$ is the maximum Q-value among all possible actions in the next state "s'".

## Q-Learning Algorithm

The Q-Learning algorithm can be summarized as follows:

1. **Initialization**: Initialize the Q-table with arbitrary values or set it to zero.
2. **Exploration vs. Exploitation**: During each time step, the agent selects an action based on an exploration-exploitation trade-off.
3. **Action Selection**: The agent selects an action using an exploration strategy, such as ε-greedy or softmax.
4. **Observation and Reward**: After taking an action, the agent observes the resulting state and receives a reward.
5. **Q-Value Update**: Update the Q-value for the previous state-action pair using the Q-learning update rule.
6. **Repeat**: Continue the process of selecting actions, observing outcomes, and updating Q-values until convergence or a predefined number of iterations.

## Applications of Q-Learning

Q-Learning has diverse applications across various domains, including:

- **Game Playing**: Q-Learning has been successfully applied to various games, including board games (e.g., Tic-Tac-Toe) and video games.
- **Robotics**: Q-Learning can be used to train robots to navigate environments and perform tasks autonomously.
- **Optimization**: Q-Learning has applications in optimization problems, such as route planning and resource allocation.

## Implementation Example

Check out the [Q-Learning implementation](Q_Learning_Implementation.ipynb) notebook in this repository for a practical example of Q-Learning applied to a simple environment.

Feel free to experiment with the code, tweak parameters, and explore different scenarios!

Happy learning and exploring! 🤖
