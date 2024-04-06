# Week 5

### Problem 4 b)

| Column1    | Column2    | Column3    | Column4    | Column5    |
| ---------------- | --------------- | --------------- | --------------- | --------------- |
| S         |           |           |           |
| $\varnothing$  | B         |           |           |
| S         | $\varnothing$  | C, B      |           |
| A         | B         | B         | A, C      |
| a         | b         | b         | c         |

> [!NOTE]
> Rules of CYK deduction:
> 
> - List out the word at the bottom row
> - For $w$ above an existing row, check that the word on the block lower and right-lower can be formed by conjoining the word.

# Quick recap

1. Regular languages
    1. DFA
        - Minimal states -> Myhill-Nerode
    2. NFA
    3. RegEx
    4. Non regular
        - Pumping Lemma (May not work at times)
        - Myhill-Nerode
2. Context-free
    1. CFG
    2. PDA
    3. Non-CF
        - Pumping Lemma for CF languages
    4. CNF + CYK algorithm for deciding $\omega \in L(G)$.
3. Turing Machine

### Example: Turing modelling
```vhdl
; Machine starts in state 0.

; State 0: read the leftmost symbol
0 _ _ * halt-accept
0 1 1 * halt-reject
0 0 _ r scan-to-end

scan-to-end 0 0 r scan-to-end
scan-to-end 1 1 r scan-to-end
scan-to-end _ _ r check-1

check-1 0 0 * halt-reject
check-1 1 _ 1 scan-to-left
check-1 _ _ * halt-reject

scan-to-left 0 0 1 scan-to-left
scan-to-left 1 1 1 scan-to-left
scan-to-left _ _ r 0

```
