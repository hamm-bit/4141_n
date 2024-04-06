# Making a simple imperative language

| Column1   | Column2    |
|--------------- | --------------- |
| loops   | Macro   |
| if   | for loop |
| condition   | objects |
| variable / memory   | types |
| I/O      | functions |
| assignment |  |
| expressions|  |

---

# Questions

### 1)
What is a regex?

A language that can be fitted in a DFA (very informal)

###### a)
$$(b^*ab^*a)^*b^*$$

###### b)
$$a^*b(a^*ba^*b^*)a^*$$

###### c)
union a) and b)

---

### 2)
###### c)
Union of two $\mathrm{\epsilon-NFA}$, joins the terminating state of the first NFA with the initial state of the second one with the $\epsilon$ transition.

Subset construction for $\mathrm{\epsilon-NFA}$ differs from regular NFA by all states connected by epsilon transitions are merged together.

Check photos for final answer.

---

### 3)


--- 

### 4)

#### Pumping Lemma
If $L \subseteq \Sigma^*$ is regular and $\exists p \in \mathbb{N}$ (pumping length) where if $w \in L$ with $|w| \geq p$, then $w$ may be split into substrings $x, y, z$ s.t.
* $|xy| \leq p$
* $|y| > 0$
* $xy^iz \in L , \, \forall i \in \mathbb{N}$

