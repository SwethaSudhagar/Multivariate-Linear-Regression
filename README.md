 Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import the required libraries such as Numpy and scikit-learn.

### Step2
Load the dataset and separate the input features (X) and output variable (Y).
### Step3
Split the dataset into training and testing data.

### Step4
Train the Multivariate Linear Regression model using the training data.

### Step5
Predict the output using the testing data and display the predicted results.

## Program:
```
 Dataset Setup - Run this cell before starting the experiment

 import pandas as pd

 url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

 df = pd.read_csv(url)
 df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")
Developed by: Swetha S
Register number: 26012309

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
#Developed by: Swetha S
#Register number: 26012309

Coefficients: [0.00755095 0.00780526]
Intercept: 79.69471929115939
Predicted CO2 for the corresponding weight and volume: [114.75968007]







```
## Output:
<img width="935" height="778" alt="image" src="https://github.com/user-attachments/assets/6331ac4c-956a-4209-9d48-31137b06414d" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
