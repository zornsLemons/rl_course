# Tasks

Tasks come in  2 different flavors. an **episodic task** is one where there is a terminal state, i.e. every travectory $\tau = (a_i)$ is fnite. a **continuing task** is one where every $\tau =(a_i) is$ infinite.

Am agent doing a coninuting task must interact with it's environment and simultaneously find the actions.

# Exploration/Explotiation 

an agent *explores* the environment by randomly acting to gather infomration about the environment, and agent *exploits* the environment to maximize reward. Going straight to the exploit without exploring sufficiently risks finding local optima that are not globally optimal or even winning, where as over exploring takes away precious cycles from exploting the crap out of a winning strategy. 

>Remember the cannonical restraunt example


# Policy v Value approach

There are 2 Approaches to RL problems, the **policy** based methods and the **Value** based methods. a **policy** based method focuses on setting an action based on the state the agent is in where as a **value** based method understands the action based on the possible return from the available next states.

For this section, let $S$ be the state space or set of all possible states and let $A$ be the action space, the set of all possible actions. 

## Policy fxn
in a polict based approach we seek to find a fxn $\pi : S \rightarrow A$ that specifies the action the agent ought to take when in state S. 
in the policy approach, the goal is to directly learn the actions to take based on current state, in a value approach we learn $\pi$ indirectly by assesing the most valuable next state.

## policy based approach
in a policy approach, $\pi$ is a mapping of states to actions. this can be a deterministic process $a=\pi(s)$ ($\pi$ is effecitvely a table) or a probabalistic approach, $\pi(a\vert s) = P(A \vert s)$ where $\pi$ is defined as a condiditional probability distribution over $A$ given $s$.

## value base methods

In a value based method we learn a **value fucntin**
 $\v_{\pi} : S \rightarrow R$ such that 
$$ v_{\pi} = E[R(\tau) = \sum_{k=0}^{\infty}\gamma^{k-1} r_{t+k} \vert S_{t-1} = s] $$

## Deep Reinforcement learning is deep b/c:

We don't do tables anymore, we use an nn. 





