# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
Program to implement univariate Linear Regression to fit a straight line using least squares.
```
Developed by: MADHAVAN V M
Register Number: 212225060144

import numpy as np
import matplotlib.pyplot as plt

#Preprocessing Input data

x=np.array([1,2,3,4,5])
y=np.array([2,4,5,4,5])

plt.scatter(x,y)
plt.show()
#Building the model
x_mean=np.mean(x)
y_mean=np.mean(y)

num=0
den=0
for i in range(len(x)):
    num+=(x[i]-x_mean)*(y[i]-y_mean)
    den+=(x[i]-x_mean)**2
m=num/den
c=y_mean-m*x_mean
print(m,c)
#Making predicitions
y_pred=m*x+c
print(y_pred)

plt.scatter(x,y) #actual
#plt.scatter(x,y_pred,color='red')
plt.plot([min(x),max(x)],[min(y_pred),max(y_pred)],color='red') #predicted
plt.show()
```

## Output:

<img width="391" height="545" alt="image" src="https://github.com/user-attachments/assets/15385080-0668-4102-857b-c0c84f99fce3" />

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
