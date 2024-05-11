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
Developed by: P.Jeshwanth Kumar
RegisterNumber: 212223240114

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

# Result Output:

![image](https://github.com/Jeshwanthkumarpayyavula/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742402/87e2f972-32dd-48c1-8d48-b857f1cc3ecb)

# data.head()

![image](https://github.com/Jeshwanthkumarpayyavula/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742402/cab07cec-fe6b-456d-85ba-15d4dac71771)

# data.info()

![image](https://github.com/Jeshwanthkumarpayyavula/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742402/00842c82-0350-4aa4-884f-6d72c800706e)

# data.isnull().sum()

![image](https://github.com/Jeshwanthkumarpayyavula/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742402/5f288782-c918-4a0f-a23a-75ef14762c06)

# Y_Prediction value

![image](https://github.com/Jeshwanthkumarpayyavula/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742402/553edd7c-f8c1-42f0-822a-06b4a53e16d9)

# Accuracy Value

![image](https://github.com/Jeshwanthkumarpayyavula/Implementation-of-SVM-For-Spam-Mail-Detection/assets/145742402/3803e0d3-ebd0-4035-9ff4-8fd562a8c1b0)


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
