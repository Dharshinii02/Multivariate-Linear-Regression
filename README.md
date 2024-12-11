# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas as pd and read the CSV file containing data about car weight, volume and co2 into dataframe

### Step2
Select weight and volume as a input features(x) and co2 as target variable (y)

### Step3
Create a linear agression model linear_model.LinearRegression() and fit it to x and y
### Step4
Print the coefficients and intercepts of the trained regression model

### Step5
Use the trained model to predict co2 for given weight and volume and end the program by displaying the precited model
## Program:
```
import pandas as pd
from sklearn import linear_model
df = pd.read_csv(r"C:\Users\admin\Desktop\carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:',predictedCO2)
```
## Output:
![Screenshot 2024-12-11 091226](https://github.com/user-attachments/assets/bbd7c96d-9a25-4c15-b7e9-6835ef576b4e)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
