# Gaussian Elimination

## AIM:
To write a program to find the solution of a matrix using Gaussian Elimination.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```python

Developed by: Abdul Kadher S
RegisterNumber: 212225230002

import numpy as np
import sys
n=int(input())
a=np.zeros((n,n+1))
x=np.zeros(n)
for i in range(n):
    for j in range(n+1):
        a[i][j]=float(input())
for i in range(n):
    if a[i][i]==0.0:
        sys.exit('Divide by zero detected!')
    for j in range(i+1,n):
        ratio=a[j][i]/a[i][i]
        for k in range(n+1):
            a[j][k]=a[j][k]-ratio*a[i][k]
x[n-1]=a[n-1][n]/a[n-1][n-1]
for i in range(n-1,-1,-1):
    x[i]=a[i][n]
    for j in range(i+1,n):
        x[i]=x[i]-a[i][j]*x[j]
    x[i]=x[i]/a[i][i]
for i in range(n):
    print('X%d = %0.2f'%(i,x[i]),end=' ')

```

## Output:
<img width="1189" height="660" alt="AdobeExpressPhotos_86e39cfdf231483183652372db9a5e6d_CopyEdited" src="https://github.com/user-attachments/assets/1708de40-f6e1-4690-8892-fc692e32d686" />
<img width="1218" height="484" alt="AdobeExpressPhotos_3f4243cfc8244a9ab0f1258e350bb80b_CopyEdited" src="https://github.com/user-attachments/assets/5dc1c1cf-8b0b-4b91-9eaf-8b225cccddd6" />



## Result:
Thus the program to find the solution of a matrix using Gaussian Elimination is written and verified using python programming.

