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
![[Pasted image 20220908141004.png]]

- This can be solve through **iterations**.

#### MLE of mixture model iteration step
- **The following 2 pictures are of the same step with different interpretation.**
![[Pasted image 20220905152024.png]]
![[Pasted image 20220905152035.png]]

### EM algorithm for general latent variable (Z)

- Let **X** be the entire set of observed variables and **Z** be the entire set of latent variables. The log-likelihood is therefore:

$$log(P(X|\theta)) = log(\sum_{Z}P(X,Z|\theta))$$
where we've simply maginalized **Z** out of the joint distribution.
- As we noted above, the existence of the sum inside the logarithm prevents us from applying the log to the densities which results in a complicted expression for the MLE.
- Also if we knew **Z**, the maximization would be easy. We **typically don't know Z**, but the **information we do have about** **Z is contained in the [[Posterior]] $P(Z|X,\theta)$**.
- Since we don't know $log(P(X,Z|\theta))$ (which is called the [[Complete log-likelihood]]), we consider its expectation under the posterior distribution of the latent variables. We maximize this expectation to find a new estimate for the parameters.
- $log(P(X|\theta))$ is called the [[Incomplete log-likelihood]].

#### General em algorithm steps
1. Initialize the current values of $\theta$. Let $\theta^0$ denote the current values. Evaluate the [[Incomplete log-likelihood]] with $\theta^0$.
2. **E-Step:** Using $\theta^0$, compute the [[Posterior]] distribution of the latent variables given by $P(Z|X,\theta^0)$
3. **M-Step:** Obtain new parameter estimates $\hat{\theta}$ which maximise the expectation of the [[Complete log-likelihood]] with respect to this **posterior** $P(Z|X,\theta^0)$. Specifically, $$\hat{\theta}=argmax_\theta Q(\theta, \theta^0)$$ where  $$Q(\theta, \theta^0)=E_{Z|X,\theta^0}[log(P(X,Z|\theta))]$$
4. Evaluate the [[Incomplete log-likelihood]] with $\hat{\theta}$. If the [[Incomplete log-likelihood]] has changed by less than some small $\epsilon$, stop. Otherwise, replace the current values with the new parameter estimates $(\theta^0,\hat{\theta})$ and go back to step 2.


#### example of one derivation for one iteration of em algorithm
- [[EM-Algorithm-One-Iteration-Example.pdf]]

#### Code example for em algorithm
- [[EM-1.pdf]]




### Advantages:
- Guranteed "positive" hill-climbing behaviour
- Fast to converge
- Results in probabilistic cluster assignment


### Disadvantage:
- Has an element of randomness - final model may differ depending on initial parameters.
- Can get stuck in a local maximum; not guaranteed to find the maximum-likelihood solution
- The number of clusters (k) must be assumed.

