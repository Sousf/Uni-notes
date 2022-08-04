# Proving Termination
Suppose that, for each loop in a program, we can find some "measure" (a function of the program variables) such that
1) The measure is a natural number, and
2) The measure gets smaller with each loop iteration


Then the program must terminate for all input, because a natural number cannot be made smaller indefinitely.

# Note 
The general problem of termination is **undecidable** [[Turing Machine#Turing Decidable]]