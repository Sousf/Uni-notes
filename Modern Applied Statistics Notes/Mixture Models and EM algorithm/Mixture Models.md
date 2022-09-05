### Overview
- Want to find the over-arching distribution from samples of $X_i$ that has its own distribution.
- When each sample $X_i$ is distributed normally, then we call the the overaching distribution a **Gaussian Mixture Model** (GMM)




### Theorem:
- **Assume** we observe independent samples $X_1, X_2,... ,X_n$ and that each $X_i$ is sampled from one of K mixture components.
- **Associated** with each random variable $X_i$ is a label $Z_i$  $\epsilon$ {1,...K} which indicates which component $X_i$ came from.

We assume that $Z_1,...,Z_n$ are independent and identically distributed as  
follows. For i = 1 ...,n,

$$Z_i \sim categorical(\pi_1,...,\pi_n)$$
- $Z_i$ follows a categorical distribution with $\pi_1,...,\pi_n$ as parameters
- $Z_i$ = k with probability $\pi_k$ for k = 1,...,K
- each $\pi_i$ is the probability that the label $Z_i$ is some $k$
- Here, the $\pi_k$ are called **mixture proportions** or **mixture weights** and they represent the probability that $X_i$ belongs to the **k**-th mixture component.
- The **mixture proportions** are **nonnegative** and they sum to one.
	- $\Sigma\pi_k = 1$


We assume that $X_1,...,X_n$ conditional on $Z_1,...,Z_n$ are independent and  
identically distributed as follows. For i = 1 ...,n,

$$(X_i |Z_i = k) \sim P (X_i |\theta k )$$
- **k = 1,...,K**
- This is the distribution of each sample $X_i$ given that we know its label $Z_i = k$
- We call $P (X_i |\theta k )$ the **mixture component**, and it represents the  
distribution of $X_i$ assuming it came from component k (i.e., $Z_i$ = k ).

#### probability of observing the independent samples $X_1,...,X_n$
![[Pasted image 20220905141638.png]]

This is also the **Likelihood function** for observing the samples and can be use to calculate **MLE**
![[Pasted image 20220905141813.png]]

#### Finding mle using the [[em algorithm]]


#### Final goal
- After we have obtained the MLE estimate. **We want to infer, given a data point $X_i$ , which component it is likely to belong to**. More precisely, we want to **compute** $P (Z_i = k |X_i )$ for k = 1,...,K.
![[Pasted image 20220905142142.png]]


