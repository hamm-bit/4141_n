=========================================
Welcome to COMP4141 Theory of computation

### The lecture was attended from break, first half of lecture is omitted

Course timeline:
- Introduction, set theory, finite automata
- Regular language
- Context-free language and Pushdown automata
- Recursively enumerable language and Turing machine
- Decidability and reductions
- W6
- Time and space complexity: P and NP
- NP-completeness
- ...


=========================================

### Set Theory

A simple callback:

union, intersection, empty set etc..

### Representing set

- discussion: an example of a small, finite set
- i.e.
    - Simple q:     Is $$x \in S$$:
    - Others:       Is $$S = \empty? Is S \cap T = \nullzero$$? etc

- what about an infinite set?
    - Same simple q: Is $$x \in S$$?

- The question:
    - Can all sets be represented in a computer storage (finite)
    - NO
        - uncountably infinite set (recall countable infinity)


### Another view of formal langauge theory

- A language can be abstracticzed as a Boolean function. {Property / Predicate}

- Basis for tools and programming techniques:
    - Lexical analysis
    - Parsing
    - Program analysis
- Many interesting problems in prog langs implementations are hard or impossible to solve
    - Equivalence of grammar
    - Almost any exact analysis


### Strings
    
    - Strings are informally a sequence of one of 128 characters.
    - Definition of a string over some alphabet $$\Sigma$$
        - Base: $$\epsilon$$ is a string over $$\Sigma$$
        - Induction: If x is a string over $$\Sigma$$ and $$a$$ is a symbol from $$\Sigma$$

    Show that for arbitrary strings x, y, z over $$\Sigma$$ concatenation is associative,
        \[
            x \cdot (y \cdot z) = (x \cdot y) \cdot z; \quad \text{associativity}
        \]
    
    > [!NOTE]
    > This is an example of **Sturctural Induction**
        Begin proof:
            - $$ \epsilon \in \Sigma $$
            - $$ Base case: x = \epsinlon $$
            - $$ \epsilon \cdot (y \cdot z) = (y \cdot z)$$
            - $$ = y \cdot z$$
            
            - $$ \text{let} x = a\omega$$
            - $$ a\omega \cdot (y \cdot z) = (y \cdot z)$$
            - $$ = y \cdot z$$
            - ...

### Sidenote: Proof expectations

We dont want to lose sight of the forest because of the tree.
Here are the "forest-level" points with proofs.
    - What is the proof strategy
        - Induction on strings. **Base and Induction**.
        - Induction on expressions. ...
        - Diagonalization
        - Reduction from another problem. **Direction of proof**.
    - What are the key insights?
    - Often this is a construction
        - Translation between regex, finite automatas
        - Translation from a problem to another.
Explain these things clearly in your proofs. 
If we can see quickly that you did the right kind of proof and got the major point right,
you may get nearly full marks.

### Languages
A language over $$\Sigma$$ is a subset of $$\Sigma^\star$$ (Recall what this operator mean).
    
