# Formal proof of DFA correctness

### Proof for Tut2 Q2 b)

Prove
    If f(V) = 1         iff has no 0s
    If f(w) = 2         exactly one 0s
    If f(w) = 3         two or more 0s

- Base case: $w = \epsilon$
    - $f(8) = 1$ and $\epsilon$ has no 0s.
    - Base case proved

- Inductive case:
    - Assume true for some $x \in Epsilon^*$
    - Prove for $xa \in Epsilon^*$ for $a \in Epsilon$
    - Case 1: $f(x) = 1$,
        - If $a = 0$, DFA moves to state 2.
        - Also, $x$ has no 0s by assumption.
        - So $xa$ has exactly one 0.
    - If $a = 1$, DFA stops at current state
    - $xa = x \cdot 1$ has empty no. 0s.

___

### Q2 d)
Union operation for b) and c)


