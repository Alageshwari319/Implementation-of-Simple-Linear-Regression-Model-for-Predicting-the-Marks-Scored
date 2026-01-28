# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Read the dataset containing study hours (independent variable) and marks scored (dependent variable).
2. Calculate the mean of study hours and marks, then compute the slope (m) and intercept (b) of the regression line. 
3. Predict the marks using the simple linear regression equation:
         Y=mX+b
4. Display the predicted marks and plot the regression line along with the given data points.

## Program:
```
/*
Program to implement the simple linear regression model for predicting the marks scored.
Developed by: ALAGESHWARI V
RegisterNumber:  212224240010
*/
```

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
data = pd.read_csv("student_scores.csv")
X = data['Hours'].values
Y = data['Scores'].values
X_mean = np.mean(X)
Y_mean = np.mean(Y)
num = 0
den = 0
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2

m = num / den
b = Y_mean - (m * X_mean)
Y_pred = m * X + b

print("Slope (m):", m)
print("Intercept (b):", b)
hours = float(input("Enter number of study hours: "))
predicted_marks = m * hours + b
print("Predicted Marks:", predicted_marks)
plt.scatter(X, Y)
plt.plot(X, Y_pred)
plt.xlabel("Study Hours")
plt.ylabel("Marks Scored")
plt.title("Simple Linear Regression – Marks Prediction")
plt.show()
```

## Output:

<img width="927" height="855" alt="image" src="https://github.com/user-attachments/assets/1fdb5bb0-6ea0-4ad0-acf9-a147bddaae43" />




## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
