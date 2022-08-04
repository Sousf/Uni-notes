---
aliases: [TM]
---
# Definition
A Turing machine (TM) is theoretical machine that forms the foundation of modern day computers, it is represented as tuple ($Q, \Sigma, \Gamma, \delta, q_0, q_a,q_r$) where
1) $Q$ is a finite set of states
2) $\Gamma$ is a finite *tape* alphabet, which includes the blank character 
3) $\Sigma$ is the input alphabet that does not include the blank character
4) $\delta$ is the transition steps
5) $q_o$ is the initial state
6) $q_a$ is the accept state
7) $q_r$ is the reject state, accept and reject state has to be different.

- TM operates on a tape which extends infinitely to the right
![[Pasted image 20211102172105.png]]

## [[TM Example]]

# Transition
![[Pasted image 20211102172240.png]]

# [[Non Deterministic TM]]

### Acceptance and Rejection, Halting
Let M be a TM
- M ***accepts*** a string $w$ if, starting in some configuration, it reaches the accept state after finitely many transaction.
- M ***rejects*** a string $w$ if, starting in some configuration, it reaches the reject state after finitely many transitions.
- M will only ***halt*** if M ***accepts*** or ***rejects***. M could potentially run forever.

### Turing Recognisable

- A [[Language]] $A$ is recognisable if it is a [[Language]] of some TM
	- Formally: Let M be a TM, $A$ is recognisable if L(M) = $A$
- This means that, this TM has to accept strings within $A$, for the other strings not in the [[Language]] it doesn't matter if the machine accept or reject or run forever.

### Turing Decidable

- A [[Language]] is decideable if there is a TM that accept all strings within this [[Language]], and reject all others.
- This means that this TM will always ***halt*** no matter what.
- M in this case is known as a ***decider***


### Relation between Recognisable and Decidable.
- Recognisability is more powerful than decidability because TM that are decidable ***is*** also recognisable
- Let M be a TM; M being decidable => M being recognisable

### [[Turing Universal]]

### [[Turing Closure]]
- [[Turing Closure#Decidable Language Closed Under Complement]]
- [[Turing Closure#Decidable Language Closed Under Union]]
- [[Turing Closure#Decidable Language Closed Under Intersection]]
- [[Turing Closure#Decidable Language Closed Under Concatenation]]
- [[Turing Closure#Decidable Language Closed Under Kleene Star]]

### [[Turing Decidable Problems]]
- [[Turing Decidable Problems#Acceptance of DFA and NFA]]
- [[Turing Decidable Problems#Acceptance of CFL]]
- [[Turing Decidable Problems#Acceptance of CFG]]
- [[Turing Decidable Problems#Emptiness of DFA]]
- [[Turing Decidable Problems#Emptiness of CFG]]

### [[Turing Undecidable Problems]]
- Overview:
	- ![[Pasted image 20211106155449.png]]
- [[Turing Undecidable Problems#Turing Accept Problem]]
- [[Turing Undecidable Problems#Turing Halting Problem]]
- [[Turing Undecidable Problems#Turing Emptiness Problem]]
- [[Turing Undecidable Problems#Turing Equivalence Problem]]

# [[Rice's Theorem]]