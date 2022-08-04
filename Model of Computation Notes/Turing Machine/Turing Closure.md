# Decidable Language Closed Under Complement

- If A is decidable, then $A^c$ is also decidable

***Proof:***
- To build a [[Turing Machine|TM]] for $A^c$, simply swap $q_a$(accept) and $q_r$(reject) the same process in [[Complement DFA]]
- We know that, since $Turing Machine_A$ is decidable and hence must always halt:
	- $TM_A$ reaches $q_a$ in finite time, TM<sub>A<sup>c</sup></sub> reaches $q_r$ in finite time.
	- And $TM_A$ reaches $q_r$ in finite time, TM<sub>A<sup>c</sup></sub> reaches $q_a$ in finite time.

- ***Hence*** both $TM_A$ and [[Turing Machine|TM]]<sub>A<sup>c</sup></sub> are deciders and ***hence*** Decidability is closed under Complement.


# Decidable Language Closed Under Union

If we have
- $D_1$ decides $L_1$
- $D_2$ decides $L_2$
is $L_1$ $\cup$ $L_2$ decidable?

***Proof:***
- Have a [[Turing Machine|TM]] that simulates the 2 TMs above on $L_1$ $\cup$ $L_2$
- Since the 2 TMs above are deciders, they run in finite time, and hence our new machine will also run in finite time.
- If at least 1 of the [[Turing Machine|TM]] above accept, then we accept, else we reject.
- We have just built a decider for $L_1$ $\cup$ $L_2$ and ***hence*** Decidability is closed under Union

# Decidable Language Closed Under Intersection

If A and B are decidable, then A $\cap$ B is also decidable

***Proof:***
- By *De Morgan's Law*:
	- A $\cap$ B = ($A^c$ $\cup$ $B^c$)<sup>c</sup>

- We know that [[Decidable Language Closed Under Complement|turing complement]] and [[Decidable Language Closed Under Union|turing union]] are closed under decidability, ***hence*** Intersection is closed under decidability

# Decidable Language Closed Under Concatenation

Let A be decided by $D_1$ and B be decided by $D_2$

Simulate a machine that runs on A $\cdot$ B
On input w:
1) Split w into 2 pieces in all possible ways
2) Run $D_1$, on first, run $D_2$ on second
3) If both accept, accepts. Otherwise Reject

- This [[Turing Machine|TM]] runs in finite time, and hence is a decider, ***hence*** closed under Concatenation.

# Decidable Language Closed Under Kleene Star

Let A be decided by $D_1$, is A* decidable?

Simulate the machine:
On input w:
1) Split w into any number of pieces in all possible ways (this is finite)
2) Run $D_1$ on all pieces
3) If all accept, accepts. Otherwise reject.

- This [[Turing Machine|TM]] runs in finite time, ***hence*** Kleene Star is closed under Decidability