#UninformSearch 

## Overview
- This is Depth First Search but with depth limit. This algorithm iteratively increases the depth limit from 1 up in order to find the most optimal solution using Depth First Search
- By having a limit, we can negate some of the bad effects of sticking to one path at a time by Depth First and have some of the goodness of Breadth First Search.

## Example Steps:
![[Pasted image 20220310123345.png]]


![[Pasted image 20220310104057.png]]

## Time Complexity: O($b^d$)
- Basically same time complexity as [[Breadth First Search]]
- Even though we repeat visiting some nodes, most of the nodes are on the last level, and that is only visited once, and hence the repeated visits are marginally small compare to the number of nodes in last level, which has $b^d$ number of nodes.
- The complete Time Complexity is $(d+1)b^0 + db^1 + (d-1)b^2 + ... + b^d = O(b^d)$. 
## Space Complexity: O($bd$)
- Since the underlying search is [[Depth-first Search]], the space complexity will be the same. Except that the depth level will always be the same $d$ instead of having a maximum depth level $m$ since we are limiting the depth at every step. This is an advantage over [[Breadth First Search]]
## Optimal:
- Yes only when **b** is finite, it will always find the optimal solution because the depth limit will stop it from getting stuck into a very long path
- 

## Completeness: 
- Yes, it will be able to find the solution when there is one.



![[Pasted image 20220318165836.png]]