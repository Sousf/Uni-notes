### Definition
- Y is a GLM if it is from an exponential family, and that
- $\mu$ is defined as $E(Y) = g^{-1}(x^T\beta)$
- where **g** is a monotonic differentiable funtion called the link function
- where **x** is a vetor of independent (predictor) variables,
- where **$\beta$** is a vector of parameters

**Note**:
- $\mu =  g^{-1}(x^T\beta) \rightarrow g(\mu) = x^T\beta$
- A good estimator for $\mu$ is $\hat{\mu}_i = y_i$



### Canonical link
Recall Y is from an exponential family if
- **$f(y; \theta, \phi) = exp[\frac{y\theta - b(\theta)}{a(\phi)} + c(y, \phi)]$
- if $g(\mu) = g(E(Y)) = x^T\beta = \theta$ then $g$ is called the cannonical link. Since $\mu = b'(\theta)$, it follows that the canonical link must be $(b')^{-1}$

![[Pasted image 20220823141806.png]]



