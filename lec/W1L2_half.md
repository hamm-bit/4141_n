# W1L2 - DFA and NFA, 02/16/2024

### Non-determinism

In a DFA, from each state
- Each input symbol leads to exactly one next state, and therefore
- Each input string leads to a unique state

In a NFA,
- There can be several possible next states for each input symbol (or none), and
- an input string can end at non-terminal state

Essence of non-determinism
- Multiple alternative computations (often hige numbers of them)
- Success if any succeeded
Different perspectives on the flavour of non-determinism
- Massive parallel search
- Search with "backtracking"
- Miraculously guessing the right option at each step.
- This is also known as the angelic non-determinism in the literature

### NFA vs DFA
An NFA is no more powerful than a DFA (though sometimes it can be a lot smaller)
With other kinds of automata, the non-deterministivc versions are sometimes more powerful than the deterministic ones.

### Subset Construction
The DFA produced by subset construction tracks the set of states that NFA can possibly be in (given the string)
The reason behind construction as the follows,
... Suppose the original automata was in one of the states in the set $${q_0, q_1}$$, and we received a `0`...

Given an NFA $$N = (Q, \Epsilon, q_0, \deta_N, F_N)$$ construct a DFA
    $$D = (2^Q, \Epsilon, {q_0}, \deta_D, F_D)$$
such that $$L(D) = L(N)$$
The key is in the definition of $$\deta_D$$ and $$F_D$$
    $$\deta_D(S,a) = \Cup_{q\in S} \delta_N(q, a), \, \text{for each} \, S \subset Q
The final states of $$D$$ are subsets that contain at least one final states of $$N$$.


### Proof (by induction)
(B case)
Trivial, omitted

(I case)

$$\hat{\delta}_D(S, aw) = \hat{\delta}($$\text{assuming} = \hat{\delta}(\delta(S, a), w)$$
$$ &= \Cup_{q' \in \delta(S, a)} \mathrm{Last}(q', m) (\Epsilon)



