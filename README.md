# Application-of-reinforcement-learning-for-financial-trading

The Financial Trading System that we chose is inspired by F. Bertoluzzo & al "Testing Different Reinforcement Learning configurations for financial trading: Introduction and applications".

We start by defining the state as the last five percentage returns of the traded asset (corresponding to the last five trading days): 

$$latex s_t = (r_{t-4}, r_{t-3}, r_{t-2}, r_{t-1}, r_t)$$

Where $r_t$ is the log return of the asset $r_t = log(P_t) - log(P_{t-1})$

Concerning the actions, we use the following :

$$ a_t =
    \begin{cases}
        -1 & \text{sell signal}\\
        0 & \text{stay out of the market signal} \\
        1 & \text{buy signal}
    \end{cases}$$

As for the immediate reward: $r_t = a_{t-1} * (log(P_t) - log(P_{t-1})))$

We define the total gains of the trading strategy as follows :

$G = \sum_t r_t$
