### Overview:
- Implementation of [[MCMC]]
- Used to simulate data from a joint bivariate distribution
- It  is difficult to simulate data from a distribution $f(x,y)$
	- However, it is easy to simulate from the conditional distribution of $f(x|y)$ and $f(y|x)$



### Procedure
1. Start at  some $x^0,y^0$
2. Sample $x^1$ from $f(x^0|y^0)$
3. Sample $y^1$ from $f(x^1|y^0)$
4. Repeat step 2 - 3

- **Can think of Gibbs sampling as a form of [[Metropolis–Hastings Algorithm]] with Acceptance Probability A of always = 1.**



### Limitations:
- If the correlation between the variables are strong, Gibbs sampling can be slow.
	- This is because Gibbs sampler samples from conditional distribution, meaning that one variable (y) effects the other (x). If they correlate strongly, Gibbs might be slower to explore the entire sample space as it might get stuck on certain values or track when sampling.
