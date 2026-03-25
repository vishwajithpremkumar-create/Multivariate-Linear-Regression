# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>
import pandas as pd
### Step2
<br>
Read the csv file
### Step3
<br>
Get the value of X and y variables
### Step4
<br>
Create the linear regression model and fit.
### Step5
<br>
Predict the CO2 emission of a car where the weight is 2300kg, and the volume is 1300cm cube
## Program:

```

import numpy as np

# Example data
Weight = np.array([790, 1160, 929, 865, 1140])
Volume = np.array([1000, 1200, 900, 1100, 1300])
CO2 = np.array([99, 95, 90, 97, 96])

# Simple linear regression using least squares (basic idea)
X = np.column_stack((Weight, Volume))
X = np.c_[np.ones(X.shape[0]), X]  # add intercept

# Compute coefficients using normal equation
beta = np.linalg.inv(X.T @ X) @ X.T @ CO2

print("Coefficients:", beta[1:])
print("Intercept:", beta[0])

# Prediction
new = np.array([1, 3300, 1300])
pred = new @ beta

print("Predicted CO2:", pred)




```
## Output:
<img width="684" height="65" alt="Screenshot 2026-03-25 191854" src="https://github.com/user-attachments/assets/79c74b0a-c417-441c-b501-be04e3f06826" />

### Insert your output

<br>
<img width="762" height="609" alt="Screenshot 2026-03-25 194231" src="https://github.com/user-attachments/assets/3045207d-4e3b-4e7b-9860-9733fefbc6d4" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
