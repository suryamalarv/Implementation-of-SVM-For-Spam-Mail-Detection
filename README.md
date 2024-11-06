# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

 1.Import the necessary python packages using import statements.

  2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

  3.Split the dataset using train_test_split.

  4.Calculate Y_Pred and accuracy.

  5.Print all the outputs.

  6.End the Program.
## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: SURYAMALAR V
RegisterNumber: 212223230224
*/
```
```
import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows-1252')
data.head()
```
![image](https://github.com/user-attachments/assets/f80295a1-6728-4a4c-ba1b-f96078fff18c)
```
data.tail()
```
![image](https://github.com/user-attachments/assets/a857314f-c979-47a2-a32e-38aa584d1cc4)
```
data.info()
```
![image](https://github.com/user-attachments/assets/bb380000-cd3e-49be-8e03-9a7279b12649)
```
data.isnull().sum()
```
![image](https://github.com/user-attachments/assets/61ab5d5d-a0c0-4318-9980-8c0b205e41ca)
```
x=data['v2'].values
y=data['v1'].values
```
```
y.shape
```
![image](https://github.com/user-attachments/assets/0a1da91d-7de8-48c6-8e5a-8c6a9b9877ce)
```
x.shape
```
![image](https://github.com/user-attachments/assets/20e9f8e6-50df-46d7-a0f1-7f28bc8c60ec)
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
x_train.shape
```
![image](https://github.com/user-attachments/assets/2a7fd179-150a-4498-b051-43380e72242d)
```
y_train.shape
```
![image](https://github.com/user-attachments/assets/2a7fd179-150a-4498-b051-43380e72242d)
```
x_test.shape
```
![image](https://github.com/user-attachments/assets/e2608e0d-ca0b-472b-8dc6-84e20498ddb7)
```
y_test.shape
```
![image](https://github.com/user-attachments/assets/e6c3cc65-4235-4446-b2b6-6949c4fb702c)
```
from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()
x_train = cv.fit_transform(x_train)  
x_test = cv.transform(x_test)
```
```
x_train.shape
```
![image](https://github.com/user-attachments/assets/33faaa01-37a3-4225-8cfa-83371f0ce957)
```
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred 
```
![image](https://github.com/user-attachments/assets/59be76cb-1b80-452f-be61-77b9324ebd46)
```
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
![image](https://github.com/user-attachments/assets/c0a2f5ea-faa0-48d4-9c8f-708986216b33)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
