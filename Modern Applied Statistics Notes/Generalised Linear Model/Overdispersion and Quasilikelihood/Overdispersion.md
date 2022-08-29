### Overview
- Overdispersion describes the observation that variation is higher than would be expected


### Example with Poisson Regression
- For example, the _normal distribution_ does that through the parameter $\sigma$ (i.e. the standard deviation of the model), which is constant in a typical regression. In contrast, the _Poisson distribution_ has no such parameter, and in fact the variance increases with the mean (i.e. the variance and the mean have the same value)
- If the observed variation is much higher than the mean in the data, then the data is overdispersed.


### Solution 
- One way to deal with **Overdispersion** is [[Quasi-likelihood]]


### Checking for overdispersion
- [[Estimating phi]], if $\phi$ is much bigger than what it should be there is probably overdispersion
- To know what the value should be for $\phi$, check [[Exponential Family#Example]]
- ![[Pasted image 20220829184315.png]]

### Important note
- If you ignore overdispersion when fitting a binomial/poisson regression, your estimation is unaffected, but your inference changes.
- With proper modelling of overdispersion
	- Your F statistic is reduced, making model comparison less significant in general (so you may end up with fewer significant variables in the model).
	- Your estimate of Σ also increases, so you get larger CI for your parameter estimates.