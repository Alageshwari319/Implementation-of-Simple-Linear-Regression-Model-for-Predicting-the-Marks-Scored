# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Start the program and input the dataset containing hours studied (independent variable) and marks scored (dependent variable).
2.Create and train the Simple Linear Regression model using the given dataset. 
3. Predict the marks for the given number of study hours using the trained model.
4. Display the predicted result and plot the regression line along with the actual data points.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: 
RegisterNumber:  
*/
```

```
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression
X = np.array([1, 2, 3, 4, 5, 6, 7, 8]).reshape(-1, 1)
Y = np.array([35, 40, 50, 55, 65, 70, 75, 85])
model = LinearRegression()
model.fit(X, Y)
hours = np.array([9]).reshape(-1, 1)
predicted_marks = model.predict(hours)
print("Predicted marks for 9 hours of study:", predicted_marks[0])
Y_pred = model.predict(X)

plt.scatter(X, Y, label="Actual Marks")
plt.plot(X, Y_pred, label="Regression Line")
plt.xlabel("Hours Studied")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression - Marks Prediction")
plt.legend()
plt.show()
```

## Output:

<img width="804" height="648" alt="image" src="https://github.com/user-attachments/assets/14cf815e-b03f-48c0-9c74-7ea8f603f52a" />



## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
