### Overview:
- An implementation of [[MCMC]]


### Process:
1. Start with an initial value of $\theta^0$, set $t = 0$
2. Use $q(\theta^0,.)$ to generate a new $\theta^{\prime}$
3. Define the acceptance probability **A** as
	1. ![[Pasted image 20220928120818.png]]
	2. Where $\theta^{\prime}$ is the next proposed value for the parameter
	3. Where $\pi(\theta)=P(\theta,x_1,...,x_n)=P(\theta)P(x_1,...,x_n | \theta)$
	4. Where $q(\theta, \theta^{\prime})=P(\theta^{\prime} | \theta)$
4. Here we can say that the Probability of accepting $\theta^{\prime}$ as the new $\theta^{1}$ is **A** and the probability of keeping the value of $\theta^{0}$ as the value for $\theta^{1}$ is **$1-A$**. We pick the value with the highest probability.
5. Increase **t**, now we return to step 2.


![[Pasted image 20220928121344.png]]
![[Pasted image 20220928121356.png]]

### Example:
[[MHexample-1.pdf]]

#### Random walk metropolis hasting
![[Pasted image 20221024190640.png]]

![[Pasted image 20221024190714.png]]