# UNIT 1 - INTRODUCTION

## State action and reward: 

RL Processes are a sequience of 'states' $S_i$, 'actions' $A_i$ and 'rewards' $R_i$. The environment hands us a state, our agent takes the state and determines and action and then the environment gives us a reward and a new state. 

>! Rewards can be positive or negative. 

>! not all environments will give us perfect infomration about the state.

**Reward Hypothesis** : All goals can be descrtibed as the maximization of an expected return (cumulative reward).

**Markov Property** : RL processes have the Markov property, that is they are 'memoryless' all that matters for action $A_i$ is state $S_i$

## state and observation space
Some games have imperfect information about the environment. 

a **State** is a full description of the environment. think chess

an **observation** is a partial description of the *state* of the environment. Think AOE, the fog of war is there so you can't see everything, but there is a finite state of teh game at any given second. 

**State Space** is the set of all states of the process, **Observation space** is the set of information we have about he environment. 

## Action Space

The set of all possi9ble actions in an environment in an environment is called the **Action Space**. Sometimes action space is finite, in that case we say there is a **discrete action space** sometimes the set of actions is inifite we call this **continuous action spcace**. Think chess, go, or mario for discrete and self-driving cars, asteroid, or Darksouls, for continuous.

## Rewards
Rewards are the only feedback our agent gets. if $r_t$ is the reward we get for our action $a_{t-1}$, and if $\tau$ is the sequence of actions $a_{t-1},a_t,...$ called a *trajectory* then the **Return** of the trajectory $\tau$ is:

$$R(\tau) = \sum_{k=0}^{\infty}r_{t+k}$$ 

But since Rl processes have negative rewards too, we need to balance risk by weighting the sum by adding a *discount* $\gamma \in (0,1)$ to this sum. 
> generally this discount if between $0.95$ and $0.99$

The closer $\gamma$ is to 1, the smaller the discount is and the more our agent is interested in long term reward, the closer to 0 $\gamma$ is the more the more our agent cares about short term reward. 

so in reality, after adding discounts, the *return* fxn looks like this

$$R(\tau) = \sum_{k=0}^{\infty}\gamma^{k-1} r_{t+k}$$ 



