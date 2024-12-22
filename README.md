# LU Decomposition 

## AIM:
To write a program to find the LU Decomposition of a matrix.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Start with the Matrix:
Let 
𝐴
A be a square matrix of size 
𝑛
×
𝑛
n×n.
Initialize two matrices: 
𝐿
L (lower triangular matrix) and 
𝑈
U (upper triangular matrix).
𝐿
L starts as the identity matrix (ones on the diagonal, zeros elsewhere).
𝑈
U starts as a copy of the matrix 
𝐴
A.
2. Perform Gaussian Elimination:
For each column 
𝑘
k from 1 to 
𝑛
n:
For rows below the pivot (i.e., 
𝑖
>
𝑘
i>k):

Calculate the multiplier 
𝑚
𝑖
𝑘
=
𝐴
𝑖
𝑘
𝐴
𝑘
𝑘
m 
ik
​
 = 
A 
kk
​
 
A 
ik
​
 
​
  (this is the element of 
𝐿
L).
Update the rows in 
𝑈
U to zero out the entries below the pivot in column 
𝑘
k by subtracting 
𝑚
𝑖
𝑘
×
m 
ik
​
 × the pivot row from row 
𝑖
i.
Store the multiplier 
𝑚
𝑖
𝑘
m 
ik
​
  in 
𝐿
L at the position 
𝐿
𝑖
𝑘
L 
ik
​
 .
This process makes the matrix 
𝐴
A become the upper triangular matrix 
𝑈
U, and 
𝐿
L is gradually populated with the appropriate multipliers.

3. Update the Matrix 
𝑈
U:
After the Gaussian elimination step, the matrix 
𝐴
A is transformed into an upper triangular matrix 
𝑈
U (with non-zero elements above the diagonal and zeros below the diagonal).
4. Construct the Matrix 
𝐿
L:
After the elimination steps, the matrix 
𝐿
L contains the multipliers used in the row elimination process.
The diagonal elements of 
𝐿
L are set to 1 (since the diagonal of 
𝐿
L is 1 in LU decomposition).
5. Return the Matrices 
𝐿
L and 
𝑈
U:
After completing the elimination, the matrices 
𝐿
L and 
𝑈
U represent the LU decomposition of 
𝐴
A.
The final output is the pair 
𝐿
L and 
𝑈
U, such that 
𝐴
=
𝐿
𝑈
A=LU.



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

