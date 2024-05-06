# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm:
#### Step 1 : Start
#### Step 2 : Data Collection
#### Step 3 : Data Preprocessing
#### Step 4 : Model Training
#### Step 5 : Model Evaluation
#### Step 6 : Prediction
#### Step 7 : Stop

## Program:
```
import pandas as pd
data=pd.read_csv("C:/Users/admin/Downloads/Salary.csv")
data.head()
```
## Output:
![Screenshot 2024-04-06 113914](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/7f7af2a7-d950-48b4-863b-5a88656860f6)

## Program:
```
data.info()
```
## Output:
![Screenshot 2024-04-06 114038](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/6d70f043-95c3-438a-bbda-d89f9b34655e)

## Program:
```
data.isnull().sum()
```
## Output:
![Screenshot 2024-04-06 114349](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/053cc254-9505-4b1b-8702-b7330a96e5fb)

## Program:
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()
```
## Output:
![Screenshot 2024-04-06 114239](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/880835a9-cfdc-4eea-ba7d-9d72091eae4b)

## Program:
```
x=data[['Position','Level']]
y=data['Salary']
```
## Program:
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
```
## Program:
```
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)
```
## Program:
```
from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_predict)
mse
```
## Output:
![Screenshot 2024-04-06 114729](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/7ce4bb95-9a93-4fb0-be98-13d0e51284b0)


## Program:
```
r2=metrics.r2_score(y_test,y_predict)
r2
```
## Output:
![Screenshot 2024-04-06 114805](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/05ce016e-42df-4348-9255-7e3b6a81b840)

## Program:
```
dt.predict([[5,6]])
```
## Output:
![Screenshot 2024-04-06 114856](https://github.com/Mkumar262006/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/147139472/642170c7-1ab4-4e8b-8059-6f0a5e3bcd53)


```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: MANOJ KUMAR S
RegisterNumber: 212223240082
*/
```

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
