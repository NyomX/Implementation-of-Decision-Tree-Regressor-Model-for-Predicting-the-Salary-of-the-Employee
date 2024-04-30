# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.  Import the libraries and read the data frame using pandas.
2.  Calculate the null values present in the dataset and apply label encoder.
3.  Determine test and training data set and apply decison tree regression in dataset.
4.  calculate Mean square error,data prediction and r2.
   

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:Tarun S
RegisterNumber:212223040226
*/

import pandas as pd
 data=pd.read_csv("C:/Users/admin/OneDrive/Desktop/Salary.csv")
 data.head()
 data.info()
 data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
 le=LabelEncoder()
 data['Position']=le.fit_transform(data['Position'])
 data.head()
 x=data[['Position','Level']]
 y=data['Salary']
 from sklearn.model_selection import train_test_split
 x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_stat
 from sklearn.tree import DecisionTreeClassifier
 dt=DecisionTreeClassifier()
 dt.fit(x_train,y_train)
 y_predict=dt.predict(x_test)
 from sklearn import metrics
 mse=metrics.mean_squared_error(y_test,y_predict)
 mse
 r2=metrics.r2_score(y_test,y_predict)
 r2
dt.predict([[5,6]])
 
 
```



## Output:
Data.head()

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/8e40edbc-0435-4cf4-8dd8-c4d91fd39edb)

Data.info()

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/bcf1f4a2-b3ce-4b97-8857-b2363c57e02a)


#data.isnull().sum()

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/00e4d7e4-e203-4b0b-9611-fa75feef14d5)

Data.Head() for salary:

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/149dcf5c-3432-4b25-b78c-ec56094c8ced)

#MSE Value:

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/bfbe64f5-bee6-4684-88a1-4521ae9455a5)

#r2 Value:

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/53d2f973-8b1f-46a1-9117-6e8c4c7b8fe5)

#Data Prediction:

![image](https://github.com/NyomX/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/145953580/1a778706-3a24-4a33-8ed5-084be6a7e637)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
