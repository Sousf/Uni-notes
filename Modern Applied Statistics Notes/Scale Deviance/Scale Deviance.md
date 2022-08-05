### Overview

- this statistic measures how much a current fitted model **deviates** from a 'perfect' model on the dataset.
- Use to measure model goodness
- The 'perfect model' is known as the saturated model.
- Formally, **scale deviance is defined as the difference between the log-likelihood of the fitted model and the saturated model on a given dataset**.
	- $D=-2[l(\hat{\beta})-l_s]$
	- where $l(\hat{\beta})$ is the log-likelihood of fitted model
	- $l_s$ is the log-likelihood of the saturated model.
	- $l_s$ is always bigger than $l(\hat{\beta})$
- the _deviance is always larger or equal than zero_, being zero only if the fit of the model is perfect.

### The Saturated model
- This is the name for a theoretical model that perfectly fit the data at hand
- Theoretically, the saturated model will have the same number of parameters as the number of instances in the dataset, where there is a parameter for each data point


**An Example of saturated, fitted, and null model**
![[Pasted image 20220805143408.png]]


### Distribution of Scale Deviance
- follows a $\chi^2$ Distribution with d.o.f n - k 
	- where k is the parameters of the fitted model
	- this is because the saturated model will have n parameters, hence the d.o.f will just be the difference between the 2.
- 

### Testing model goodness 
- We know that scale deviance follow a Chi2 distribution with degree of freedom k.
	- where k is the difference in df of the loglikelihood of scale model and the fitted model
- If we see that the p-value is bigger than 0.05, "probabilistically reasonable to occur", then we say the model is adequate.
- else if it is smaller than 0.05, then we say it is not adequate.


### Scale Deviance for model selection
- Assume we have 2 models A,B
- If A is nested within B
- If A has deviance $D_A$ and B has deviance $D_B$
- Then:
	- $D_A - D_B=-2[logl(\hat{\Theta}_A) - logl(\hat{\Theta}_B)]$
	- where $logl(\hat{\Theta}_A)$ and $logl(\hat{\Theta}_B)$ is log-likelihood of A and B respectively
	- That is, the log likelihood for the saturated model cancels, and we are left with the [[log-likelihood ratio]]
