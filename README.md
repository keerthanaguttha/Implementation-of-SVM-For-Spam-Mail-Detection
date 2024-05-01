# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary packages.
2.Read the given csv file and display the few contents of the data.Assign the features for x and y respectively.
3.Split the x and y sets into train and test sets.Convert the Alphabetical data to numeric using CountVectorizer.
4.Predict the number of spam in the data using SVC (C-Support Vector Classification) method of SVM (Support vector machine) in sklearn library.
5.Find the accuracy of the model.

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Guttha Keerthana
RegisterNumber: 212223240045

import chardet
file = '/content/spam.csv'
with open(file,'rb') as rawdata:
  result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data= pd.read_csv("/content/spam.csv",encoding='Windows-1252')

data.head()

data.info()

x=data["v1"].values

y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

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
## Result Output:

![image](https://github.com/keerthanaguttha/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742927/8edf97bf-d362-4e05-a777-2f139b423d46)

## data.head()

![image](https://github.com/keerthanaguttha/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742927/dec92239-9bb4-42f5-b85a-a79e602c4f32)

## data.info()

![image](https://github.com/keerthanaguttha/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742927/7b40980c-c631-4fc0-b674-e8bb128cd295)

## data.isnull().sum()

![image](https://github.com/keerthanaguttha/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742927/b5eb1005-6ecb-46c7-960c-a953b24910fe)

## Y_Prediction value

![image](https://github.com/keerthanaguttha/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742927/4faf2464-134f-4b73-bdd7-37be7eae681e)

## Accuracy Value

![image](https://github.com/keerthanaguttha/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742927/fd1b94fe-87de-41cd-a89e-4ca47b865cd8)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
