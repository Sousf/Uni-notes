### Definition
- $r_p(i) = \frac{y_i - \hat{\mu}_i}{\sqrt{v(\hat{\mu}_i)}}$

- Pearson residuals are (approximately) homoskedastic, and $\Sigma_ir_p(i)^2 = X^2$
- where $X^2$ is Pearson's Chi-Squared.


**Code**:
- residuals(model, type = "pearson")