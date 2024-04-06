# week 2 HD tutor

___

### 2b) recap

To constract no more than one '1', at least two '0'.

This string could be summarized by ${0^n.1.0^m}$.
The DFA solution bases on the number of zeroes from the beginning of string.

Hence the DFA have 3 main cases
    - no '0's before '1'
    - exactly one '0' before '1'
    - at least two '0' before '1', including no '1' (infinite '0')s

Hence we can construct an inductive proof as follows,

___

### Prove
There has to be 3 cases
- Let $f$ denote the depth of the '1'-erecting state from entry.
    - If $f(w) = 1$       iff no 0s
    - If $f(w) = 2$       iff exactly one 0s
    - If $f(w) = 3$       iff at least two 0s, including infinity
    
- Base case: $w = \epsilon$
    - $f(w)$ = 1, stayed at first node with depth 1. Hence this case is true

- Inductive case: 
    - Assume true for some $x \in \Epsilon^*$
    - Prove for $xa \in \Epsilon$ 
    - Case now splits:
        
        - Case 1: $f(x) = 1$, no '0's before '1'.
        - DFA moves takes the bottom most path from starting state
        - The distance to the accepting state is 2
        - The path to accepting state comprises only of 0
        - $a := 0$ from here on since $xa$ already comprise of one '1'
        - $f(xa)$ remains 1.
        - hence $xa \in \Epsilon^*$.
        ___
        - Case 2: $f(x) = 2$, exactly one '0' before '1'.
        - DFA moves takes the upper path to '0', then takes '1'
        - The distance to the accepting state is 1
        - Similarly to Case 1 here,
        - The path to accepting state comprises only of 0
        - $a := 0$ from here on since $xa$ already comprise of one '1'
        - $f(xa)$ remains 2.
        - hence $xa \in \Epsilon^*$.
        ___
        - Case 3: $f(x) = 3$, at least two '0's before '1'.
        - DFA moves takes the bottom most path from starting state
        - The distance to the accepting state is 0, not including loops
        - the path to accepting state can take either 0 or 1.
        - $a \in {0, 1}$ since $xa$ has not hit the limit of one '1', 
        - $f(xa)$ remains 3
        - hence $xa \in \Epsilon^*$.

- Hence by structural induction, the DFA constructed for 2 b) is correct. QED
