---
aliases: [CFG]
---

### Definition
Context Free Grammar are to [[Context Free Language]] as Regular Expressions are to [[Regular Languages]]. 
They describe a recipe for creating strings of the [[Language]].

Context Free Grammar are non-deterministic by nature

### Structure 
A Context Free Grammar (CFG) $G$ is a 4-tuple ($V,\Sigma,R,S$) where

1) $V$ is a finite set of variables,
2) $\Sigma$ is a finite set of terminals,
3) $R$ is a finite set of **rules**, each consisting of a variable and a string in ($V \cup \Sigma*$),
4) $S$ is the starting variable



## Example: Context Free Grammar $G$
$G$ := ({$S,A,B$},{0,1}, $R,S$)
S --> A | BAB
A --> 0A0 | $\epsilon$
B --> 1B | $\epsilon$



### Ambiguous CFG
- Context Free Grammar is ambiguous if there is a string in its [[Language]] that has 2 distinct parse trees.

### [[Context Free Language#Ambiguous CFL]]

### Empty Context Free Grammar
- A Context Free Grammar G will have its [[language]] L(G) = $\emptyset$ if it its rules ($R$) is empty, or if it doesnt contain any set of terminals ($\Sigma$), or if its rules ($R$) doesn't have a rule that resolve into a standalone terminal.

