# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the numpy module to use the built-in functions for calculation.

2.Prepare the lists from each linear equations and assign in np.array().

3.Using the scipy.linalg and imort lu_fator and lu_solve we get the values.

4.End the program

## Program:
```
/*
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: singamala venkata sai kumar reddy
RegisterNumber:23004205 
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]), end= ' ')
*/
```

## Output:
![maths2222](https://github.com/23004205/Gaussian/assets/138971114/0ad6e64f-7496-4e82-a25e-fc922f931326)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

