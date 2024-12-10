# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import numpy as np and load the dataset 

### Step2
Compute the slope (m) and intercept (b) using the least square formula

### Step3
Use the equation and calculate the predicted values

### Step4
Plot the original data and the regression line for visualization

### Step5
End the program

## Program:
```
import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output:
![Screenshot (17)](https://github.com/user-attachments/assets/ed2588cf-0a39-466c-bdf7-b79a983967d7)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
