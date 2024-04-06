# Week 3 HW, pass tasks

### i)
**a)**

A straight forward (not merged) regex can be $$1^*(01^*01^*)^* \cup 0^*10^*10^*$$
The first case of the above regex was talked about in W3 tutorial. However I have moved residue $1$ from the back to the front, due to it being more analytically formal as it doesn't introduce conflicting limit points of the generated sequence.

**b)**

According to the formation of the DFA written for W2 tutorial, a possible regex can be written as
$$ 000^* | (001\cdot 0^*) | (010 \cdot 0^*) | (100\cdot 0^*)$$
This language is regular, since it is converted from the DFA before.


