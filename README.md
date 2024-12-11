# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas module import linear_model from sklearn
### Step2
read the csv file (saved in the same directory) using pd.read_csv
### Step3
prepare regression using linear_model.linearRegression() and assign it to the identifier"regr".
### Step4
The coefficient can be obtained by regr.coef_and the intercept can be obtained byregr.intercept_. The predicted result can be obtained by regr.predict().
### Step5
print the predicted output from the code.
## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
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
![exp 10](https://github.com/user-attachments/assets/08855767-4151-44c7-9982-9f7bbe4932e3)
## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
