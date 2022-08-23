### Overview
- There are multiple different statistics that can be used to analyse a model, these can be use for visualization. 

### Residuals
- [[Response Residuals]]
- [[Pearson Residuals]]
- [[Deviance Residuals]]

- For linear models, **patterns in the residuals** indicate structure in the **data that has not been captured by the model**
- We can plot the residuals against predictor variables, the responses, or the fitted means. Often a plot against $\hat{\eta}_i = x^T_i\hat{\beta}$ works well.
- With **count** data residual plots exhibit banding due to the discrete nature of the responses, and this can make it hard to see other patterns. In this case we can use a smotthed fit of the residuals to help spot trends/patterns.
- ye

[[Leverage]]
[[Studentised Residuals]]
[[Jack-knife Residuals]]
[[Cook's Distance]]

