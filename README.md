# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Read the order of the matrix and input the augmented matrix coefficients.

2.Perform Gaussian elimination row operations to convert the matrix into upper triangular form.

3.Apply backward substitution to compute the values of unknown variables.

4.Print the obtained solutions of the system of equations.

## Program:
```
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: Devadhaarini.R
RegisterNumber: 212225040061.
*/
import numpy as np
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
    print('X%d = %0.2f '%(i,x[i]),end='')
```

## Output:
<img width="1920" height="1080" alt="Screenshot (156)" src="https://github.com/user-attachments/assets/29fc3236-1482-4db1-8a67-94c5c3a375cf" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

