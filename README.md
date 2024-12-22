## Aim:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. Input and Initialization - Read number of equations and initialize arrays 
2. Forward Elimination (Gaussian Elimination) - Eliminate coefficients below diagonal using row operations
3. Back Substitution - Calculate solutions from last row to first row.
4. Print the Solutions - Print solutions in the format X%d = %0.2f.

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: Akbar
RegisterNumber: 24900203
'''
import numpy as np
n=int(input())
matrix=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        matrix[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=matrix[j][i]/matrix[i][i]
        for k in range(n+1):
            matrix[j][k]=matrix[j][k]-ratio*matrix[i][k]
#back substitution
x[n-1]=matrix[n-1][n]/matrix[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=matrix[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-matrix[i][j]*x[j]
    x[i]=x[i]/matrix[i][i]
for i in range (n):
    print ("X%d = %0.2f" %(i,x[i]),end=" ")
```

## Output:

![Screenshot (28)](https://github.com/user-attachments/assets/37460d83-f009-4495-bcc0-a80d63ef50c1)





## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

