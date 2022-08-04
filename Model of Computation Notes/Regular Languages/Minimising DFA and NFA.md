# Steps:
### Minimising DFA
Algorithm is
• Reverse the NFA/DFA 
• Run the subset construction method on this new machine to determinise it 
• Reverse again 
• Run the subset construction method on it again

### Reversing the [[NFA]]/[[DFA]] (Step 1 above)
1) If NFA has multiple accept states, make a NEW accept state, and connect it via epsilon transitions from each old accept state, then make the original accept states non-accepting.
2) Reverse all transitions (flip the arrows), start state becomes accept and accept becomes start
3) Any accept state becomes a new start state (only 1 accept state if followed step 1, but can allow for many start states), and previous start state arrow is removed.