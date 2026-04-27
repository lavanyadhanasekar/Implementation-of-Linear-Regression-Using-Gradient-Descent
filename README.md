# Implementation-of-Linear-Regression-Using-Gradient-Descent

## AIM:
To write a program to predict the profit of a city using the linear regression model with gradient descent.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import required libraries
2.Initialize dataset (e.g., population vs profit)
3.Initialize parameters: slope m and intercept b
4.Choose learning rate α and number of iterations
5.For each iteration:
6.Predict values:
	​y=mx+b
7.Compute error
8.Update parameters using gradient descent
9.Repeat until convergence
10.Plot the regression line 


## Program:
```
/*
Program to implement the linear regression using gradient descent.
Developed by: 
RegisterNumber:  
*/

# Program to implement Linear Regression using Gradient Descent
# Developed by:
# Register Number:

import numpy as np
import matplotlib.pyplot as plt

# Sample dataset (Population vs Profit)
X = np.array([1, 2, 3, 4, 5], dtype=float)
Y = np.array([2, 4, 5, 4, 6], dtype=float)


m = 0
b = 0


learning_rate = 0.01
iterations = 1000
n = len(X)

for i in range(iterations):
    Y_pred = m * X + b
    
    
    dm = (1/n) * np.sum((Y_pred - Y) * X)
    db = (1/n) * np.sum(Y_pred - Y)
    
    
    m = m - learning_rate * dm
    b = b - learning_rate * db


print("Slope (m):", m)
print("Intercept (b):", b)


Y_pred = m * X + b

plt.scatter(X, Y, color='blue', label='Actual Data')
plt.plot(X, Y_pred, color='red', label='Regression Line')
plt.xlabel("Population")
plt.ylabel("Profit")
plt.title("Linear Regression using Gradient Descent")
plt.legend()
plt.show()
```

## Output:
<img width="746" height="614" alt="image" src="https://github.com/user-attachments/assets/a347aaef-fece-45dd-94b9-314d2a8d8ccf" />



## Result:
Thus the program to implement the linear regression using gradient descent is written and verified using python programming.
