#GamePlayingWithML 


## Overview
- We know that supervised learning is for single step prediction, e.g predict Saturday's weather based on Friday's weather
- Temporal Difference (TD) learning is for multi-step prediction, e.g predict Saturday’s weather based on Monday’s weather, then update prediction based on Tue’s, Wed’s, ...  
- e.g. predict outcome of game based on first move, then update prediction as more moves are made
- **TD learning is a form of reinforcement learning**


## TDLeaf($\lambda$) algorithm
- Combines temporal difference learning with [[MiniMax Search]].
- Basically computes the evaluation score (and running it through tanh(x) function to squash the range to be between 0 and 1), take the difference of the evaluation score between each successive state, this difference is called the **temporal difference**. **Our goal is** to minimise this **temporal difference** so that the model is more consistent between each stage. We then use this difference in our weight update function.




## Explanation

- ![[Pasted image 20220403090853.png]]



## Optimisation
- Can use the strategy of [[Gradient Descent]], but the weight update rule will be different.
- The way we would optimise it is to use the following
	- the **temporal difference** is $d_i = r(s^{l}_{i+1}, w) - r(s^{l}_{i}, w)$
	- The **weight update rule** is
	- ![[Pasted image 20220403091142.png]]


## How to set $\lambda$ values
- When $\lambda$ is 0, weights are adjusted to make the estimated reward of each state closely approximate **that of the next state**, rather than the final utility. This is useful when the evaluation function is stable and is good. 
- However, if we are not confident that our evaluation function is great ( **The function is bad and not stable** ), then we can have a high value for $\lambda$ that will tell the algorithm to adjust the weights such that each state reward will **approximate the true utility value of the final state**. 


## Problems with using a supervised ML approach with Gradient Descent for game playing learning
- **Delayed reinforcement** - reward resulting from an action may not be received until several time steps later, which also slows down the learning.
	- May have to play through the entire game to get some feedback on how the agent perform, rather than immediately after a move is made. 
	- This slows down the learning process. Have to play complete games to learn, rather than learning after every move.
- **Credit assignment** - need to know which action(s) was responsible for the outcome.
	- Can't exactly say which move was critical, good, or bad. 
	- We only have a sequence of move but not sure which one, not sure how to assign credit. 
- [[Temporal Difference Learning#TDLeaf lambda algorithm]] can be use to address these problems.







