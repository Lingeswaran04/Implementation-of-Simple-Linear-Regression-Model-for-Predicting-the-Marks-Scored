# Implementation-of-Simple-Linear-Regression-Model-for-Predicting-the-Marks-Scored

## AIM:
To write a program to predict the marks scored by a student using the simple linear regression model.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Load Data: Import the data from student_scores.csv and separate it into hours studied (x) and scores (y).

2.Split Data: Divide the data into training and testing sets.

3.Train Model: Use linear regression to train a model on the training data.

4.Make Predictions: Predict the scores for the test data.

5.Evaluate & Visualize: Calculate error metrics (like MAE, MSE, RMSE) and plot graphs to compare actual vs. predicted scores for training and test data.

## Program:
### df.head():
```

Program to implement the simple linear regression model for predicting the marks scored.
Developed by: LINGESWARAN K
RegisterNumber:  212222110022
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt 
from sklearn.metrics import mean_absolute_error, mean_squared_error
df=pd.read_csv("student_scores.csv")
df.head()
```
### df.tail():
```
df.tail()
```
### ARRAY VALUE OF X:
```
#segregating data to variables
x=df.iloc[:,:-1].values
x
```
### ARRAY VALUE OF Y:
```
y=df.iloc[:,1].values
y
```
### VALUES OF Y PREDICTION:
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=1/3,random_state=0)
from sklearn.linear_model import LinearRegression
regressor=LinearRegression()
regressor.fit(x_train,y_train)
y_pred=regressor.predict(x_test)
y_pred
```
### ARRAY VALUES OF Y TEST:
```
y_test
```
### TRAINING SET GRAPH: 
```
plt.scatter(x_train,y_train,colour="orange")
plt.plot(x_train,regressor.predict(x_train),colour="red")
plt.title("hours vs scores(training set)")
plt.xlabel("hours")
plt.ylabel("scores")
plt.show()
```
### TEST SET GRAPH:
```
plt.scatter(x_test,y_test,color='purple')
plt.plot(x_test,regressor.predict(x_test),color='yellow')
plt.title("Hours vs Scores (Test Set)")
plt.xlabel("Hours")
plt.ylabel("Scores")
plt.show()
```
### VALUES OF MSE,MAE,RMSE
```
mse=mean_absolute_error(y_test,y_pred)
print('MSE = ',mse)
mae=mean_absolute_error(y_test,y_pred)
print('MAE = ',mae)
rmse=np.sqrt(mse)
print("RMSE= ",rmse)
```
## Output:
### df.head():
![image](https://github.com/user-attachments/assets/1845f889-5079-4d4f-8241-ae2c1b40783b)
### df.tail():
![image](https://github.com/user-attachments/assets/698a5498-9af2-4a20-be72-10ef781d3507)
### ARRAY VALUE OF X:
![image](https://github.com/user-attachments/assets/b808ef52-3dd9-4fbc-979b-e1c49fdb7372)
### ARRAY VALUE OF Y:
![image](https://github.com/user-attachments/assets/c00df820-cdf3-40a8-b5c6-21a012a5b679)
### VALUES OF Y PREDICTION:
![image](https://github.com/user-attachments/assets/2c9c548d-18ce-4baa-a834-dae5213c152f)
### ARRAY VALUES OF Y TEST:
![image](https://github.com/user-attachments/assets/4aa91477-cff9-491f-9ce3-63aa821199a9)
### TRAINING SET GRAPH: 
![image](https://github.com/user-attachments/assets/6f61873f-024b-46a4-897b-0a8fd2eb3a5e)
### TEST SET GRAPH:
![image](https://github.com/user-attachments/assets/2373041c-bbd1-46a0-ac2f-3780f7548972)
### VALUES OF MSE,MAE,RMSE
![image](https://github.com/user-attachments/assets/b6042cd3-87d8-4ed2-8e54-c79c6056a95f)





## Result:
Thus the program to implement the simple linear regression model for predicting the marks scored is written and verified using python programming.
