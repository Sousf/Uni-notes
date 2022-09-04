$$\phi = \frac{X^2}{(n-p)}$$

Where $X^2$ is Pearson residual of the model.
Also:
$$\phi = \frac{X^2}{(n-p)}$$
follows Chi Squared Distribution with degree of freedom n-p

### Code:
(phihat <- sum(residuals(model,type="pearson")^2)/(n-p))
