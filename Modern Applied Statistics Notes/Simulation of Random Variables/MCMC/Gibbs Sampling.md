### Overview:
- Used to simulate data from a joint bivariate distribution
- It  is difficult to simulate data from a distribution $f(x,y)$
	- However, it is easy to simulate from the conditional distribution of $f(x|y)$ and $f(y|x)$



### Procedure
1. Start at  some $x^0,y^0$
2. Sample $x^1$ from $f(x^0|y^0)$
3. Sample $y^1$ from $f(x^1|y^0)$
4. Repeat step 2 - 3

