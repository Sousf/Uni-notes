# CFL Closed Under Union

- Let L1 and L2 be CFLs
- We can construct a Context Free Grammar for L1 $\cup$ L2
by doing this to the Starting state
S-->S1 | S2


# CFL Closed Under Concatenation
To make the CFG for L1$\cdot$L2 we simply make the Start state as below:
S-->S1S2


# CFL Closed Under Kleene Star
Let L1 be a CFL, The starting state of L1* would be
- S --> $\epsilon$ | S<sub>1</sub>S

This is to ensure that the starting state of L1* is anyone number of L1 concatenated together, only when S becomes $\epsilon$ can all the S<sub>1</sub> resolve into their set of terminals.

# CFL is NOT Closed Under Intersection HOWEVER...
- CFL $\cap$ CFL does not gurantee to also be a CFL
- CFL $\cap$ [[Regular Languages]] IS a CFL
