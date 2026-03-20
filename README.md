# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Start and import the required libraries — pandas for data handling and linear_model from sklearn for regression.

### Step2
Load the dataset from the CSV file using pd.read_csv() and store it in a DataFrame df.

### Step3
Select features and target:
Set X = [['Weight', 'Volume']] (independent variables).
Set y = ['CO2'] (dependent variable).

### Step4
Create a Linear Regression model using linear_model.LinearRegression() and store it in regr.

### Step5
Train the model using regr.fit(X, y) and display the model’s coefficients and intercept.

### Step6
Predict CO2 value for a given weight and volume using regr.predict() and print the predicted result.

## Program:
```Python
'''Developed by: Aditya Jorim F S
RegisterNumber: 212225240004
'''
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("cars.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:
<img width="1340" height="646" alt="Screenshot 2026-03-20 164612" src="https://github.com/user-attachments/assets/9b009221-4b07-45bd-946c-493a44a3fcbd" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
