# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. First we want to import the numpy then import sys,and import the variable
2. For gaussian elimination we want to make 2nd and 3rd column zero
3. For that we want to make a range according to our program output
4. Then pin the program with correct form the the output will display 
5. End the program

## Program:
# Program to solve a matrix using Gaussian elimination without partial pivoting.
# Developed by: THARUN D
# RegisterNumber: 23013993 
~~~
import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i] == 0.0:
        sys.exist('Divide by zero detected!')
    
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        
        for k in range(n+1):
            a[j][k]=a[j][k]- ratio*a[i][k]
x[n-1] = a[n-1][n]/a[n-1][n-1]

for i in range(n-2,-1,-1):
    x[i]=a[i][n]
    
    for j in range(i+1,n):
        x[i]=x[i] - a[i][j]*x[j]
        
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f' %(i,x[i]),end=' ')
~~~

## Output:
![Screenshot 2024-01-01 120040](https://github.com/THARUNDT/Gaussian/assets/144871537/d63027aa-02d9-45ab-99f6-1fb2c7d43a03)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

