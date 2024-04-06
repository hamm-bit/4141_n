# Week 3 HW, credit tasks

### a)
From the DFA constructed for W2 Pass f) or Credit c), we can construct a regex which doesn't contain '011' as substring as
$$1^*(0^* | 1\cdot0)^*$$

### b)
After the resubmission of W2 Distinction tasks, the DFA is ready.

![image](/Users/ntatsu/Desktop/4141/4141_2/lab/autotut1/D_2a_DFA.png)
*DFA obtained for W2 D_2a*

The regex for this graph can be obtained by listing out states:

- $q_7 = \epsilon | q_61 | q_31 | q_71$
- $q_6 = q_70 | q_40$
- $q_5 = q_60 | q_50$
- $q_4 = q_51$
- $q_0 = q_41 | q_01 | q_11$
- $q_1 = q_30 | q_00$
- $q_2 = q_10 | q_20$
- $q_3 = q_21$

After collapsing states and solving simultaneously, we can obtain a final regex, in multiple rows
$$(1|01|000^*1(000*1)^*01|000^*1(000^*1)^*11^*0(11^*0)^*01^*1(0(11^*0)^*01^*1)^*1)^* \, \cdot$$ 
$$(\epsilon|0|000^*|000^*1(000^*1)^*(\epsilon|0|000^*))$$
