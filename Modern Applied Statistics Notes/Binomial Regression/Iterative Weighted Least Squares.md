### Overview
Suppose $Y = X\beta + \epsilon$ where $\epsilon$ ~ $N(0,\Sigma)$, and $X$ and $\Sigma$ are full rank.

Multiplying by $\Sigma^{-1/2}$ we get $\Sigma^{-1/2}Y = \Sigma^{-1/2}X\beta + \epsilon^{'}$ where $\epsilon^{'}$ ~ $N(0,I)$

What is the least squares estimator for $\beta$

The estimator of $\beta$ that minimises the following sum of squares
$(\Sigma^{-1/2}y - \Sigma^{-1/2}X\beta)^T(\Sigma^{-1/2}y - \Sigma^{-1/2}X\beta)$ = $(y - X\beta)^T\Sigma^{-1}(y - X\beta)$

**is:**
**$\hat{\beta} = (X^T\Sigma^{-1}X)^{-1}X^T\Sigma^{-1}y = (X^TWX)^{-1}X^TWy)$**

**where the weight:** W = $\Sigma^{-1}$

So now:
$g(Y_i) \approx g(\mu_i) + (Y_i - \mu_i)g'(\mu_i)$

Let $Z_i = g(\mu_i) + (Y_i - \mu_i)g'(\mu_i)$ and $\epsilon = (Y_i - \mu_i)g'(\mu_i)$,
**Then**
$Z_i = x_{i}^{T}\beta +\epsilon_i$

**where**
Var $\epsilon_i$ = $(g'(\mu_i))^2Var(Y_i)$

If we knew $Var(\epsilon_i)$ then the estimator of **$\beta$ would be the solution to the weighted least squares problem**:

$\underset{\beta}{min}(z-X\beta)^T\Sigma^{-1}(z-X\beta)$

where $\Sigma$ is diagonal with $\Sigma_{ii} = Var(\epsilon_i)$


We have $g(Y) \approx Z = X\beta + \epsilon$ where $\epsilon = (Y_i - \mu_i)g'(\mu_i)$ 

and $\Sigma = Var(\epsilon)$ is diagonal with entries
$\Sigma_{ii} = (g'(\mu_i))^2Var(Y_i) = (g'(\mu_i))^2v(\mu_i)a(\phi)$

This suggests:
$\hat{\beta} = (X^T\Sigma^{-1}X)^{-1}X^T\Sigma^{-1}z$

**Problem:** $z_i$ and $\Sigma_{ii}$ depend on $\beta$ because $\mu_i = g^{-1}(x_{i}^{T}\beta)$
**Solution** is to iterate

**NOTE**: $a(\phi)$ factor in the expression for $\hat\beta$ cancels out.

![[Pasted image 20220822125328.png]]


**Variance of $\hat{\beta}$ from IWLS algorithm**

![[Pasted image 20220822131405.png]]
![[Pasted image 20220822131419.png]]

![[Pasted image 20220822131443.png]]