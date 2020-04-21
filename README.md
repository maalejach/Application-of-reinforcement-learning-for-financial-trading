# Application-of-reinforcement-learning-for-financial-trading

The Financial Trading System that we chose is inspired by F. Bertoluzzo & al "Testing Different Reinforcement Learning configurations for financial trading: Introduction and applications".

We start by defining the state as the last 5-30 (variable) log returns of the traded asset (corresponding to the last five trading days)

We will adapt a daily trading strategy. Each day, at the market opening, the agent has the choice between 3 actions :
0 : no action 
1 : buy (long)
-1: sell (short)

The instant reward of the agent at the end of the day is the log return of the asset r_t = log(P_t) - log(P_{t-1})

We define the total gains of the trading strategy as the sum of all the daily rewards until the current instant.

## Reinforcement learning methods implemted :

- Kernel based reinforcement learning
- Deep q-learning (DQN) & double deep Q-learning (DDQN)
- Evolution strategy with deep reinforcement learning
