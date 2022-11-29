# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the required packages.

2.Import the dataset to operate on.

3.Split the dataset.

4.Predict the required output.

5.End the program.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: NAVEENKUMAR V
RegisterNumber: 212221230068

import pandas as pd
data=pd.read_csv("/content/spam.csv",encoding='Windows-1252') 

import chardet
file='/content/spam.csv'
with open(file,'rb')as rawdata:
  result=chardet.detect(rawdata.read(100000))
result

data.head()

data.isnull().sum()

x=data["v1"].values 

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics 
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
*/
```

## Output:
![SVM For Spam Mail Detection](sam.png)
![image](https://user-images.githubusercontent.com/94165322/204452205-b4f036b7-5e02-4175-ad6b-b6e7128ff8e9.png)
![image](https://user-images.githubusercontent.com/94165322/204452230-fa3580d9-f497-44a0-8864-50b1e5108924.png)
![image](https://user-images.githubusercontent.com/94165322/204452245-8800e1e0-2efe-4984-937e-4ad55f496e0d.png)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
