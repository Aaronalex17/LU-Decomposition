# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
(i) To find the L and U matrix
```
'''Program to find L and U matrix using LU decomposition.
Developed by: 
RegisterNumber: 
'''

import numpy as np
from scipy.linalg import lu
A = np.array(eval(input()))
P,L,U=lu(A)
print(L)
print(U)

(ii)
import numpy as np
from scipy.linalg import lu_factor,lu_solve
A = np.array(eval(input()))
b = np.array(eval(input()))
lu,piv=lu_factor(A)
X=lu_solve((lu,piv),b)
print(X)
```
## Output:
![Screenshot (46)](https://github.com/user-attachments/assets/bb197495-22e6-41e4-9e21-464ad39441f0)
![Screenshot (47)](https://github.com/user-attachments/assets/303a8689-0f6a-4dd7-a51f-b14abedff357)




## Result:
Thus the program to find the LU Decomposition of a matrix is written and verified using python programming.

