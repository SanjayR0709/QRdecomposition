# Algorithm for QR Decomposition
## Aim:
To implement QR decomposition algorithm using the Gram-Schmidt method.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Intialize the matrix Q and u
2.	The vector u and e is given by

    ![eqn1](./ex4.jpg)

    ![eqn2](./ex6.jpg)

    ![eqn3](./ex3.jpg)

3.	Obtain the Q matrix   
    ![eqn4](./ex1.jpg)
4.	Construct the upper triangular matrix R
    ![eqn5](./ex2.jpg)



## Program:
### Gram-Schmidt Method

### import os
### os.environ["OPENBLAS_NUM_THREADS"]="1"

### import numpy as np
### def QR_Decomposition(A):
###     A = np.array(A, dtype=float)
###     n,m = A.shape
    
###     Q = np.zeros((n,m))
###     R = np.zeros((m,m))
    
###     for j in range(m):
###         u = A[:,j].astype(float)
        
###         for i in range(j):
###             R[i,j] = np.dot(Q[:,i], A[:,j])
###             u -= R[i,j] * Q[:,i]
        
###         R[j,j] = np.linalg.norm(u)
        
###         if R[j,j] < 1e-12:
###             raise ValueError("Columns are linearly dependent")
        
###         Q[:,j] = u / R[j,j]
        
###     print("The Q Matrix is")
###     print("", Q)
    
###     print("The R Matrix is")
###     print("", R)
    
### a = np.array(eval(input()), dtype=float)
### QR_Decomposition(a)








## Output

<img width="1277" height="742" alt="image" src="https://github.com/user-attachments/assets/8ecec710-a3c5-4818-b5f2-33581991215b" />



## Result
Thus the QR decomposition algorithm using the Gram-Schmidt process is written and verified the result.
