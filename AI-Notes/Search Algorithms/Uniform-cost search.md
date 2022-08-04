#UninformSearch
## Overview
- Good resource: https://youtu.be/dRMvK76xQJI
- Also known as Cheapest First Search
- Traverse the graph and take the route that has the shortest total cost at each step until the destination is reached.
- Insert nodes into the queue in order of increasing path cost

![[Pasted image 20220310102016.png]]
![[Pasted image 20220310102054.png]]
choosing the next lowest path cost.


**Optimal:** Yes
**Complete:** Most of the time, except when there are negative path costs
**Time Complexity:** 