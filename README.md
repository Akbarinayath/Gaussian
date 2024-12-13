# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.step1.Input and Initialization - Read number of equations and initialize arrays 
2. step2.Forward Elimination (Gaussian Elimination) - Eliminate coefficients below diagonal using row operations
3.step3. Back Substitution - Calculate solutions from last row to first row.
4. step4.Print the Solutions - Print solutions in the format X%d = %0.2f.

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: 
RegisterNumber: 
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
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: 
RegisterNumber: 
*/
```

## Output:![Screenshot 2024-12-13 085922](https://github.com/user-attachments/assets/14f59028-f58e-43d1-bfaf-bab05a611dc0)

![gaussian elimination]()


## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

