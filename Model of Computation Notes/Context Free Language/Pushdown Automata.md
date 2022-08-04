---
aliases: [PDA]
---

### Definition
- A pushdown automaton (PDA) can be use to recognise [[Context Free Language]], it is what [[DFA]] and [[NFA]] are to [[Regular Languages]].
- A pushdown automaton (PDA) is a 6-tuple ($Q, \Sigma, \gamma, \delta, q_o, F$)
1) $Q$ is a finite set of state
2) $\Sigma$ is the finite input alphabet
3) $\Gamma$ is the finite stack alphabet
4) $\delta$ is the transition function
5) $q_0$ $\epsilon$ $Q$ is the *start state*
6) $F$ $\subseteq$ $Q$ are the *accept states*

- A PDA also require a stack structure to track the current string. The stack is initialised empty.
- A PDA is more capable than [[DFA]] and [[NFA]] but are less capable than Turing Machines


### Example PDA
![[Pasted image 20211102153035.png]]


### Sequence of Operation
A PDA has 1 operation step as follow

***a, b --> c***
- **a** = what we see on the input string currently
- **b** = what we see ontop of the stack currently
- **c** = what we are going to replace the b with inside the stack.
**After replacing b with c we transition to the next state**




### [[Progressive PDA]]
### [[Deterministic PDA]]