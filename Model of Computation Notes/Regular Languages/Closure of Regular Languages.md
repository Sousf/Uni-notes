# Regular Languages are Closed Under Union and Intersection

- This is proved using [[Product Construction of DFA and PDA|Product DFA]]
- [[Product Construction of DFA and PDA#Product Construction Can Be Used To Construct Union and Intersection DFA]]

**Alternatively for Union Only We Can Also Show:**

Let A and B be [[Regular Languages]], with [[DFA]]s M<sub>A</sub> and M<sub>B</sub> as recognisers. Together the two [[DFA]]s make up an [[NFA]] which recognises A $\cup$ B.
![[Union of 2 DFAs visual.png]]

The $\epsilon$ transitions go to the start states of M<sub>A</sub> and M<sub>B</sub>. Note that the resulting [[NFA]] has two initial states.



# Regular Languages are Closed Under Concatenation

Let A and B be [[Regular Languages]], with the below DFAs as recognisers:
![[Concatenation of Regular Language.png]]

From these we can easily construct an [[NFA]] that recognises A $\cdot$ B
![[Concatenation_regular_visual.png]]


# Regular Languages are Closed Under Kleene Star

Let A be a regular [[Language]] with the [[DFA]] shown below as a recogniser
![[Kleene star regular.png]]


Here is how we construct an [[NFA]] to recognise A*
![[Kleene star regular construction.png]]


# Regular Languages are Closed Under Complement

# Regular Languages are Closed Under Complement
- We can construct a [[Complement DFA]]


# How To Prove?
Given any [[regular languages]] A,B, with NFAs D<sub>A</sub>,D<sub>B</sub>, construct

- Construct an [[NFA]] which recognises any of the operations on D<sub>A</sub> and D<sub>B</sub>
