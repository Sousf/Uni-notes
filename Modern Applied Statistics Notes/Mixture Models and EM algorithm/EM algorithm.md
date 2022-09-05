### Overview
- The expectation-maximization (EM) algorithm aims to obtain the maximum likelihood estimates (MLEs) of parameters of a [[Mixture Models]]

### Theorem
- If we observe independent samples $X_1,...,X_n$ from GMM, the likelihood function of the parameters, $θ = (π_1,...,π_{K −1},μ_1,σ^2_{1},...,μ_K ,σ^2_K )$, is
 ![[Pasted image 20220905150651.png]] 
where f (xi ; μk ,σ2k ) is the probabilitydensity function of a normal (gaussian) distribution with mean = $μ_k$ and variance $σ^2_k$ .

We will describes the EM algorithm which aims to obtain the MLE of $θ = (π_1,...,π_{K −1},μ_1,σ^2_{1},...,μ_K ,σ^2_K )$ given observations ${X_1,...,X_n}$


#### Mle of normal distribution
![[Pasted image 20220905151041.png]]


#### Mle of gmm
![[Pasted image 20220905151143.png]]
![[Pasted image 20220905151150.png]]
![[Pasted image 20220905151412.png]]
![[Pasted image 20220905151509.png]]

A common unknown variable above is $P(Z_i = k|X_i)$
- If we know what this is, we can compute $\hat{\mu}$, $\hat{\sigma}^2$, $\hat{\pi}$
- This can be solve through **iterations**.

#### MLE of mixture model iteration step
- **The following 2 pictures are of the same step with different interpretation.**
![[Pasted image 20220905152024.png]]
![[Pasted image 20220905152035.png]]



### Advantages:
- Guranteed "positive" hill-climbing behaviour
- Fast to converge
- Results in probabilistic cluster assignment


### Disadvantage:
- Has an element of randomness - final model may differ depending on initial parameters.
- Can get stuck in a local maximum; not guaranteed to find the maximum-likelihood solution
- The number of clusters (k) must be assumed.

