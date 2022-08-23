### Overview
- Use to predict the odds of seeing an event, given a vector of regression variables.
- $Y = bin(n_i , p_i = g^{-1}(\eta_i))$
	- where $\eta_i = x_{i}^{T}\beta => \beta_0 + \beta_1x_1 + \beta_2x_2 + ...$


### PMF of Binomial Distribution
**$Pr(y = k) = {n \choose k}p^k(1-p)^{n-k}$**

Where
- **y** is the number of successes observed in **n trials**
- **p** is the success rate

### Link function g(.)
- the success rate **p** is usually modelled by a linking function **g(x)**
- **$p = g(\eta)^{-1}$**
- **x** is some input (quality or feature) that **g(x)** will take

- **g(x)** is usually a **logit** (also known as **log odds**) function:
	- $g(\eta)^{-1} = p = \frac{1}{1+exp(-\eta)} = \frac{exp(\eta)}{1+exp(\eta)}$ 
	- $g(p) = \eta = log(\frac{p}{1-p}) = \theta$
	- 

### Parameter estimation
**To estimate the Parameters of Binomial Regression, we use  MLE**
- We use this because MLE doesnt require the outcome to be normally distributied (because it is binomially distributed in this case)

**Steps to estimating the parameters:**
1. Identify the Marginal PMFs
	- $Pr(y = k) = {n \choose k}p^k(1-p)^{n-k}$

1. Find the Likelihood function 
	- $\Pi{n \choose k}p^k(1-p)^{n-k}$

2. Find the log likelihood equation
	- when taking the log of the likelihood function above, we can ignore terms that do not contain the parameters $\beta$, $\eta$ and $p$ contains $\beta$ however
	- after some algebra, we will get
	- **C** + $\Sigma[y_i\eta_i - m_ilog(1+exp(\eta_i))]$
	- where **C** are all terms that do not contain $\beta$

3. maximise this log likelihood equation
	- Find the Maximum value  for each $\beta_i$ by taking derivative with respect to each $\beta$ and setting the equation to 0
	- R has its own way of doing this


**Important note about Parameter Estination**
- This is done differently in R
- it turns out that we can compute the parameters by solving a least square problem
- This technique is called [[Iterative Weighted Least Squares]]


The Parameters distribution is
$\hat{\theta} = N(\theta, I(\theta)^{-1})$







