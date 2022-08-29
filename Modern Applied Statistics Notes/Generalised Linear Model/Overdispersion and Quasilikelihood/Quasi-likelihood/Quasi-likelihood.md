### Overview
- In a theoretical perfect situation for general linear regression we tend to use the MLE to estimate the parameters of the model/distribution. 
- However, many real life dataset wont tend to follow any theoretical distribution perfectly. In the case of Poisson regression for example, we tend to observe [[Overdispersion]]. 
- Quasi-likelihood is a technique use to estimate the parameters of a model without assumming and underlying statistical distribution and hence can be used to overcome certain limitations.


### Pros
- Extremely robust as no underlying theoretical distribution is assumed
- Can be used to solve problems of [[Overdispersion]]

### Cons:
- Parameter estimate tends to have higher standard error (the trade off to have a better robust model)



### Definition
If $E(Y_i) = \mu_{i}$ and $Var(Y_i) = \phi v(\mu_i)$ ([[Variance function]]), then we let the score $u_i$
- $u_i=\frac{Y_i-\mu_i}{\phi v(\mu_i)}$

![[Pasted image 20220829170144.png]]
- 



![[Pasted image 20220829170246.png]]

### Model Selection
[[Model Selection Quasideviance]]

### Example
[[Quasi-Binomial]]
[[Quasi-Poisson]]
[[troutegg-2.pdf]]
[[Faraway - Quasi-likelihood-1.pdf]]




### Proofs
Proof for $E(\frac{dlogL}{d\theta}) = 0$
![[IMG_0341.jpg]]

![[IMG_0342.jpg]]
