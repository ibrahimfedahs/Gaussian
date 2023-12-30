# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. start the program.
2. 
3. 
4. end the program

## Program:
```
'''Program to solve a matrix using Gaussian elimination without partial pivoting.
Developed by: IBRAHIM FEDAH S
RegisterNumber: 23014264
'''
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
       a[i] [j]=float(input())
for i in range (n):
    if a[i][i]==0.0:
        sys.exit('DIvide by zero detected!')
    for j in range (i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range (n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end = ' ')
```

## Output:
![WhatsApp Image 2023-12-31 at 02 29 44_4c9435d7](https://github.com/ibrahimfedahs/Gaussian/assets/150319493/1761bc49-77c0-4815-bb9d-df63c2b89ef6)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

