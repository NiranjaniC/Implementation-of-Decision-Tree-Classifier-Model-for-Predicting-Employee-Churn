# Implementation-of-Decision-Tree-Classifier-Model-for-Predicting-Employee-Churn

## AIM:
To write a program to implement the Decision Tree Classifier Model for Predicting Employee Churn.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.mport pandas module and import the required data set.
2.Find the null values and count them.
3.Count number of left values.
4.From sklearn import LabelEncoder to convert string values to numerical values.
5.From sklearn.model_selection import train_test_split.
6.Assign the train dataset and test dataset.
7.From sklearn.tree import DecisionTreeClassifier.
8.Use criteria as entropy.
9.From sklearn import metrics.
10.Find the accuracy of our model and predict the require values.

## Program:
```
/*
Program to implement the Decision Tree Classifier Model for Predicting Employee Churn.
Developed by: Niranjani.C
RegisterNumber:  212223220069

import pandas as pd
data = pd.read_csv("Employee.csv")
data
data.head()
data.info()
data.isnull().sum()
data["left"].value_counts
from sklearn.preprocessing import LabelEncoder
le= LabelEncoder()
data["salary"]=le.fit_transform(data["salary"])
data.head()
x= data[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
y=data["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state = 100)
from sklearn.tree import DecisionTreeClassifier
dt = DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
from sklearn import metrics
accuracy = metrics.accuracy_score(y_test,y_pred)
accuracy
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
*/
```

## Output:
![Screenshot 2024-09-30 155436](https://github.com/user-attachments/assets/2c68f10d-1cf9-47e3-b2e6-0215be188271)
![Screenshot 2024-09-30 155614](https://github.com/user-attachments/assets/9f16467e-5e88-47f9-9c7d-00fdfe5d5998)
![Screenshot 2024-09-30 155701](https://github.com/user-attachments/assets/d1519780-e12a-4ae3-9ddc-43040080e9c6)
![Screenshot 2024-09-30 155724](https://github.com/user-attachments/assets/677f0c3c-6d61-40c8-8b83-8b7161251a98)
![Screenshot 2024-09-30 155853](https://github.com/user-attachments/assets/205c3bb7-934a-4e88-8923-ceef1773032b)
![Screenshot 2024-09-30 155913](https://github.com/user-attachments/assets/0ae8ea64-fce4-49e7-b459-7450d17a5005)
![Screenshot 2024-09-30 160514](https://github.com/user-attachments/assets/f9c335cc-e9ec-4f3f-bc62-453212ef056f)
![Screenshot 2024-09-30 160240](https://github.com/user-attachments/assets/ae03ac3b-028d-417a-9aba-dd0090a7b48d)



## Result:
Thus the program to implement the  Decision Tree Classifier Model for Predicting Employee Churn is written and verified using python programming.
