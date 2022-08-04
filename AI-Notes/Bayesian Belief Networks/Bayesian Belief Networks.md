## Overview:
- A simple, graphical notation for conditional independence assertions and hence for compact specification of full joint distributions.
- Bayesian network store probability distribution in the form of **Conditional Probability Table (CPT)** 



## Example 1: 
- Here is a graphical representation of Bayesian Network
![[Pasted image 20220518153522.png]]


## Example 2:
- Given the following scenario:
![[Pasted image 20220518153624.png]]
- A graphical representation with the CPT is as follow:
- ![[Pasted image 20220518153705.png]]


## Advantage of Bayesian Belief Networks
- A **Conditional Probability Table (CPT)** for a boolean X with $k$ boolean parents has $2^k$ rows for the combinations of parents values.
	- Example: **Alarm** from the above example has 2 parents, **Burglary** and **Earthquake**, **$k = 2$** in this case. Hence it has 4 rows as shown above.
	- Example: **JohnCalls** has 1 parent which is **Alarm**, hence it only have 2 rows since  **$k = 1$

- If each variable has no more than $k$ parents, then the complete network requires $O(n*2^k)$
	- This means that the number of rows grows linearly to **the number of variables (n)**
	- Whereas if we were to store a **full joint distribution** the number of rows would be $O(2^n)$ which is alot bigger




![[Pasted image 20220603145837.png]]

