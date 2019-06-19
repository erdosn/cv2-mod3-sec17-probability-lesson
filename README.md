
### Questions
* Unclear on section 17
    * let's build on probability
* Wants to have questions, but unsure of what is going wrong. So unsure what to ask. 

### Objectives

### Outline


```python
import pandas as pd
import numpy as np

import matplotlib.pyplot as plt
```


```python
# Unions
A = {1, 2, 3}
B = {2, 3, 4}
C = {2, 4, 6, 8}
```


```python
A.union(B)
```




    {1, 2, 3, 4}



### what is A^c 
* Z+ -> positive integer
* Z+- A^c = Z+/{1, 2, 3}

### B intersection C^c
 = {3}

## Axiom of Probability
* $0 \leq Prob(E) \leq 1$ for any E in S
* If an event, E, is certain to happen then P(E) = 1
* $ S = \sum_1^n E_i$, where $E_i$ are independent/mutually exclusive/disjoint


* Prob(E1) & Prob(E2) & ... & Prob(Ek) = P(E1)* ... *P(Ek)

## Factorials
10! -> 10 * 9 * ... * 1 -> 10 ways of ordering 10 distinct items





```python
def factorial(n):
    if n == 0:
        return 1
    if n == 1:
        return 1
    return n*factorial(n - 1)
```


```python
factorial(20)
```




    2432902008176640000




```python
def combination(n,k):
    combin = factorial(n)/(factorial(n-k)*factorial(k))
    return combin
```


```python
first_team = combination(16,4)
second_team = combination(12,4)
third_team = combination(8,4)
fourth_team = combination(4,4)
```


```python
total_comb =(first_team *second_team *third_team*fourth_team) / factorial(4)
total_comb
```




    2627625.0




```python
factorial(16)/(factorial(4)**4 * factorial(4))
```




    2627625.0



### Probability the sum of 2 dice equals 8 given that at least one of the dice is greater than 4.



```python
# assume d2 > 4
d1 = list(range(1, 7))
d2 = [5, 6]

total = len(d1)*len(d2)
counts = 0
for face in d1:
    for face2 in d2:
        if face + face2 == 8:
            print(face, face2)
            counts += 1

counts/total
```

    2 6
    3 5





    0.16666666666666666



### Assessment


```python

```
