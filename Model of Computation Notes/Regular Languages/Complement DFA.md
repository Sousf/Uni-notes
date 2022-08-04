### The Complement Trick
- Given a [[DFA]] or [[NFA]] $D_1$  for a [[Language]], how do we find the [[DFA]] ($D_2$) for its complement $D^c$?
	- Simply turn every accept state in $D_1$ into a non accepting state, and turn every non accepting state in $D_1$ into an accept state; this new [[DFA]] is $D_2$

### Note:
If there is an accept state that is also a start state for a DFA, it would stay the same as an accept and start state when you reverse.