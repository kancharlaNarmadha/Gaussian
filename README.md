# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm

    1.Import the numpy module to use the built in function for calculation.
    
    2.Import the sys function. Get input from the user for the matrix i and j using for loop.
    
    3.Check wheather the matrix of element is divisible by zero. If divisible by zero then print zero is detected. And further find the ratio of the matrix.
    
    4.End the program.


## Program:
/*
Program to find the solution of a matrix using Gaussian Elimination.
Developed by: KANCHARLA NARMADHA
RegisterNumber: 212222110016
*/
```
import numpy as np
n=int(input())
arr=np.zeros((n,n+1))
res=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        arr[i][j]=int(input())
for i in range(n):
    for j in range(i+1,n):
        ratio=arr[j][i]/arr[i][i]
        for k in range(n+1):
            arr[j][k]=arr[j][k]-ratio*arr[i][k]
res[n-1]=arr[n-1][n]/arr[n-1][n-1]
for i in range(n-2,-1,-1):
    res[i]=arr[i][n]
    for j in range(i+1,n):
        res[i]=res[i]-arr[i][j]*res[j]
    res[i]=res[i]/arr[i][i]
for i in range(n):
    print("X%d = %0.2f" %(i,res[i]),end=" ")

```

## Output:


![T OUTPUT 6](https://github.com/kancharlaNarmadha/Gaussian/assets/119559316/d7118f72-130d-438d-8e74-e5b9c8d33e7b)



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

