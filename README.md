# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:-

1.Get the independent variable X and dependent variable Y.

2.Calculate the mean of the X -values and the mean of the Y -values.

3.Find the slope m of the line of best fit using the formula.

4.Compute the y -intercept of the line by using the formula
 
5.Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.


## Program:
```
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: kathirvel.A
RegisterNumber:  212221230047
*/
import numpy as np
import matplotlib.pyplot as plt
#Preprocessing input data
X=np.array(eval(input()))
Y=np.array(eval(input()))

#Mean
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0

#To find sum of (xi-x') & (yi-y') & (xi-x')^2
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2

#To find slope
m=num/denom

#To find intercept
b=Y_mean-m*X_mean
print(m,b)

#To find predicted values
Y_pred=m*X+b
print(Y_pred)

#To plot the values
plt.scatter(X,Y)
plt.plot(X,Y_pred,color='red')
plt.show()
```

OUTPUT:-




![image](https://github.com/KathirvelAIDS/Find-the-best-fit-line-using-Least-Squares-Method/assets/94911373/f32e4830-bc0c-4404-a179-2a12d3c96424)






RESULT:-

Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
