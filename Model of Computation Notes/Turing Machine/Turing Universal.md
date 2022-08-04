### Definition
When we say [[Turing Machine|TM]] are ***universal***, we mean that all other notions of computation can be simulated by a [[Turing Machine|TM]], including TMs themselves.

### Alan Turing Proof
Alan Turing has a proof that given some method of encoding TMs as strings (possible since all TMs are finite), there is a [[Turing Machine]] UTM, such that, when run on a string encoding [[String Representation of TM]]
- If M accepts w, then UTM accepts
- If M rejects w, then UTM rejects
- If M does not halt on w, then UTM does not accept (can run forever)
- ***and UTM rejects all strings which are not in the right format of encoding [[String Representation of TM#<M,w>]]***

- We can see that UTM is a recogniser of this [[Language]], however, it is not a decider (Since it can run forever).