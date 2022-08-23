### Important note
In this section we will adopt the convention that $a(\phi) = \phi$


### Definition
- The scale deviance for model A is:
	- $\frac{D^A}{\phi} = -2log(\frac{l(\hat{\beta^{A}})}{l(S)})$
	- **where** $\hat{\beta^{A}}$ is the MLE of $\beta^{A}$, the parameters in the model A, and $l(S)$ is the maximum likelihood for the saturated model
	- The **deviance** is just $D^A$

The saturated model ([[Scale Deviance#The Saturated model]]) uses $y_i$ to estimate $\mu_i$

The deviance can be written as  $D = \Sigma_id_i$ where
- $d_i = (y_i - \hat{\mu_i})^2$
- where $\hat{\mu}_i$ is the fitted mean using the MLE.
- **It is equvalent to SSE (sum of squared errors) in linear models.**

![[Pasted image 20220822141229.png]]
![[Pasted image 20220822141239.png]]
![[Pasted image 20220822141252.png]]

![[Pasted image 20220822141942.png]]

![[Pasted image 20220822142006.png]]
