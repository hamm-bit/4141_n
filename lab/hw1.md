# Homework W1

### Question
Let $$\Sigma$$ be an alphabet, and let $$P(x)$$ be the proposition that:
$$\forall \ y \in \Epsilon^*, \vert x \cdot y \vert = \vert x \vert + \vert y \vert$$
Prove that $$P(x)$$ holds for all $$x \in \Sigma^*$$

### Walkthrough
We have a recursive definition of legnth of a string of grammar $$\Sigma$$.

$$
\text{Base}: \vert \epsilon \vert = 0
\text{a \cdot x} = 1 + \vert x \vert \, \forall a \in Sigma, \ x \in \Sigma^*
$$
Let $${x, y} \subseteq \Sigma^*$$,
So we can describe base case: 
For $$ x = \epsilon $$, $$ y = \epsilon $$,
$$\vert x \cdot y \vert$$
&= $$\vert \epsilon \cdot \epsilon \vert$$ \
&= $$\vert \epsilon \vert$$ \
&= $$ 0 $$

Secondary cases,
Let $$x \in \Sigma^*, y = a \in \Sigma$$,
$$\vert x \cdot y \vert$$
&= $$\vert x \cdot a \vert$$ \
&= $$\vert x \vert + 1$$ \
&= $$\vert x \vert + \vert a \vert$$.

Associativity is not proven, so secondary cases will also cover this
Let $$y \in \Sigma^*, x = a \in \Sigma$$,
$$\vert x \cdot y \vert$$
&= $$\vert a \cdot y \vert$$ \
&= $$1 + \vert y \vert$$ \
&= $$\vert a \vert + \vert y \vert$$.

Proof by structural induction.
