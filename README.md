# SGD-Regressor-for-Multivariate-Linear-Regression

## AIM:
To write a program to predict the price of the house and number of occupants in the house with SGD regressor.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
/*
Program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor.
Developed by: Sashtitha K
RegisterNumber:  25008321 / 212225230253
import numpy as np
import matplotlib.pyplot as plt

from sklearn.datasets import fetch_california_housing
from sklearn.linear_model import SGDRegressor
from sklearn.multioutput import MultiOutputRegressor
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import mean_squared_error

data = fetch_california_housing()

X = data.data[:, :3]


Y = np.c_[data.target, data.data[:, 6]]

X_train, X_test, Y_train, Y_test = train_test_split(
    X, Y, test_size=0.2, random_state=42
)


scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)


model = MultiOutputRegressor(
    SGDRegressor(random_state=42, max_iter=2000, tol=1e-3)
)


model.fit(X_train, Y_train)


Y_pred = model.predict(X_test)


mse = mean_squared_error(Y_test, Y_pred)
print("Mean Squared Error:", mse)

print("\nSample Predictions (House Price, Population):")
print(Y_pred[:5])




plt.figure()
plt.scatter(Y_test[:, 0], Y_pred[:, 0])
plt.xlabel("Actual House Price")
plt.ylabel("Predicted House Price")
plt.title("Actual vs Predicted House Price")
plt.show()


plt.figure()
plt.scatter(Y_test[:, 1], Y_pred[:, 1])
plt.xlabel("Actual Population")
plt.ylabel("Predicted Population")
plt.title("Actual vs Predicted Population")
plt.show()
*/
*/
```

## Output:

<img width="1336" height="736" alt="image" src="https://github.com/user-attachments/assets/568f3798-8080-4c10-be2d-f83f95a0d73b" />

<img width="1211" height="568" alt="image" src="https://github.com/user-attachments/assets/b39fec1d-3a5d-4f0e-bb66-7b1cbfb4666a" />

## Result:
Thus the program to implement the multivariate linear regression model for predicting the price of the house and number of occupants in the house with SGD regressor is written and verified using python programming.
